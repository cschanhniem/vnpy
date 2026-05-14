---
name: documentation-update-fusion-module
description: Workflow command scaffold for documentation-update-fusion-module in vnpy.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /documentation-update-fusion-module

Use this workflow when working on **documentation-update-fusion-module** in `vnpy`.

## Goal

Adds or updates documentation for the Fusion module, including agent, info, and strategy sections.

## Common Files

- `docs/fusion/agent/*.md`
- `docs/fusion/agent/*.rst`
- `docs/fusion/info/*.md`
- `docs/fusion/info/*.rst`
- `docs/fusion/strategy/*.md`
- `docs/fusion/strategy/*.rst`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit or add multiple markdown (.md) and reStructuredText (.rst) files under docs/fusion/agent/, docs/fusion/info/, docs/fusion/strategy/, and docs/fusion/index.rst.
- Update index.rst files to reflect new or changed documentation.
- Optionally, update docs/index.rst to include new sections.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.