---
name: presentation-outline
description: Turn a topic, brief, or pile of notes into a slide-by-slide presentation outline with speaker notes. Use when the user says "outline a deck on X", "build me slides for X", "I'm presenting X next week, help me structure it", "what slides should this deck have", or wants the bones of a talk before building visuals.
---

# Presentation outline

You are turning raw material (topic, notes, doc) into a slide-by-
slide outline. Output is a written plan — not visuals.

## When to load

- User says "outline a deck", "structure a presentation",
  "what slides do I need"
- User has a topic and a time slot and needs a skeleton

## Approach

1. **Get the goal first.** What does the audience need to do, decide,
   or feel after this deck? If the user didn't say, ask once — then
   commit.
2. **Pick a spine** that matches the goal:
   - **Persuade** → Problem → Stakes → Solution → Ask
   - **Inform** → Context → Findings → Implications → Next steps
   - **Update** → Where we are → What changed → What's next
3. **One idea per slide.** If a slide has two ideas, split it.
4. **Speaker notes are the script** — not bullet points repeated.

## Output

```md
# {{Title}}

**Audience:** {{who}}
**Goal:** {{what they should do/decide/feel}}
**Length:** {{N slides for an M-minute slot}}

---

## Slide 1: {{title}}
**Visual:** {{1-line description of what's on the slide}}
**Speaker notes:** {{2-4 sentences of what to say}}

## Slide 2: {{title}}
**Visual:** ...
**Speaker notes:** ...

...

## Slide N: {{title — usually "Ask" or "Next steps"}}
```

## Pitfalls

- **Don't open with a title slide-equivalent.** Slide 1 should hook
  or set stakes. Title slides are bookkeeping.
- **Don't bullet-overload.** If the visual is 7 bullets and the
  speaker notes restate them, you have one bad slide instead of
  one good slide and one good script.
- **End with a single ask.** Decks that close with "Questions?"
  waste the highest-attention moment.
