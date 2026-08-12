# Memory and archive policy

## Purpose

Maintain enough durable context for another AI agent to resume professional work accurately while minimizing context bloat, duplicated facts and stale history.

## Memory tiers

### Tier 1 — durable profile

`profile/PROFILE.md`, `profile/GOALS.md`, `profile/PREFERENCES.md`.

Contains only stable or medium-term professional facts and working preferences. Keep concise and consolidated. Do not copy full conversations here.

### Tier 2 — active cases

`cases/<domain>/<project-or-client>/<YYYY-MM-DD>-<objective>.md`

One canonical file per continuing objective. This is the primary working memory.

### Tier 3 — archive

`archive/` contains closed/superseded cases and checkpoint history removed during compaction.

### Tier 4 — raw private sources

`private-profile/` may contain raw interviews or source material only after the repository is private. Raw sources are evidence, not default context. Do not load them routinely after they have been distilled.

## Checkpoint trigger

Write when at least one occurs:

- substantial analysis or research is completed;
- material facts or constraints are established;
- a decision, price, strategy or position is chosen;
- a reusable deliverable is produced;
- project state changes materially;
- a meaningful stage is completed;
- the conversation moves to a materially different objective.

Do not write after every message and do not wait for an imaginary end-of-chat event.

## Case identity

Before creating a case, search by project/client, subject, key entities and objective. Update an existing case when the objective is substantially the same. Create another only for a materially different objective.

Statuses: `active`, `paused`, `closed`, `superseded`.

## Active case structure

Use `_templates/case.md`.

Upper sections are always the consolidated current truth. The checkpoint log records only what changed, not a recap of the entire discussion.

## Compression budget

Targets are guidelines, but agents should actively enforce them:

- active case target: **≤ 2,500 words**;
- active case hard compaction trigger: **~4,000 words**;
- checkpoint log in active file: **max ~8 recent entries or ~600 words**;
- `profile/PROFILE.md`: target **≤ 1,500 words**;
- `profile/GOALS.md`: target **≤ 1,000 words**;
- `profile/PREFERENCES.md`: target **≤ 1,500 words**.

When an active case approaches the hard trigger:

1. Rewrite current-state sections from scratch using only still-relevant facts.
2. Delete duplicate and superseded statements from the active snapshot.
3. Move older checkpoint entries or historically useful detail to `archive/checkpoints/<case-id>/<YYYY>.md`.
4. Keep links/references to important archived material instead of copying it back.
5. Ensure `Exact next action` is one short, executable instruction.

Compaction must preserve decisions, amounts, dates, named entities, selected alternatives, material rationale, deliverable locations and unresolved risks.

## Closing and archiving

When an objective is completed, abandoned or replaced:

- set status to `closed` or `superseded`;
- move the final consolidated case to `archive/cases/<domain>/<project-or-client>/` when practical;
- remove it from the active section of `INDEX.md`;
- add a compact archive reference if future retrieval is plausible.

`paused` cases may remain active when resumption is likely.

## Retrieval budget

For normal work, prefer:

1. `INDEX.md`;
2. relevant profile files;
3. 1–3 relevant active cases.

Do not bulk-load archive or raw interviews unless the question depends on historical detail. Search first, then fetch only the smallest useful set.

## Profile promotion rule

Promote a fact from a case/raw source into profile only if it is durable and likely to matter across multiple future conversations. Project-specific facts stay in project cases.

Do not promote guesses, temporary moods, one-off preferences or stale operational details.

## Privacy

Public template forks must contain no personal information. **Make the fork private before adding profile, interviews, clients or business-confidential data.**

Never store credentials, secrets, payment-card data, seed phrases or private keys.

Sensitive personal topics are excluded from professional memory by default.

## Commit policy

Use one commit per meaningful checkpoint, not per message. Suggested formats:

- `memory(profile): update durable context`
- `memory(projects): update <project>`
- `memory(sales): update <client>`
- `memory(archive): compact <case>`

After success, report repository, path and commit SHA. Never report a save before GitHub confirms it.