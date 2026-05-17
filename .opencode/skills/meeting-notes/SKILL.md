---
name: meeting-notes
description: Turn raw meeting transcripts, audio notes, or bullet-point scratch into clean, structured meeting notes. Use when the user asks to "write up the meeting", "summarize this call", "draft minutes for X", "turn this transcript into notes", or shares a Zoom/Granola/Otter dump and wants a digestible artifact for the team.
---

# Meeting notes

You are turning a raw meeting artifact (transcript, recording summary,
shorthand notes) into a clean, scannable meeting note.

## When to load

- User says "write up the meeting" / "summarize this call" / "draft
  minutes"
- User pastes a transcript or links a recording
- User wants to share what happened in a meeting with someone who
  wasn't there

## Output shape

Always produce **exactly** these sections, in this order, even if a
section is empty (write "(none)" rather than skipping it):

```md
# {{Meeting title}} — {{ISO date}}

**Attendees:** {{names, comma-separated}}
**Driver:** {{who ran it, if clear}}

## TL;DR
1-3 sentence summary. Lead with the outcome, not the topic.

## Decisions
- {{decision 1}} — owner: {{name}}
- ...

## Action items
- [ ] {{action}} — {{owner}} — due {{ISO date or "tbd"}}
- ...

## Open questions
- {{question}} — to resolve by {{when, if known}}
- ...

## Notes
{{Bullet log of substantive points, grouped by topic. No verbatim chat,
no "Sarah said hi" filler.}}
```

## Voice

- Past tense ("decided", "agreed", "punted") not present tense.
- Drop pleasantries, jokes, side conversations.
- Name owners; if someone owned a thing implicitly, attribute it.

## Pitfalls

- **Don't invent decisions.** If the transcript is ambiguous on
  whether something was decided, put it under Open questions instead.
- **Don't lose dissent.** If two people disagreed and the meeting
  punted, capture both positions briefly.
- **Don't reorder action items by priority** unless the user asks —
  preserve discussion order so people can match it to their memory.
