# Agent instructions

This repository is durable professional memory for an AI assistant. Treat it as a compact handoff system, not a transcript archive.

## Read protocol

At the start of work that may depend on prior professional context:

1. Read this file and `ARCHIVE_POLICY.md`.
2. Read `INDEX.md`.
3. Read only the relevant files from `profile/`.
4. Search for the relevant active case by project, client, subject, entities and objective.
5. Read no more than the 1–3 most relevant active cases by default.
6. Read `archive/` or raw sources only when historical detail is actually required.

Do not scan the whole repository merely to feel informed. Context quality matters more than context volume.

## Write protocol

Write only at meaningful professional checkpoints: substantial analysis, material facts/constraints, a decision, price, strategy, completed deliverable, project-state change, completed stage, or meaningful objective change.

Before every write:

1. Read the current `ARCHIVE_POLICY.md`.
2. Search for an existing case.
3. Update the existing canonical case when the objective is substantially the same.
4. Create a new case only for a materially different objective.
5. Consolidate rather than append blindly.
6. Update `INDEX.md` when active case status, owner/project identity or exact next action materially changes.

Never claim a save succeeded until GitHub returns a commit SHA. After a successful memory write, report repository, path and commit SHA briefly.

## What belongs here

Store reusable professional context: projects, business decisions, clients, sales, marketing, pricing, operations, design work, professional learning, deliverables, constraints, project-specific preferences and next actions.

Do not store casual conversation, transient chatter or every message.

Do not store intimate, romantic, family-emotional or other sensitive personal conversations. Health information should not be stored unless the user explicitly asks for a professional-purpose record and it is necessary; prefer not to store it.

Never store passwords, API keys, private keys, seed phrases, authentication tokens, full payment-card/bank credentials or identity-document secrets.

## Active-memory rule

An active case is a **current state snapshot**. It should answer:

- What are we trying to achieve?
- What is true now?
- What constraints matter?
- What has been decided?
- What reusable outputs exist?
- What remains open?
- What is the exact next action?

It is not a diary. Replace superseded facts instead of keeping every historical version in the active section. Preserve important historical detail in Git history or `archive/`.

## User agency

Memory supports the user; it does not define the user. Do not infer permanent identity, values or life goals from a single conversation. Promote something into stable profile memory only when it is explicitly stated, repeatedly evidenced, or clearly durable.