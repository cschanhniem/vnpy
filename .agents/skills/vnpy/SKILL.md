```markdown
# vnpy Development Patterns

> Auto-generated skill from repository analysis

## Overview

This skill teaches the core development patterns, coding conventions, and collaborative workflows used in the `vnpy` Python codebase. `vnpy` is a quantitative trading framework with modular architecture, supporting extensible engines, user interfaces, and algorithmic modules. This guide covers file organization, code style, documentation, feature development, and testing practices to help maintain consistency and efficiency in contributions.

## Coding Conventions

**File Naming**
- Use `snake_case` for all Python files.
  - Example: `engine.py`, `main_window.py`

**Import Style**
- Prefer **relative imports** within packages.
  - Example:
    ```python
    from .engine import Engine
    from ..utils import some_utility
    ```

**Export Style**
- Use **named exports**; avoid wildcard (`*`) exports.
  - Example:
    ```python
    __all__ = ["Engine", "MainWindow"]
    ```

**Commit Messages**
- Prefix with tags such as `[Mod]`, `[Add]`, `chore`, `[Del]`, `[Fix]`.
- Keep messages concise (average ~41 characters).
  - Example: `[Add] Support for new WeChat notification`

## Workflows

### Documentation Update: Fusion Module
**Trigger:** When you need to add or update documentation for the Fusion module (agent, info, strategy).
**Command:** `/update-fusion-docs`

1. Edit or add `.md` and `.rst` files under:
    - `docs/fusion/agent/`
    - `docs/fusion/info/`
    - `docs/fusion/strategy/`
2. Update `docs/fusion/index.rst` to reflect new or changed docs.
3. Optionally, update `docs/index.rst` to include new sections.
4. Commit with a message like `[Mod] Update Fusion module documentation`.

**Example:**
```bash
# Edit docs/fusion/agent/new_agent.md
# Update docs/fusion/index.rst
git add docs/fusion/agent/new_agent.md docs/fusion/index.rst
git commit -m "[Add] Fusion agent documentation"
```

---

### CI Workflow & Dependabot Update
**Trigger:** When you need to upgrade CI workflows or update Dependabot settings.
**Command:** `/update-ci-dependabot`

1. Edit `.github/workflows/pythonapp.yml` to upgrade action versions or tweak logic.
2. Edit or add `.github/dependabot.yml` for dependency update schedules.
3. Optionally, update `.github/CODEOWNERS` for review rules.
4. Commit with a message like `chore: update CI workflow versions`.

**Example:**
```bash
# Edit .github/workflows/pythonapp.yml
# Edit .github/dependabot.yml
git add .github/workflows/pythonapp.yml .github/dependabot.yml
git commit -m "chore: update CI and Dependabot configs"
```

---

### Feature Development: UI and Engine
**Trigger:** When adding a new feature involving engine logic and UI (e.g., notification or communication features).
**Command:** `/add-notification-feature`

1. Edit/add core logic in `vnpy/trader/engine.py`.
2. Edit/add UI logic in:
    - `vnpy/trader/ui/mainwindow.py`
    - `vnpy/trader/ui/widget.py`
3. Add new protocol/integration file (e.g., `vnpy/trader/wechat.py`).
4. Update `pyproject.toml` if dependencies/configuration change.
5. Optionally, update documentation and i18n files.
6. Commit with a message like `[Add] WeChat notification support`.

**Example:**
```python
# vnpy/trader/wechat.py
class WeChatNotifier:
    def send(self, message: str):
        # Implementation
        pass
```
```bash
git add vnpy/trader/engine.py vnpy/trader/wechat.py
git commit -m "[Add] WeChat notification support"
```

---

### Alpha Module Enhancement and Fix
**Trigger:** When enhancing or fixing the `vnpy.alpha` module (e.g., new operators, bug fixes).
**Command:** `/update-alpha-module`

1. Edit/add files in:
    - `vnpy/alpha/dataset/`
    - `vnpy/alpha/model/models/`
    - `vnpy/alpha/strategy/`
    - `vnpy/alpha/lab.py`
2. Update/add tests in `tests/alpha/`.
3. Optionally, update `pyproject.toml` for configuration/typing.
4. Update `__init__.py` as needed.
5. Commit with a message like `[Fix] mypy warnings in alpha module`.

**Example:**
```python
# vnpy/alpha/dataset/new_operator.py
def new_operator(data):
    # Implementation
    pass
```
```bash
git add vnpy/alpha/dataset/new_operator.py tests/alpha/test_new_operator.py
git commit -m "[Add] New operator to alpha module"
```

## Testing Patterns

- **Test Framework:** Not explicitly specified; use standard Python testing conventions.
- **File Pattern:** Test files follow the `*.test.*` or `tests/alpha/*.py` pattern.
- **Placement:** Place tests in the `tests/alpha/` directory for alpha module features.
- **Example:**
    ```python
    # tests/alpha/test_new_operator.py
    from vnpy.alpha.dataset.new_operator import new_operator

    def test_new_operator():
        assert new_operator([1, 2, 3]) == expected_result
    ```

## Commands

| Command                | Purpose                                                        |
|------------------------|----------------------------------------------------------------|
| /update-fusion-docs    | Add or update Fusion module documentation                      |
| /update-ci-dependabot  | Update CI workflows or Dependabot configuration                |
| /add-notification-feature | Add new notification or communication feature (UI/engine)   |
| /update-alpha-module   | Enhance or fix the vnpy.alpha module                           |
```
