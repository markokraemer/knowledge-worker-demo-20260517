---
name: competitive-scan
description: Research a competitor or peer company and produce a focused comparison brief — positioning, pricing, target customer, key differentiators, gaps. Use when the user says "look up X", "what's Y doing", "compare us to Z", "do a competitive scan", or wants intel on a specific company before a meeting/strategy session.
---

# Competitive scan

You are producing a focused brief on a competitor or peer company —
positioning, pricing, target customer, key differentiators, gaps.

## When to load

- User asks "look up X" / "what does Y do" / "compare us to Z"
- User wants intel before a meeting / strategy doc / pitch deck
- User wants to know where they're winning or losing vs a peer

## Approach

1. **Anchor in the user's own context first.** Ask: what does the
   user sell / who is their target? You can't compare without a
   reference point.
2. **Pull from primary sources first.** Their website, pricing
   page, docs, changelog, recent blog posts, recent funding /
   hiring signals. Press releases and analyst pieces last.
3. **Be specific, not vague.** "Strong on integrations" is useless;
   "Native Slack, Notion, Linear; missing GitHub" is useful.

## Output

```md
# Brief: {{Company}}

## What they do
1-2 sentences. Plain English.

## Target customer
{{ICP — segment, size, role of the buyer}}

## Pricing
| Tier | Price | What's included | Gotchas |
| --- | --- | --- | --- |
| ... | ... | ... | ... |

## Positioning
How they describe themselves vs how the market sees them. Quote
their homepage tagline if it's load-bearing.

## Key differentiators (vs us)
- {{what they have we don't}}
- {{what we have they don't}}
- {{ambiguous — claimed but unverified}}

## Recent signals
- {{funding / hiring / launches in the last 6 months}}

## Where this matters for us
{{2-3 takeaways. Be opinionated.}}

## Sources
- {{URL}}
- ...
```

## Pitfalls

- **Don't trust the homepage uncritically.** Marketing copy ≠
  reality. Triangulate with docs and changelogs.
- **Don't compare on features alone.** Pricing, support, distribution,
  brand all matter.
- **Don't pad with stale info.** A 2-year-old blog post about their
  roadmap is worse than no info.
