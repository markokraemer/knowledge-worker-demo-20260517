---
name: inbox-zero
description: Process an email inbox (pasted, exported, or via integration) and produce a triage plan: respond now, snooze, archive, delegate. Use when the user says "help me clear my inbox", "triage these emails", "what should I respond to", "I'm 200 emails behind", or shares an inbox export.
---

# Inbox zero

You are processing an inbox dump and producing a triage plan with
draft responses where the response is fast.

## When to load

- User pastes / exports an inbox
- User says "triage", "clear my inbox", "help me get to zero"
- User is buried and wants a defensible sweep

## Approach

For each message, decide one of:

- **Respond now** — needs a reply you can draft. ≤ 5 lines.
- **Snooze** — needs a reply but not this week. State the trigger.
- **Delegate** — belongs to someone else. Name them.
- **Archive** — no action needed. State why so user can sanity-check.

Use the "two-minute rule": if a reply takes < 2 minutes to write,
draft it. Don't snooze quick wins.

## Output

```md
## Respond now ({{N}})
### {{Sender}} — {{Subject}}
**Why:** {{1-line context}}
**Draft reply:**
{{the reply}}

---
### {{next}}

## Snooze ({{N}})
- {{Sender}} — {{Subject}} — re-surface when {{trigger}}

## Delegate ({{N}})
- {{Sender}} — {{Subject}} → {{owner}} because {{reason}}

## Archive ({{N}})
- {{Sender}} — {{Subject}} — {{why archived}}
```

## Pitfalls

- **Don't archive without stating why.** Two days later the user
  will wonder if you dropped something important.
- **Don't snooze everything.** If 80% of the inbox is "snooze",
  you're punting, not triaging.
- **Don't draft responses that commit the user to things** they
  haven't agreed to. Flag those as "needs decision before reply".
