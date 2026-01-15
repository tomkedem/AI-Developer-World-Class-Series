---
title: "Chapter 9 - Performance, Context, and Cost"
weight: 10
---

## **Chapter 9 - Performance, Context, and Cost**

### How Too Much Context Hurts Quality

The first instinct when working with a code agent is to give it everything.

All the files.

All the history.

All the context.

The intention is good.

If it understands more, it will work better.

But in practice, too much context hurts quality.

When an agent sees too much code at once,

it struggles to distinguish between what matters and what does not.

Between critical code and incidental code.

Between a core decision and historical noise.

The result is solutions that are too generic.

Too cautious.

Or ones that try to “cover everything” instead of solving one problem well.

More context does not mean more understanding.

Sometimes it means the exact opposite.

A developer who directs the work does not ask,

“how much information can I give”,

but,

“what information is actually necessary for this task”.

Once context is reduced deliberately,

the agent works sharper.

More focused.

And most importantly, more relevant.

### Filtering Code Areas

Not all code is relevant to every task.

That is true for humans, and critical for code agents.

When code areas are not filtered, the agent does what it knows how to do:

it scans broadly.

Looks for patterns.

And tries to connect too many things at once.

The result is diffusion.

Filtering code areas is not hiding.

It is focusing.

You are telling the agent:

this is where the problem lives.

this is where impact is likely.

and the rest of the system only matters if we get there.

This filtering saves:

- unnecessary analysis  
- side changes  
- and “broad” solutions that are not actually required  

A developer who directs the work does not let the agent wander through the project.

They guide it to the area where value exists.

And when this is done consistently,

even large projects feel smaller,

or at least manageable.

### Working in Large Projects

In a small project, almost every change is felt immediately.

In a large project, a small change can disappear without a trace, or explode somewhere else entirely.

When a code agent enters a large project, its challenge is not writing.

It is navigation.

More files.

More layers.

More history it was never part of.

If you do not guide it, it will either try to be too cautious,

or do the opposite and touch too many places to “be safe”.

In both cases, the cost is high.

Correct work in large projects starts with reduction.

Not what the agent can see, but what it needs to see right now.

Which layer is relevant.

Where the entry point is.

And which parts of the system can be ignored at this stage without risk.

A developer who directs the work understands that in a large project,

success is not measured by how much code was written,

but by how little code needed to be touched.

Once you adopt this approach,

large systems stop feeling intimidating,

and become a sequence of focused problems that can be solved one by one.

### When It Is Better to Hide Information

Intuitively, hiding information feels like a disadvantage.

As if we are reducing the agent’s ability to understand the full picture.

But sometimes, hiding is exactly what enables understanding.

There is code that is not relevant to the current task.

There are layers that only add confusion.

And there is information that adds load without adding value.

When an agent sees everything, it feels obligated to consider everything.

It becomes overly cautious,

or suggests general solutions that try to fit every possible scenario.

Hiding information at the right time enables focus.

It says: this is the world we are working in right now.

The rest exists, but it does not need to occupy us at the moment.

A developer who directs the work is not afraid to hide.

They know it is temporary,

and that the information will return when it is genuinely needed.

When this is done correctly,

quality goes up,

and solutions become simpler and clearer.

### Reducing Runtime and Work Costs

Time is a resource.

And when a code agent works, it consumes time quietly.

You do not always feel it immediately.

Another run.

Another scan.

Another attempt to understand an overly broad context.

But every such action accumulates.

In time.

And in cost.

Reducing runtime does not start with technical optimization.

It starts with managerial decisions.

How much context is really needed.

Where you can stop early.

And when you do not need to “check everything”, only what matters.

The better the task is defined,

the more constrained the working space,

the faster and more accurately the agent works.

A developer who directs the work does not try to squeeze more and more out of the agent.

They try to make every run precise.

And when this is done consistently,

time shrinks,

costs go down,

and the work feels lighter.
