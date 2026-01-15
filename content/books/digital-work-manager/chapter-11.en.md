---
title: "Chapter 11 - Working in a Real Environment"
weight: 13
---

## **Chapter 11 - Working in a Real Environment**

### Legacy Code

Most real systems were not written yesterday.

They grew layer by layer, with decisions that made sense at the time,

and with code that no one remembers why it looks the way it does.

That is legacy code.

Not necessarily bad code.

Veteran code.

A code agent does not distinguish between new and old.

If you do not tell it otherwise,

it will treat legacy code like any other code:

something that can be improved, simplified, or “cleaned up”.

And that is exactly where the danger lies.

In legacy code, a small change can break behavior that no one can explain anymore,

but that someone still depends on.

A developer who directs the work does not let the agent “tidy up” legacy code.

They first ask for understanding.

What does this code do today.

Where does it touch the system.

And which changes are considered safe versus those that require special caution.

Sometimes the conclusion is not to touch it at all.

Sometimes only to wrap it with tests.

And sometimes to make a very small, very measured change.

The principle is simple:

with legacy code, you do not start with improvement,

you start with respect.

### Broken Tests

Broken tests are constant noise in real environments.

Sometimes they have been broken for months.

Sometimes they failed because of a completely different change.

And sometimes no one is even sure they are still relevant.

When a code agent encounters broken tests, it tries to “fix” them.

Adjust the code.

Update expectations.

Or simply work around them.

But a broken test is not necessarily a code problem.

Sometimes it is evidence that the system changed,

and the tests did not evolve with it.

A developer who directs the work does not let the agent automatically fix tests.

They first ask:

- what was this test trying to protect  
- is the behavior it checks still desired  
- and is its failure a sign of a real problem or just old debt  

Only after answering these questions

does it make sense to decide whether to fix, update, or delete it.

Broken tests are not an obstacle.

They are an opportunity to understand the gap between how the system is supposed to work

and how it actually works today.

### CI That Fails

CI systems run automated checks on every code change.

Their goal is simple: verify that the system still works after a change.

In an ideal system, a red CI means something is truly broken.

In a real system, that is not always the case.

Sometimes CI is broken because of an old change.

Sometimes because tests were never updated.

And sometimes simply because no one dealt with it in time.

When a code agent encounters a failing CI,

it tends to see it as a problem that must be fixed immediately.

Fix tests.

Update configuration.

Or “clean things up” until everything turns green.

This is where you need to stop.

A failing CI is not necessarily part of the task.

Sometimes it is just background noise.

A developer who directs the work does not let the agent chase green at all costs.

They first define:

- which tests are relevant to the current change  
- which failures truly block progress  
- and which can be left for separate work  

CI is an important tool,

but it also needs to be managed, not just obeyed.

### Messy Projects

Not every project is organized like the books suggest.

In reality, most are not.

Folders without a clear logic.

Files with overly generic names.

Code that handles multiple responsibilities at once.

This is not unusual.

It is everyday life.

When a code agent enters a messy project,

it looks for order.

It tries to organize, unify, “clean”.

But cleanup without understanding is a recipe for trouble.

In a messy project, external order does not always reflect internal logic.

Things that look accidental are often deeply tied to business logic.

Shortcuts have, over time, become part of the system.

A developer who directs the work does not ask the agent to “clean up” such a project.

They ask it first to understand how things actually work here.

Where changes usually pass through.

Which files are touched carefully.

And which mess is just mess, versus which signals a deeper constraint.

Only after that distinction is clear

is there room for improvement.

And in many cases,

the right decision is not to clean everything,

but to touch the minimum required to move forward without breaking things.

### When There Are No Docs and No Order

There are systems with almost no documentation.

No diagrams.

No explanations.

And sometimes no one left to ask.

This is not an edge case.

It is a common reality.

When a code agent enters such an environment,

it has no anchors.

Nothing to compare against.

No external “truth” to validate its assumptions.

In this situation, the biggest risk is moving forward too fast.

Changing before understanding.

Building on guesses that sound reasonable.

A developer who directs the work slows down intentionally.

They use the code itself as documentation.

They read flows.

They look for connection points.

And they move in small, reversible steps.

The agent can help a lot here,

but only if you give it the right role:

not “to fix”,

but “to discover”.

To identify how the system actually works today,

before trying to change it.

When you work this way,

even a system without docs and without order

becomes something you can understand,

and slowly, also improve.
