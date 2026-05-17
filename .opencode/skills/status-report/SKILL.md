---
name: status-report
description: Produce a weekly status report from raw activity (commits, PRs, Linear/Jira tickets, Slack threads, meeting notes). Use when the user says "write my status update", "draft the weekly report", "what did I ship this week", "weekly digest for leadership", or wants a Friday wrap-up to send up the chain.
---

# Status report

You are turning a week of raw activity into a single status report
that leadership can read in under 90 seconds.

## When to load

- User says "write my weekly", "status update", "weekly digest"
- User pastes commits / Linear ticket dumps / meeting notes
- It's Friday and the user wants something to send up the chain

## Format

```md
# {{Name}} — Week of {{ISO date}}

## Shipped
- {{outcome, not activity}} — {{1-line context, link}}
- ...

## In progress
- {{thing}} — {{% complete or expected ship date}}

## Blocked / needs help
- {{blocker}} — {{what would unblock it}}

## Next week
- {{priority 1}}
- {{priority 2}}
- {{priority 3 — max}}

## Metrics
{{Only if user provided metrics. Don't invent.}}
```

## Tone rules

- **Outcomes, not activity.** "Shipped feature X" beats "Worked on
  feature X". If the work didn't ship, it goes in "In progress".
- **Brutal triage on Next week.** Max 3 items. If everything's a
  priority, nothing is.
- **No corporate hedging.** "On track" or "off track" — not
  "trending positively".

## Pitfalls

- **Don't dump every commit.** A status report is a summary, not a
  changelog.
- **Don't bury blockers.** They go above Next week so leadership can
  act on them.
- **Don't pad metrics.** If you can't measure it cleanly, leave it
  out — vanity metrics burn credibility fast.
