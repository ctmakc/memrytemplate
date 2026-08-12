# First private-fork bootstrap

Give this file to your AI assistant after forking and making the repository private.

## Instruction to the assistant

Initialize this repository as my professional long-term Memory Palace.

1. Verify that the repository is private before writing personal or confidential information. If you cannot verify privacy, do not write such information.
2. Read `AGENTS.md` and `ARCHIVE_POLICY.md` completely.
3. Read `INDEX.md` and all three files in `profile/`.
4. If I provide a full interview/profile Markdown file, save the uncompressed source as `private-profile/interview-full.md`. Treat it as a raw source of truth, not as default context.
5. Distill that source into compact current files:
   - `profile/PROFILE.md` — stable professional identity/context;
   - `profile/GOALS.md` — current medium/long-term goals and direction;
   - `profile/PREFERENCES.md` — working/communication/decision preferences.
6. Do not copy project-heavy detail into the profile. Create active cases for substantial ongoing projects instead.
7. Create/update `INDEX.md` so future agents can locate relevant active cases without scanning the repository.
8. From then on, write only at semantic checkpoints and follow compaction limits in `ARCHIVE_POLICY.md`.
9. Use active files as state snapshots. Preserve old history in Git history/archive instead of allowing files to grow indefinitely.
10. After each successful write, tell me repository, path and commit SHA.

## Recommended one-time validation

After bootstrap, ask the assistant:

> Summarize what you know about my professional context using only INDEX + profile files, then list active cases without loading their full contents.

A good answer should be useful but compact. If it is enormous, the profile is too bloated.