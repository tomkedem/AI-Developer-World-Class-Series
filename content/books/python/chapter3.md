
---

## 📘 קובץ 4: chapter3.md  
פרק שלישי עם קוד אמיתי

```markdown
---
title: "בניית כלי AI ראשון"
weight: 3
---

בפרק זה נבנה כלי שעושה שימוש במודל AI.

דוגמה:

```python
from transformers import pipeline

clf = pipeline("sentiment-analysis")
result = clf("I love AI") 
print(result)
