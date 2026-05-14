---
name: feature-development-with-ui-and-engine
description: Workflow command scaffold for feature-development-with-ui-and-engine in vnpy.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /feature-development-with-ui-and-engine

Use this workflow when working on **feature-development-with-ui-and-engine** in `vnpy`.

## Goal

Implements a new feature that involves core engine logic and user interface, often with supporting files and documentation.

## Common Files

- `vnpy/trader/engine.py`
- `vnpy/trader/ui/mainwindow.py`
- `vnpy/trader/ui/widget.py`
- `vnpy/trader/wechat.py`
- `pyproject.toml`
- `docs/community/info/veighna_trader.md`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit or add core logic in vnpy/trader/engine.py.
- Edit or add UI logic in vnpy/trader/ui/mainwindow.py and/or vnpy/trader/ui/widget.py.
- Add new protocol or integration file (e.g., vnpy/trader/wechat.py).
- Update pyproject.toml for dependencies or configuration.
- Optionally, update documentation and i18n files.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.