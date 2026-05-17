---
name: research-synthesis
description: Combine multiple sources (articles, papers, docs, notes, URLs) into a concise brief with citations. Use when the user says "summarize this research", "synthesize these articles", "what does the literature say about X", "give me a brief on Y", or pastes 3+ links/excerpts and wants one coherent writeup.
---

# Research synthesis

You are reading multiple sources and producing one short, citable
brief. The brief is for someone who hasn't read the sources.

## When to load

- User pastes/links multiple sources (3+) and wants a single writeup
- User asks "what does the research / literature say about X"
- User wants a primer before a meeting or decision

## Approach

1. **Read every source first.** Don't summarize one and bolt the rest
   on. If the user gave you 5 sources, your synthesis should reflect
   all 5.
2. **Find the through-line.** What do these sources agree on? Where
   do they disagree? What's the consensus, the contrarian view, and
   the open question?
3. **Cite inline.** Every claim → `[Source 1]` (numbered in the
   order they appeared in the input). Source list at the bottom.

## Output

```md
# Brief: {{topic}}

## TL;DR
2-3 sentence answer to the question being researched.

## What sources agree on
- {{point}} [1, 3, 4]
- ...

## Where they disagree
- {{contested point}}: {{view A}} [1, 2] vs {{view B}} [3]
- ...

## Open questions
- {{question}} — not covered by any source

## Sources
1. {{title or URL}}
2. ...
```

## Pitfalls

- **Don't hide disagreement** to make the brief tidier. Genuine
  conflict between sources is signal, not noise.
- **Don't introduce claims** not in the sources. If you know something
  the sources don't, flag it separately at the end as "Off-source
  context".
- **Don't cite vaguely.** "Studies show…" without a number is worse
  than no citation.
