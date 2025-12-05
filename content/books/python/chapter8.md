---
title: "פרק 8 – חריגות, לוגים ואבחון"
weight: 9
---
# **פרק 8 – חריגות, לוגים ואבחון**
## **למה טיפול בשגיאות הוא קריטי ב-AI**
מערכת מבוססת AI שונה ממערכת רגילה בכך שהיא לעולם אינה יודעת הכול.
היא לומדת, משערת, מנחשת, ולפעמים פשוט טועה.
אבל יש גורם אחד שאסור לו לטעות, **המהנדס** שבונה אותה.
ולכן, טיפול בשגיאות ולוגים הוא לא רק נושא טכני, זו **שכבת ביטחון מנטלית**: מה יקרה כשהכול ישתבש?
**מפתח בלי טיפול שגיאות, זה כמו טייס בלי מכשור.** 

## **try / except / else / finally – המבנה הבסיסי**
כל שפת תכנות מציעה דרך להתמודד עם שגיאות.
בפייתון, זה נעשה באמצעות בלוק try/except, עם שני תוספים חשובים: else ו-finally.
```python
def load_model(path: str):
```
    try:
```python
        print("טוען מודל...")
        with open(path, "rb") as f:
            model = f.read()
```
    except FileNotFoundError:
```python
        print("❌ הקובץ לא נמצא.")
```
    except Exception as e:
```python
        print(f"⚠️ שגיאה לא צפויה: {e}")
```
    else:
```python
        print("✅ המודל נטען בהצלחה.")
```
    finally:
```python
        print("ניקוי משאבים...")
```
**הסדר חשוב:**
Try  –קוד שעלול להיכשל.
Except  –טיפול בשגיאות ידועות או כלליות.
Else  –קוד שרץ רק אם **לא** הייתה שגיאה.
Finally  –קוד שרץ תמיד, גם במקרה של כישלון (לניקוי משאבים, סגירת חיבורים וכו').
במערכות AI אמיתיות נשתמש כמעט תמיד בכל הארבעה. במיוחד כשיש קריאות API, קריאה מקבצים או טעינת מודלים.

## **יצירת חריגות מותאמות (Custom Exceptions)**
ככל שהמערכת שלך גדלה, תרצה לדעת לא רק ש"הייתה שגיאה" אלא **איזה סוג שגיאה** ולמה.
במקום לזרוק Exception כללי, ניצור חריגות מותאמות משלנו.
```python
class ModelNotFoundError(Exception):
```
    """נזרקת כאשר קובץ המודל חסר."""
    pass

```python
class InvalidDatasetError(Exception):
```
    """נזרקת כאשר מבנה הנתונים שגוי."""
    pass

```python
def load_dataset(path: str):
```
    if not Path(path).exists():
```python
        raise InvalidDatasetError(f"הקובץ {path} לא קיים.")

```
יתרון עצום של גישה זו הוא יכולת טיפול ממוקדת:
try:
    load_dataset("data/train.csv")
except InvalidDatasetError as e:
```python
    logger.error(f"שגיאה בטעינת הנתונים: {e}")
```
כך אפשר להבדיל בין "בעיה בנתונים" לבין "בעיה ברשת", בין "מודל חסר" ל"טוקנים שנגמרו".

## **logging בסיסי – רמות INFO/WARNING/ERROR**
קריאות print הן כמו הודעות בוואטסאפ, הן זמניות ונעלמות.
לוגים, לעומת זאת, הם **היסטוריה רשמית של מה שהתרחש**.
```python
import logging

```
logging.basicConfig(
    level=logging.INFO,
    format="%(asctime)s [%(levelname)s] %(message)s",
    encoding="utf-8"
)

logging.info("המערכת הופעלה")
logging.warning("המודל איטי מהרגיל")
logging.error("טעינת dataset נכשלה")

רמות הלוגינג:
**DEBUG** –למידע מפורט על זרימת הקוד.
**INFO**  –לאירועים רגילים.
**WARNING**  –בעיה לא קריטית.
**ERROR** –תקלה חמורה אך ניתנת להתאוששות.
**CRITICAL**  –כשצריך לעצור הכול ולקרוא למתכנת באמצע הלילה.
במקום print, השתמש תמיד ב-logger. הוא יודע לרשום לקבצים, 
ל-stdout, ל-syslog, ולשירותים כמו ELK או Datadog.

## **Structured Logging – extra dict ו-correlation ID**
כשיש לך עשרות microservices, מאות משתמשים ומיליארדי טוקנים, לוגים רגילים כבר לא מספיקים.
Structured Logging מאפשר להוסיף **שדות קבועים** לכל הודעה, כך שמערכות ניתוח לוגים (כמו Kibana או Grafana) יוכלו לפלטר, לקבץ ולזהות בעיות במהירות.
```python
import logging
import uuid

logger = logging.getLogger(__name__)
logging.basicConfig(level=logging.INFO, format="%(asctime)s [%(levelname)s] %(message)s")

def process_request(user_id: str):
```
    correlation_id = str(uuid.uuid4())  # מזהה ייחודי לבקשה
    try:
```python
        logger.info("מתחיל עיבוד בקשה", extra={"correlation_id": correlation_id, "user_id": user_id})
  # comment
```
        raise ValueError("שגיאה מדומה")
    except Exception as e:
```python
        logger.error("כישלון בעיבוד", extra={"error": str(e), "correlation_id": correlation_id})

```
עקרון **Correlation ID**  (מזהה מתאם) נועד לאפשר מעקב אחרי כל בקשה או תהליך לאורך כל שלבי המערכת.
לכל בקשה מוקצה מזהה ייחודי, וכל הלוגים שנוצרים במהלכה כוללים את אותו מזהה. כך שניתן לעקוב אחר הזרימה שלה מתחילתה ועד סופה, גם במערכות מבוזרות או בפייפליין מורכב.

## **דוגמה מרכזית: עטיפת pipeline עם לוגים וחריגות**
נראה עכשיו איך משלבים הכול יחד במערכת אחת שעושה ניקוי נתונים
ו-AI Inference.
```python
import logging
import pandas as pd
from pathlib import Path

logger = logging.getLogger("pipeline")
logging.basicConfig(level=logging.INFO, format="%(asctime)s [%(levelname)s] %(message)s", encoding="utf-8")

class PipelineError(Exception):
```
    pass

```python
def load_data(path: Path) -> pd.DataFrame:
```
    if not path.exists():
```python
        raise FileNotFoundError(f"לא נמצא הקובץ {path}")
    df = pd.read_csv(path, encoding="utf-8")
```
    if df.empty:
        raise PipelineError("ה-dataset ריק")
```python
    return df

def run_inference(df: pd.DataFrame):
```
    if "text" not in df.columns:
        raise PipelineError("עמודה 'text' חסרה ב-dataset")
```python
    df["length"] = df["text"].str.len()
    return df

def main():
```
    try:
        logger.info("🚀 התחלת pipeline")
```python
        data = load_data(Path("data/input.csv"))
        result = run_inference(data)
        result.to_csv("data/output.csv", index=False, encoding="utf-8")
```
        logger.info("✅ pipeline הושלם בהצלחה")
    except PipelineError as e:
```python
        logger.error(f"❌ שגיאה בתהליך: {e}")
```
    except Exception as e:
```python
        logger.exception(f"⚠️ שגיאה כללית: {e}")
```
    finally:
        logger.info("🔚 סיום pipeline")

```python
if __name__ == "__main__":
```
    main()

דוגמה זו משקפת את המציאות: טעינה, עיבוד ושמירה של נתונים, עם טיפול בחריגות ולוגים. הכל במהלך אחד מסודר וברור.
**Best Practices**
**אל תבלעו חריגות**
except Exception: pass הוא אויב. עדיף לכתוב לוג ולטפל.
**השתמשו ב-logger במקום print**
כדי לשלוט ברמות, לנתב ולשמור היסטוריה.
**אל תחשפו מידע רגיש בלוגים**
```python
(סיסמאות, API keys).
```
**תעדו חריגות במבנה עקבי** 
סוג, זמן, מזהה בקשה.
**הוסיפו correlation ID** 
לכל תהליך ארוך או בקשה חיצונית.
**תנו שמות חריגה משמעותיים**  
לא CustomError, אלא ModelNotLoadedError.
**שמרו לוגים לקובץ נפרד בכל מודול חשוב**
```python
(למשל pipeline.log, api.log).
```
## **סיכום – לוגים טובים הם העיניים של המערכת**
בעולם שבו המידע זורם במהירות והמערכות מבוזרות, לוגים הם הדרך היחידה להבין מה באמת קרה.
חריגות אומרות לנו **מה נכשל**, ולוגים מספרים **איך זה קרה**.
במערכת AI חכמה, לא מספיק לדעת לטפל בשגיאה.
צריך לדעת **לזהות אותה בזמן, להבין את ההקשר, ולהמשיך לעבוד**.
לוגים טובים הם לא רעש, הם מצפן.
וכשמגיע הבאג הראשון בפרודקשן, הם יהיו הקול השפוי היחיד שיספר לך את האמת.
**תרשים זרימה של טיפול בשגיאות**
