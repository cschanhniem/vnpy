---
name: ci-workflow-and-dependabot-update
description: Workflow command scaffold for ci-workflow-and-dependabot-update in vnpy.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /ci-workflow-and-dependabot-update

Use this workflow when working on **ci-workflow-and-dependabot-update** in `vnpy`.

## Goal

Upgrades GitHub Actions workflow versions and/or refines Dependabot configuration for automated dependency management.

## Common Files

- `.github/workflows/pythonapp.yml`
- `.github/dependabot.yml`
- `.github/CODEOWNERS`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit .github/workflows/pythonapp.yml to upgrade action versions or tweak workflow logic.
- Edit or add .github/dependabot.yml to configure dependency update schedules.
- Optionally, update .github/CODEOWNERS for code review rules.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.