# Repository Instructions

This repository is a handbook for reusable Codex engineering practices.

## Repository organization

Put content into the correct layer:

- `rules/`: mandatory behavioral or engineering constraints
- `workflows/`: end-to-end task procedures
- `techniques/`: specific effectiveness tips
- `templates/`: reusable project/task templates
- `cases/`: real project examples and retrospectives
- `docs/`: navigation and meta documentation

Do not place unrelated notes directly in the repository root.

## Git

Follow `rules/git-branch-policy.md`.

For future changes:

- never modify `main` directly;
- use a task-specific branch;
- do not auto-merge without explicit user authorization.

## Documentation quality

Each substantive article should identify its type where useful:

- Rule
- Workflow
- Technique
- Template
- Case

Prefer concise, reusable engineering guidance over chronological chat transcripts.
