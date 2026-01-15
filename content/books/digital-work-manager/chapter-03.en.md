---
title: "Chapter 3 - Breaking Down Problems and Defining Tasks Correctly"
weight: 4
---

## **Chapter 3 - Breaking Down Problems and Defining Tasks Correctly**

### The Difference Between a Task That Is Too Broad and One That Is Too Narrow

One of the most common reasons a code agent “gets lost” is not a coding mistake,

but a task that was not defined correctly.

A task that is too broad sounds like a good idea at first.

Give the agent freedom.

Let it see the big picture.

In practice, this is exactly what causes it to scatter.

When you tell an agent “improve this module” or “do a refactor”,

it has to decide on its own:

what counts as an improvement,

where to start,

and which change is worth the cost.

At that point, it is no longer executing a task.

It is defining a task for itself.

On the other hand, a task that is too narrow suffocates its advantage.

Line level instructions, point changes without context,

turn it into a very slow code editor.

The balance is in the middle.

A good task for a code agent is:

- clear in its goal  
- defined in scope  
- and leaves room for choice within a frame  

Not “write code for me”,

and not “do whatever you think”.

But something like:

there is a problem here, this is the area, these are the constraints, and this result counts as success.

A developer who guides work learns to recognize this point.

Not by a fixed formula,

but by the feeling of when they are delegating responsibility intelligently and when they are simply giving it up.

### How to Cut a Problem So the Agent Does Not Get Lost

When a problem is not cut correctly, the agent is not wrong.

It simply does what it can.

It starts reading files.

Identifies patterns.

And tries to figure out on its own what matters and what does not.

This is exactly where drift begins.

To prevent this, the cut of the problem needs to be clear before you start.

Not at the implementation level, but at the intent level.

A good cut answers three simple questions:

- where in the system the problem actually lives  
- where you do not touch even if it is tempting  
- and what change counts as a sufficient solution, not a perfect one  

The agent does not need to know everything.

It needs to know where to focus.

When you do not define the focal point,

it will choose one itself.

And sometimes that is exactly the wrong point.

A developer who guides work does not try to predict every step the agent will take.

They try to reduce the space of possible mistakes.

When you do that,

the work becomes more precise, calmer, and most importantly more predictable.

### When to Break Things Apart and When to Keep a Sequence

There is a natural temptation to break every problem into small parts.

It feels organized.

Controlled.

Safe.

But not every problem likes being broken apart.

When you break too much, the agent loses context.

It solves parts separately,

but misses the flow between them.

On the other hand, when you leave a sequence that is too large,

it has to hold too many things in mind at once,

and starts improvising.

The important distinction is this:

breaking things apart is meant to clarify intent, not to break responsibility.

If the parts are tightly coupled,

if one change immediately affects the other,

it is better to keep a sequence and let the agent see the full picture.

If, on the other hand, there are clear stages,

where you can stop between them, check direction,

and only then continue,

that is a good place to break things apart.

A developer who guides work does not ask

“how small can I cut this”,

but

“where is it right to stop and review”.

Once you understand that difference,

it becomes easier to decide when to split and when to let a sequence run.

### Professional Pause: Resetting Context and Reopening a Task

There is a moment in working with a code agent when the task is no longer clear,

but no one stopped to say it.

The solution is not progressing.

The instructions get longer.

And the conversation fills up with small corrections.

That is a sign that the context is tired.

Resetting context is not a failure.

It is a professional action.

Instead of continuing to patch a sequence that has lost direction,

a developer who guides work knows to stop

and reopen the task.

Not to start from scratch technically,

but to rephrase what actually needs to happen.

A proper reset includes three things:

- a short and clear formulation of the goal  
- a renewed definition of the task boundaries  
- and a conscious decision about what is not included this time  

When you do this,

a lot of noise simply disappears.

The agent does not need more information.

It needs the right information.

When working with agents,

a long sequence is not a goal in itself.

It is a means.

And those who are willing to stop and reopen a task in time

save themselves hours of late fixes.

### Dividing Work Between Human and Agent

The most common mistake in dividing work with a code agent is thinking of division as task allocation.

Who does what.

Who writes which code.

But that is not the real division.

The important division is between decisions and execution.

The human decides:

- what the problem is  
- what counts as a good solution  
- and which constraints must not be broken  

The agent executes:

- searching through the code  
- trying implementations  
- making adjustments and changes within the given frame  

The moment the agent starts making fundamental decisions,

something has gone wrong in the division.

And the moment the human intervenes in every small detail,

the agent’s advantage disappears.

A good division looks like this:

the human defines direction,

the agent progresses within that direction,

and the human reviews and reorients as needed.

This is not a hierarchy of superiority.

It is a division of roles.

A developer who guides work does not give up thinking.

They simply move it to where it has the highest value.

### Everyday Examples From Real Projects

Most problems when working with a code agent do not come from extreme scenarios.

They come from a normal workday.

A request to add a small piece of logic.

A change in the behavior of an existing API.

A “small” refactor in code that already works.

In these situations, it is easy to think there is no need to stop and cut the problem properly.

Everything looks familiar.

Everything feels under control.

And then the agent:

- touches a file you did not intend  
- changes a flow you did not ask for  
- or solves one problem and creates another on the side  

Not because it did something unusual,

but because the task was defined too generally.

In examples like these, the difference between good work and frustrating work is small:

one sentence of context.

one clear boundary.

or a decision to keep a sequence instead of breaking it apart.

A developer who guides work learns to recognize these moments.

Not only in big projects,

but especially in the small, everyday changes,

where it is easiest to lose focus and let the agent “figure it out”.

And when you get used to defining tasks correctly there as well,

working with a code agent stops being a gamble,

and becomes a professional routine.
