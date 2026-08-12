# MemryTemplate — personal AI Memory Palace

A lightweight GitHub-based long-term memory system for ChatGPT and other AI assistants.

## What this repository is

This repository is not a transcript dump. It stores compact, durable state that lets an AI assistant continue professional work across chats without rereading months of conversation.

The model is deliberately simple:

- **Profile** — stable professional context, preferences and long-term goals.
- **Active cases** — one canonical state snapshot per ongoing objective.
- **Archive** — closed/superseded history and old checkpoint detail.
- **Raw private sources** — optional source material kept only after the fork is made private.

## First-time setup

1. Fork this repository.
2. Rename the fork if desired, e.g. `MemPalace`.
3. **Make the fork private before adding any personal information.**
4. Connect the private repository to ChatGPT/GitHub.
5. In ChatGPT Custom Instructions, tell it to use this repository as professional long-term memory and to read `AGENTS.md` + `ARCHIVE_POLICY.md` before every memory write.
6. Send ChatGPT `BOOTSTRAP.md` and ask it to initialize the private fork.
7. Put any full interview/profile source material in `private-profile/` only after the repository is private.

## Repository map

```text
AGENTS.md                 AI operating rules
ARCHIVE_POLICY.md         write, compaction and privacy policy
BOOTSTRAP.md              first-run instructions
INDEX.md                  compact map of active knowledge
profile/                  durable professional profile and goals
cases/                    active case snapshots
archive/                  closed/superseded cases and old history
private-profile/          private raw source material after fork
_templates/               canonical templates
```

## Core principle

**Active memory is state, not history.**

An active case should tell the next agent what is true now, what was decided, what remains open and what to do next. Old detail belongs in Git history or `archive/`, not in an ever-growing active file.

## Privacy

The public template intentionally contains no personal information. Do not add personal, client-confidential or sensitive data until your fork is private.
