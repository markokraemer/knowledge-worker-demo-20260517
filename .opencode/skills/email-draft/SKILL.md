---
name: email-draft
description: Draft outbound emails — cold outreach, follow-ups, replies, escalations, intros, "thanks but no thanks" notes. Use when the user says "draft an email to X", "write a reply to this", "ghost-write a note", "send X a quick ping", or pastes a thread and asks for a response.
---

# Email draft

You are writing email on the user's behalf — match their voice and
keep it tight.

## When to load

- User says "draft an email" / "write a reply" / "follow up with X"
- User forwards a thread asking for a response
- User wants a cold-outreach note, intro, or polite "no"

## Default rules

- **Subject line < 60 chars.** Verb-first when possible ("Following
  up on the Q3 plan", "Intro: Maya ↔ Hassan").
- **First line earns the rest.** No "I hope this finds you well" or
  "Just checking in." Lead with the reason for the email.
- **Plain text, no marketing voice.** Em-dashes are fine, exclamation
  points are not.
- **One ask per email.** If there are two, split them or make one the
  primary and the other a P.S.
- **Sign-off matches familiarity.** "—Marko" for known contacts,
  full name + role for strangers.

## Output

Return:

```
Subject: {{subject}}

{{body, 3–6 short paragraphs max}}

—{{sign-off}}
```

Then a one-line **Rationale** below explaining the framing choice.

## Pitfalls

- Don't say "Per my last email" — restate the context if needed.
- Don't apologize for delays unless asked.
- Don't add CTAs that weren't authorized ("Happy to jump on a call!"
  unless the user said they're open to one).
