---
title: "Chapter 7 - Checkpoints, Git, and Control of the Process"
weight: 9
---

## **Chapter 7 - Checkpoints, Git, and Control of the Process**

### Why Git Is Not Just Version Control but a Safety Brake

Most developers know Git as a version control tool.

Something that helps keep history, work in teams, and resolve conflicts.

When working with a code agent, Git takes on an additional role.

It becomes a safety brake.

When an agent works fast, makes many changes, and touches multiple files in sequence,

it is very easy to lose a sense of control.

Not because the code is bad,

but because it becomes hard to know when you crossed a line.

Git gives you a point of grip.

Not only to roll back if something breaks,

but to stop in time and say:

this is far enough.

Every commit is a decision.

An agreement to the change.

An approval that the direction is right.

A developer who directs the work does not use Git only at the end of the process.

They use it during the work,

as a way to slow down for a moment, look, and decide whether to continue.

Once you understand this,

Git stops being a purely technical tool,

and becomes part of managing the work with the agent.

### Creating Intentional Stopping Points

When working alone, stops happen naturally.

You write a bit, think, test.

With a code agent, everything moves faster.

Much faster.

If you do not create stops intentionally,

the work simply continues until the task is finished,

and sometimes until it is already too late to stop.

An intentional stopping point is a conscious decision.

Not because something broke,

but because it is time to check direction.

Such a stop can be:

- after a significant change  
- before moving to another layer of the system  
- or before merging several small fixes  

The goal is simple:

to make sure that what has been done so far truly serves the original goal.

A developer who directs the work does not wait for the moment when stopping becomes mandatory.

They build stops into the process.

When this happens,

working with a code agent stops feeling like a train without brakes,

and becomes a journey with clear stations.

### Understanding Checks Before Making Changes

Before changing code, most of us are used to checking whether it works.

With a code agent, you need to check something first.

Whether it understood.

Understanding checks do not look like automated tests.

They look like a pause and a conversation.

What the agent thinks the problem is.

Where it plans to make changes.

And which parts of the system it sees as related to the change.

If the agent cannot explain this simply,

it is probably not ready to write code yet.

Many mistakes are avoided at this stage.

Not because a bug was found,

but because a lack of understanding was discovered early.

A developer who directs the work does not rush to approve a change.

They make sure the direction is clear on both sides.

Once you get used to doing this,

many “unnecessary” fixes never get written in the first place.

### Professional Pause: Checking Understanding Before Continuing

Before a major change, most developers check code.

Few check understanding.

An understanding check is a short pause meant to ensure

that the agent and the human see the same system.

Not how the code is written,

but what it does,

and where it has impact.

Such a check does not require new code.

Sometimes it is enough to ask the agent to explain, in simple words:

- what it is about to change  
- why this is the right place  
- and which parts of the system might be affected  

If the explanation is too long,

vague,

or full of caveats,

that is a warning sign.

A developer who directs the work does not continue just because “it sounds reasonable”.

They continue when they understand.

A good understanding check saves a lot of backtracking.

It is also the simplest way to discover a gap early,

before it turns into a bug.

When working with agents,

code can move very fast.

Understanding does not always keep up.

A short pause here

keeps control throughout the process.

### Going Back Without Ego

Going back is sometimes perceived as failure.

We made a change, invested thought, and now we have to delete it.

When working with a code agent, this happens more often.

Not because the work is poor,

but because it is very easy to move fast in a direction that later turns out to be wrong.

This is where ego enters.

Ego says:

maybe we can fix it a bit more.

maybe add a condition.

it would be a shame to throw away what was already written.

But Git does not work with emotions.

It gives you a simple and clear option:

go back.

A developer who directs the work learns to use this option without hesitation.

Not out of disregard for the work that was done,

but out of respect for the system.

If the direction is wrong,

there is no value in improving it.

The ability to delete a change without regret

is one of the most important skills when working with a code agent.

Once ego is set aside,

the work becomes easier,

and decisions become cleaner.

### Versioning “Machine Proposals”

When working with a code agent, not every change is a final decision.

Many changes are actually proposals.

A proposal for direction.

A proposal for implementation.

A proposal for how to solve a problem.

The problem begins when a proposal is treated as if it were already a decision.

Merged too quickly.

Moved past without stopping to think.

Versioning machine proposals means one simple thing:

not every commit has to become part of the main story of the code.

Sometimes it makes sense to keep a change aside.

Sometimes it is worth comparing two proposals.

And sometimes the best proposal is the one you end up not using.

Git enables this, but it is primarily a mental decision.

To treat what the agent produces as a draft,

not as a finished product.

A developer who directs the work does not fall in love with the first proposal.

They keep it,

review it,

and decide whether it truly deserves to move forward.

When you work this way,

the agent stops being a source of pressure,

and becomes a source of options.

### Controlled Work Around Git and Diffs

Some tools are deliberately designed to slow down the pace of work.

Not because they are weak, but because they aim to prevent costly mistakes.

Aider is such a tool.

Aider is a command line tool that works inside an existing project,

and uses Git, a source control management system, to present changes in a controlled way.

Instead of changing files directly,

it presents every change as a proposal.

This proposal is shown as a diff,

meaning a clear difference between the current state of the code and the proposed change.

This allows you to see exactly which lines are about to change,

before deciding whether to approve the change.

This way of working is less fluid,

and less suitable for those who want to let a code agent run for long stretches without interruption.

But it is very well suited to situations where control matters more than speed.

The value of such tools is not that they write better code,

but the working frame they enforce.

There are no hidden changes.

No long sequence that is hard to understand or break apart.

Every step is presented separately, reviewable, and easy to discard if needed.

A developer who directs the work does not have to work this way all the time,

but it is important to know this pattern.

Because sometimes,

working through diffs

is the right way to keep a system stable,

especially when dealing with sensitive, shared, or hard to fix code.
