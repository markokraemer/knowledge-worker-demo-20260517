---
name: task-triage
description: Prioritize a backlog or to-do list using effort × impact, surface dependencies, and propose a sequence. Use when the user dumps a list of items and says "what should I do first", "help me prioritize", "triage my backlog", "what's the right order for this work", or has too much on the plate and wants a defensible cut.
---

# Task triage

You are prioritizing a pile of items into a defensible sequence.

## When to load

- User pastes a list of tasks / tickets / TODOs
- User asks "what should I do first" / "help me prioritize"
- User feels overwhelmed and wants a cut

## Approach

1. **Score each item on two axes:**
   - **Impact:** what gets unlocked or risked if this ships / doesn't
     ship? (high / medium / low)
   - **Effort:** how much time/coordination does it take?
     (small ≤ 1d, medium ≤ 1w, large > 1w)
2. **Identify dependencies.** If A blocks B, B's effective priority
   inherits from A.
3. **Cut, don't reorder.** If the list is too long, the answer is
   "drop these", not "do them later".

## Output

```md
## Top 3 this week
1. **{{task}}** — {{impact}} impact, {{effort}} effort, {{why now}}
2. ...
3. ...

## Next (queue)
- {{task}} — {{1-line rationale}}
- ...

## Cut (won't do)
- {{task}} — {{why not}}
- ...

## Blocked / waiting
- {{task}} — blocked on {{thing}}
```

## Pitfalls

- **Don't dodge the cut.** A triage that recommends doing 14 things
  isn't a triage.
- **Don't let urgency masquerade as importance.** A loud Slack
  thread isn't proof a task matters.
- **Don't reorder under-the-hood.** Ask for missing impact/effort
  context rather than guess.
