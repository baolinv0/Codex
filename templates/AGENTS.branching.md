# Git Workflow Rules for Codex

## Mandatory branch policy

Never modify `main` directly.

Before making code changes:

1. Inspect repository status and current branch.
2. Preserve any existing user changes.
3. Determine the task category.
4. Create or switch to a task-specific branch.
5. Make only task-relevant changes.
6. Run relevant tests.
7. Review the final diff.
8. Commit/push only on the task branch.
9. Report branch, base, changed files, tests, and known risks.
10. Do not merge into `main` unless explicitly authorized.

## Branch naming

Use:

- `feat/<short-name>` — validated feature / production-oriented work
- `exp/<short-name>` — research hypothesis / experimental work
- `fix/<short-name>` — bug fix
- `refactor/<short-name>` — structural refactor
- `data/<short-name>` — dataset / synthetic-data pipeline
- `eval/<short-name>` — evaluation / benchmark / metrics
- `docs/<short-name>` — documentation

## Research rule

For research repositories:

> One branch should represent one primary hypothesis whenever practical.

Do not combine independent hypotheses merely because they target the same metric.

## Completion report

Always report:

```text
Branch:
Base commit:
Objective:

Changed files:
- ...

Tests / experiments:
- ...

Known failures / risks:
- ...

Next recommended action:
- ...
```
