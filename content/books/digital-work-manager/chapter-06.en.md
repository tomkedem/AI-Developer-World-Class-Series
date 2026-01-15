---
title: "Chapter 6 - Iterative Debugging and Dialogue with the System"
weight: 8
---

## **Chapter 6 - Iterative Debugging and Dialogue with the System**

### Working With Errors, Not Against Them

In classic development, an error is something that gets in the way.

Usually, you try to eliminate it quickly and get back to the “real work”.

When working with a code agent, errors are the real work.

Not because we like failures,

but because an error is the clearest feedback you get about what the system is actually doing.

A code agent that tries to fix a bug without seeing errors

is operating in the dark.

It will guess, add conditions, and try to work around the issue.

When you treat an error as information,

it becomes a navigation tool.

What broke exactly.

Where it broke.

And what that says about the assumptions we had about the code.

A developer who directs the work does not try to shield the agent from errors.

They use errors to guide it.

Instead of saying “no, this doesn’t work”,

they say: here is the output. Here is where it broke. Look at this.

Once you get used to thinking this way,

errors stop being a blocker

and become a path.

### Using Terminal Output as Feedback

Terminal output is not noise.

It is a conversation.

Many developers look at the terminal only to see whether something passed or failed.

Green or red.

Works or does not work.

When working with a code agent, the output itself is the raw material.

An error.

A warning.

A stack trace.

Even a log line that looks insignificant.

Each of these tells the agent something about the system,

but only if you let it slow down and look at it.

Instead of saying “it failed, try again”,

you can return the output and ask the agent to respond to it.

Not as a failure,

but as information.

What does this say about the flow.

Which assumption was wrong.

And which part of the code is not behaving as expected.

A developer who directs the work does not filter the output to “make it easier”.

They use it to be more precise.

And the more precise the feedback,

the more the fix shifts from random to systematic.

### How to Guide Without Writing Code Yourself

One of the hardest mental shifts when working with a code agent is letting go of the urge to write.

There is a problem, you roughly see what needs to change, and your hand wants to jump into the file.

But this is exactly where the agent’s value lies.

Guidance does not happen through lines of code,

but through framing.

You do not tell it how to fix something,

but where the behavior feels wrong.

Not what to write,

but what does not meet expectations.

For example,

instead of proposing a solution,

you return the output and ask what it says about the assumptions that were made.

Instead of pointing to a specific line,

you point to behavior.

The agent is good at trying implementations.

You are good at identifying direction.

When these roles are kept clear,

the work flows faster and breaks less along the way.

A developer who directs the work learns to hold back.

Not because they cannot write code,

but because they know when they should not.

### When to Let It Continue and When to Stop

One of the most important decisions when working with a code agent is not what to ask it to do,

but when not to interrupt.

There are moments when the agent is in a good flow.

It understands the problem.

The direction is right.

And the changes build up in a coherent way.

In that state, early intervention breaks the flow.

You stop a process that has not yet run its course.

But there are other moments, quieter ones,

where you must stop.

Not when there is an error,

but when there are not enough questions.

If the agent moves too fast without asking for clarification,

if it touches many files without stopping to explain why,

or if the solution becomes more complex than the problem justified,

that is a signal to stop.

The stop is not meant to “correct” the agent.

It is meant to check direction before continuing.

A developer who directs the work learns to distinguish between healthy flow

and a quiet run in the wrong direction.

Once you understand that difference,

it becomes much easier to know when to let go and when to hold for a moment.

### Fixing a Cross-File Bug Step by Step

Serious bugs almost never live in a single file.

They cut across layers.

Code, configuration, tests, and sometimes assumptions that were never written down.

This is where a code agent is at its strongest,

and also where the risk of drift is highest.

The fix does not start with a change.

It starts with understanding the sequence.

Which file encountered the problem first.

Where the behavior changed.

And how information flows between different parts of the system.

Instead of asking “fix it”,

you let the agent work in stages.

First, understand.

Then, suggest a direction.

Only then, touch the code.

At each stage, you stop and ask:

What changed now.

Which assumption turned out to be wrong.

And whether you are still solving the same problem.

A developer who directs the work does not rush to merge solutions.

They let the bug fully reveal itself before closing it.

When you get used to working this way,

cross-file bugs stop being a nightmare

and become a clear process, even if it is not a short one.
