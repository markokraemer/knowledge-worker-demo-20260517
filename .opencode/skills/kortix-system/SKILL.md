---
name: kortix-system
description: How the Kortix platform works — kortix.toml manifest, repo-native projects, session sandboxes (isolated VM + ephemeral branch), triggers (cron + webhook), per-project secrets, and the contract between Kortix config and OpenCode config. Load when answering questions about how Kortix runs, how to add a trigger, how secrets resolve, what `kortix.toml` keys mean, or what the agent can/cannot do inside a session.
---

# Kortix system

You're an agent running inside a Kortix session — an isolated VM
sandbox with this project's repo cloned onto its own branch. Edit and
commit freely; the branch is yours.

See the Kortix docs for the full `kortix.toml` schema.
