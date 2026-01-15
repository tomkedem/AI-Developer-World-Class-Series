---
title: "Chapter 2 - Boundaries, Responsibility, and Controlled Damage"
weight: 4
---

## **Chapter 2 - Boundaries, Responsibility, and Controlled Damage**

### What You Never Let a Code Agent Do

One of the most common mistakes when working with a code agent is thinking that everything is a matter of trust.

That if the tool is good enough,  
and if the instruction is clear enough,  
there is no reason for permanent restrictions.

In practice, the opposite is true.

Precisely because the agent is smart, fast, and proactive,  
there are things you never let it do.

Not because it is “incapable”,  
but because the responsibility is too high.

There are areas in a system where a wrong change is not a small bug,  
but an incident.

Critical business logic.  

Security code.  

Infrastructure.  

Or places where organizational context matters no less than the code itself.

In those areas, it does not matter how confident the agent sounds.  

It does not matter how convincing the proposal is.

The decision must stay with you.

A permanent restriction is not a lack of trust.

It is a sign of professional maturity.

A developer who guides work knows there are domains where:

- you can consult  
- you can ask for analysis  

but you do not let the agent execute on its own.

And that decision is not made in the middle of the work,

but in advance.

### Sensitive Files and No Touch Zones

Every serious system has files that look like any other file,

but an incorrect touch changes far more than it seems at first glance.

They are not always the biggest or most complex files.

Sometimes it is a small configuration file.

Sometimes code that touches permissions, money, or a critical data flow.

A code agent cannot identify “sensitivity” on its own.

It identifies patterns, names, and dependencies.

The real meaning of a file comes from context,  
and that context lives with you.

That is why it is important to define No Touch zones in advance.

Not as punishment, but as protection.

A No Touch zone is a place where:

- the agent can read  
- understand  
- and suggest  

but cannot make a change without a stop and explicit approval.

This definition prevents quiet mistakes.

The kind that pass tests, look fine,

and are discovered only much later.

A developer who guides work does not wait for the agent to touch a sensitive place in order to stop it.

They mark the boundary beforehand.

### Professional Pause: Information Boundaries, Secrets, and Security Responsibility

Not everything that exists in a project should enter the context of a code agent.

Agents do not understand organizational sensitivity.

They do not know what must never leave the system,

and what should simply never appear outside a server.

That responsibility always stays with the human.

A developer who guides work needs to ask in advance:

- which files contain secrets, keys, or access details  
- which data belongs to users or customers  
- and which parts of the code do not need to be read to perform the task  

A proper boundary is not meant to slow the agent down,

but to protect the system.

There is also a quieter, opposite risk.

An agent that invents a solution based on a dependency that does not actually exist.

A library that sounds trustworthy.

An API that sounds reasonable.

Or “standard” code that does not exist in the project.

That is why any change that introduces a new dependency

requires conscious human review.

Not because of distrust,

but because of responsibility.

When working with agents,

security is not a separate layer.

It is part of management.

And those who handle it upfront

do not need to put out fires later.

### When to Stop Even If It Is “On Track”

One of the most misleading situations when working with a code agent is when everything looks fine.

The agent is progressing.

The changes look reasonable.

The tests pass.

And yet, this is exactly the moment when sometimes you must stop.

“On track” does not mean “in the right direction”.

It only means there is currently no resistance.

A code agent can move consistently, neatly, and with clear reasoning,

and still solve the wrong problem,

or solve the right problem in the wrong place in the system.

The stop is not meant to fix an error.

It is meant to check direction.

To stop and ask:

- is this really the place we wanted to touch  
- do its assumptions match what we know  
- and does this change integrate correctly with the rest of the system  

A developer who guides work learns to recognize this moment.

Not when something breaks, but when something works too fast.

Stopping in time is not a delay.

It is part of control.

#### Professional Pause: When and How to Stop a Wrong Sequence

There is a moment in working with a code agent when something feels off.

Everything is moving.

There are no hard errors.

But the direction starts to drift.

That is the moment when a work lead needs to stop.

Not because there is failure,

but because there is accumulated risk.

A deliberate stop is a skill.

And it is very different from “telling the agent it did not work”.

When an agent tries to solve a problem again and again in the same way, it is not being stubborn.

It is simply working with the wrong context.

At that point, the problem is not the last solution, but what the agent already “believes” to be correct.

A proper stop includes three clear steps.

First, stop the sequence.

Do not let it continue with “just one more try”.

The sequence itself is part of the problem.

Then, clean the context.

You do not always need to delete everything, but you do need to recognize that the last conversation no longer serves the goal.

Finally, change the angle.

Do not fix the same solution, but redefine the problem.

Sometimes you even step one level back and ask what actually needs to happen.

This is not surrender.

It is control.

A developer who guides work knows when to keep steering,

and when to stop, clean, and restart with a different intent.

Because when working with agents, sequence is power.

But only as long as it is heading in the right direction.

### Why Trust Too Early Is a Mistake

Trust is a good thing.

When working with a code agent, it is also necessary.

But timing is everything.

Early on, when the agent still does not know the system,

when it still does not understand what is sensitive and what is incidental,

full trust is not a compliment.

It is a risk.

Many developers trust too early because the first results look good.

The code works.

The tests pass.

The explanations sound reasonable.

But at that stage, the agent is still operating mostly on informed guesses.

It fills gaps.

It chooses a direction that seems plausible to it.

Not because it is the right direction, but because it is the only direction it has.

Trust is built through time and consistency, not through a first success.

Only after you see how the agent handles:

- complex code  
- sensitive areas  
- and changes with wide impact  

can you begin to release more control.

A developer who guides work does not rush to give freedom.

They earn it gradually.

And this is not a sign of suspicion.

It is a sign of deep understanding of the situation.

### Defining Safety Rules Before the First Line of Code

Most problems when working with a code agent are not born in the middle of a change.

They are born before it starts.

Before the first line of code, there are several decisions that must be settled.

Not in code, but in your head.

What is the goal of the task.

Where touching is allowed.

Where you stop for review.

And what kind of change counts as failure even if it “works”.

Safety rules are not meant to restrict the agent.

They are meant to protect you.

Once the work has started, it is hard to stop and fix the frame.

There are already changes.

There is already context.

There is already a direction.

In contrast, defining rules early creates a calmer workflow.

For you and for the agent.

You do not need a long document.

You do not need a heavy process.

A few clear sentences are enough to:

- prevent unnecessary damage  
- avoid late interruptions  
- and make the work more predictable  

A developer who guides work does not start a task by asking

“what will the agent write”,

but by asking

“under what conditions do I feel safe letting it work”.

And that is the right starting point for the next chapter.
