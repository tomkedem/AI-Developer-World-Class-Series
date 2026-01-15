---
title: "Chapter 12 - Anti Patterns in Working with Code Agents"
weight: 14
---

## **Chapter 12 - Anti Patterns in Working with Code Agents**

### Overly General Tasks

This is the most common anti pattern, and the most expensive one.

An overly general task sounds good on paper.

“Improve performance.”

“Do refactoring.”

“Clean up the code.”

But for a code agent, this is not direction.

It is a vacuum.

When there is no clear definition of what success looks like,

the agent has to invent one.

And it will invent it based on what seems reasonable to it,

not on what you actually meant.

The result is almost always the same:

- too many files changed  
- changes you did not ask for  
- and code that looks clever but is disconnected from the real need  

The problem here is not that the agent “overdid it”.

The problem is that you did not tell it where to stop.

A developer who directs the work does not give vague tasks hoping to “see what comes out”.

They define a boundary, even if it is temporary.

Which area of the system.

What kind of change.

And what does not count as part of the task, even if it is tempting.

Once you do that,

many of the other anti patterns simply do not appear.

### Moving Forward Without Tests

This happens when everything seems to work.

The change is small.

The code is clean.

And the agent is moving fast.

So tests are skipped.

Not out of neglect,

but out of a feeling that “we will test later”.

When working with a code agent, this is one of the most dangerous patterns.

When the agent moves forward without tests,

it builds a chain on top of unverified assumptions.

Each change depends on the previous one,

and when something breaks, it is hard to know where it happened.

Tests are not only meant to find bugs.

They are an anchor.

They stop the flow at the right moment.

They clarify what actually changed.

And they allow you to continue with confidence, not guesswork.

A developer who directs the work does not let the agent run in a long sequence without checkpoints.

Even if it feels slower at first.

Because when tests come in too late,

the cost is always higher.

### Trusting a Green Test Without Understanding

A green test feels like approval.

Everything passed. You can move on.

But when working with a code agent, a green test is only a signal, not proof.

A test checks something very specific.

What it was written to check.

Not necessarily what you intended to protect.

When the agent sees a green test,

it assumes the direction is correct.

If you accept that without understanding what was actually tested,

both of you may move forward based on a false assumption.

This is a classic anti pattern:

everything works, but no one knows why.

A developer who directs the work does not ask only whether the test passed,

but what the test actually confirms.

Which behavior it protects.

Which scenario it does not cover.

And where there is still a gap, even if everything is green.

A green test without understanding is an illusion of safety.

Understanding without tests is a risk.

Professional work lives in between.

### Fixing the Result Instead of the Intent

This is a subtle anti pattern, which is why it is dangerous.

Something does not work.

The agent sees the wrong result,

and fixes it directly.

The output changes.

The test passes.

And the problem is “solved”.

But the original intent remains unclear.

Fixing the result focuses on what happened,

not on why it happened.

It bypasses the problem instead of addressing it.

Code agents are very good at this.

They identify where behavior is wrong,

and find a way to make it look right.

If you do not stop it,

the system accumulates layers of local fixes,

and each layer makes the original intent harder to understand.

A developer who directs the work does not settle for a correct result.

They ask:

- what was the original intent of the code  
- where did it break  
- and does this fix bring us back to that intent, or just hide the gap  

When the intent is clear,

the result usually follows.

When only results are fixed,

the cost is always paid later.

### How to Tell You Are Heading Toward Trouble

In most cases, a problem does not appear all at once.

It signals itself.

Not with a clear error,

but with a feeling that things are becoming heavier than they should be.

Too much code for a small change.

Too many explanations for a simple solution.

Or too many “it works” moments without understanding why.

These are early signals.

When working with a code agent, it is easy to miss them.

The pace is high.

Everything is moving.

And the system is still green.

A developer who directs the work learns to stop at these moments.

Not to hunt for a bug,

but to check whether the direction is still right.

This pause does not require drama.

Sometimes it is enough to ask one good question.

Or to ask the agent to explain, in simple words, what actually changed.

When you do this consistently,

most big problems are avoided long before they explode.
