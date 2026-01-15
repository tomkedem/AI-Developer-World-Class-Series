---
title: "Chapter 5 - Agent Failures and Repeating Error Patterns"
weight: 6
---

## **Chapter 5 - Agent Failures and Repeating Error Patterns**

### False Confidence

One of the most confusing things when working with a code agent is the confidence it projects.

The answers are structured.

The code looks clean.

And the explanation sounds reasonable.

And that is exactly where the problem begins.

That confidence does not come from a full understanding of the system.

It comes from the ability to produce a solution that looks reasonable in a partial context.

A code agent does not know when it does not know.

When information is missing, it does not stop.

It fills the gaps.

That is why confidence in an agent is not a sign of quality,

but a sign that it found a plausible path and continued down it.

Many developers fall into this trap because confidence is contagious.

If the explanation sounds good,

and the code passes tests,

it is easy to assume everything is fine.

But in practice, this is exactly the point where you should be most skeptical.

Not of the code, but of the path.

A developer who guides work learns to recognize this false confidence.

Not through a bug,

but through questions.

What assumptions was the solution built on.

What was not checked.

And what information is missing, even if the agent did not ask for it.

Once you understand that confidence is sometimes a warning sign,

working with a code agent becomes far more precise.

### Filling Gaps Instead of Asking Questions

When a code agent does not know something, it almost never asks.

It fills the gap.

If context is missing, it guesses.

If it is unclear why code was written in a certain way, it invents its own logic.

And if there are several reasonable ways forward, it picks one and continues.

From its perspective, this is the only way to make progress.

The problem is that filling gaps looks like understanding from the outside.

The code is written well.

The explanation sounds convincing.

Everything fits together logically.

But in reality, the choice was made without information that was obvious to you,

and often critical.

This is where the role of the Driver comes in.

A developer who guides work does not wait for the agent to ask.

They identify points where context is likely missing,

and stop there proactively.

Not to interrupt,

but to add information the agent cannot safely guess.

The more you practice this,

the easier it becomes to tell when a solution is based on knowledge,

and when it is based on gap-filling.

Once you can tell the difference,

many mistakes simply disappear.

### Fixing Symptoms Instead of Root Causes

One of the most frustrating patterns when working with a code agent is a solution that works,

but feels wrong.

The bug is gone.

The tests pass.

But something in the system feels stranger than before.

This happens when the agent fixes a symptom, not the root cause.

It sees an exception,

adds a check.

Sees a crash,

wraps it in a condition.

From its perspective, this is progress.

The problem is gone.

But in reality, the source of the problem is still there.

The fix only hides it.

A code agent is very good at putting out fires.

It is less good at asking why the fire started in the first place.

This is where responsibility comes back to you.

A developer who guides work does not settle for the problem disappearing.

They ask:

- why did this happen  
- does this fix strengthen the system or weaken it  
- and did we add complexity to avoid understanding  

The more you work with an agent,

the easier it becomes to recognize this moment.

The moment where everything is “fine”, but not really.

And when you stop there,

a temporary fix can turn into a real solution.

### Professional Pause: Preventing AI Spaghetti and Preserving Architecture

A code agent excels at reaching a working solution.

That is also its greatest weakness.

If you do not set clear boundaries,

it will choose the shortest path to a result,

even if that path damages the structure of the system.

This is how AI Spaghetti is created.

Code that works,

but is hard to understand,

hard to extend,

and hard to maintain over time.

The issue here is not code quality at the single-line level,

but a lack of respect for the existing architecture.

A developer who guides work does not check only whether the feature works,

but whether it works in the right way.

That means paying attention to things like:

- whether the agent used patterns that already exist in the project  
- whether it introduced a new dependency just because it was convenient  
- and whether file and function names speak the language of the system  

When code feels foreign to a project,

even if all tests are green,

that is a warning sign.

A professional pause at this stage saves future technical debt.

Sometimes the right fix is not to improve the solution,

but to discard it and redefine the frame.

Because when working with agents,

the code will always be fast.

Responsibility for the architecture will always be human.

### What Early Drift Looks Like

Drift does not start with a big bug.

It starts with a small detail that feels unimportant.

A change that went in without a check.

An assumption that was never stated out loud.

A file that was touched “just to make things easier”.

At this stage, everything still works.

There are no errors.

No obvious failures.

And that is exactly the problem.

Early drift looks like progress.

The code is moving.

The task is advancing.

And the agent is confident it is on the right track.

But if you stop for a moment and look from the outside,

you can see the signs:

- too many files changing for a small task  
- a solution that requires too long an explanation  
- or a change that feels “clever” but not necessary  

A developer who guides work learns to recognize these moments.

Not by a failure,

but by a sense of misalignment.

This is not mysterious intuition.

It is attention to patterns that repeat.

And the earlier you stop,

the easier it is to bring the work back on track before real damage is done.

### When the Problem Is Not Code but Management

When something goes wrong while working with a code agent, the first instinct is to look at the code.

Search for the wrong line.

Check the logic.

Assume the problem is technical.

But often, the code is only the symptom.

The real problem lies in task management.

In an imprecise definition.

In boundaries that were never marked.

Or in the decision to give too much freedom too early.

A code agent almost never “rebels”.

It does exactly what is possible within the frame it was given.

If it touched too many files,

if the solution went in a strange direction,

or if the change feels disconnected from the system,

it is worth stopping and asking not what it did,

but what you asked for.

A developer who guides work learns to take responsibility even when they did not write the code themselves.

Not out of guilt,

but out of understanding that this is the essence of the new role.

Once you recognize that the problem is managerial rather than technical,

the solution changes completely.

Less fixing of code.

More precision in guidance.

And this may be one of the most important lessons in this book:

when working with code agents,

many problems are solved not by better writing,

but by better management.
