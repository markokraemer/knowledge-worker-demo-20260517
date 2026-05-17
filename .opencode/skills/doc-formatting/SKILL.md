---
name: doc-formatting
description: Restructure a long, unstructured doc into a scannable, well-formatted version with TOC, headings, callouts, and tight prose. Use when the user says "clean up this doc", "format this", "this is too long, structure it", "add a TOC", or shares a wall-of-text and wants it readable.
---

# Doc formatting

You are taking a long-form doc that is unstructured (or badly
structured) and producing a clean, scannable version.

## When to load

- User shares a long doc that has no headings / poor headings
- User says "make this scannable", "add structure", "format this"
- User wants a TOC added or sections reordered

## Approach

1. **Identify the natural sections** by re-reading the whole doc.
   Don't impose structure that isn't there; surface what's already
   implicit.
2. **Write a 1-line section summary** before each heading so a
   reader can skim the doc by reading just the headings + summaries.
3. **Tighten prose mercilessly.** Drop "in order to" → "to", "due to
   the fact that" → "because", any sentence that doesn't add a new
   idea.
4. **Use callouts for the load-bearing parts** — the decision, the
   warning, the example. Markdown:

   ```
   > **Decision:** {{...}}
   > **Why:** {{...}}
   ```

## Output structure

```md
# {{Title}}

> **TL;DR** — 1-3 sentences capturing the doc's point.

## Contents
- [Section 1](#section-1)
- ...

## Section 1
One-line summary of what this section says.

{{Tightened prose, lists where appropriate, callouts for the
load-bearing claims.}}

## Section 2
...
```

## Pitfalls

- **Don't change the meaning** when tightening prose. If you're
  unsure whether a hedge is load-bearing, keep it.
- **Don't add headings the doc doesn't earn.** A 200-word memo
  doesn't need 6 sections.
- **Don't bury the lede** in a new section. The TL;DR should answer
  the question the doc raises.
