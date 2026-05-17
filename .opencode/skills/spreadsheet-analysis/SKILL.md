---
name: spreadsheet-analysis
description: Analyze tabular data (CSV, TSV, Excel paste) and produce a written summary with the key trends, outliers, and answers to user questions. Use when the user pastes a table, attaches a CSV, says "what does this data show", "analyze this spreadsheet", "find the outliers in X", or asks a data question against a dataset they share.
---

# Spreadsheet analysis

You are reading tabular data and producing a written analysis —
trends, outliers, and direct answers to the user's question.

## When to load

- User pastes CSV/TSV/Excel data or attaches a sheet
- User asks "what does this data show" / "analyze this"
- User has a specific question to answer against a dataset

## Approach

1. **Confirm the schema first.** State the columns, row count, date
   range (if any) before analyzing. Catches paste errors early.
2. **Answer the question first, evidence second.** If the user asked
   "is revenue growing?", lead with yes/no/maybe, then show the
   numbers.
3. **Compute, don't eyeball.** Use the available code/exec tool to
   actually run the math — don't guess from a screenshot.
4. **Flag what you can't tell.** Missing rows, ambiguous columns,
   sparse periods — say so explicitly.

## Output

```md
## Dataset
- {{N rows × M cols}}, {{date range}} {{if applicable}}
- Columns: {{col1}} ({{type}}), {{col2}} ({{type}}), ...
- Notes: {{any data-quality flags}}

## Answer
{{Direct answer to what the user asked, 1-2 sentences.}}

## Key findings
- {{finding 1, with the supporting number}}
- {{finding 2, ...}}
- {{finding 3, ...}}

## Outliers / oddities
- {{thing that looks weird, why}}

## What I couldn't tell
- {{question you can't answer from this data alone}}
```

## Pitfalls

- **Don't claim correlation is causation.** "Sales rose when we ran
  the campaign" ≠ "the campaign caused sales to rise."
- **Don't drop the units.** $10 vs 10% vs 10 units matters.
- **Don't over-aggregate.** A median can hide a bimodal distribution.
  Look at the shape before you summarize.
