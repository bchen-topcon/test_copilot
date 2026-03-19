# AGENTS.md

This file provides guidance for AI coding agents (e.g., GitHub Copilot, Claude, GPT-based agents) working in this repository.

---

## Repository Overview

**Repository:** `bchen-topcon/test_copilot`
**Purpose:** A test/sandbox repository for evaluating and developing AI coding agent workflows.

---

## Directory Structure

See [README.md](README.md) for the full, up-to-date project structure.

---

## How to Work in This Repository

### Getting Started

1. Read `README.md` for the high-level project description.
2. Read `docs/contributing.md` for contribution workflows.
3. Read `docs/coding-standards.md` for style and conventions.
4. Read `docs/architecture.md` for design context.

### Making Changes

- Make **focused, minimal changes** that address the stated task.
- Follow the coding conventions in `docs/coding-standards.md`.
- Do **not** modify unrelated files.
- Write or update tests when changing functional code.
- Update documentation in `docs/` when adding or changing significant behavior.

### Commit Messages

Follow the commit message format defined in [docs/contributing.md](docs/contributing.md).

### Pull Requests

- Fill in the pull request template at `.github/PULL_REQUEST_TEMPLATE.md`.
- Keep PRs small and focused on a single concern.
- Reference the related issue number in the PR description (e.g., `Closes #42`).

---

## Key Conventions

Follow the coding conventions in [docs/coding-standards.md](docs/coding-standards.md) (formatting, naming, documentation, and security) and the branch naming and workflow conventions in [docs/contributing.md](docs/contributing.md).

---

## What NOT to Do

- Do **not** commit secrets, credentials, or API keys.
- Do **not** push directly to `main` — open a pull request.
- Do **not** leave large commented-out blocks of code.
- Do **not** introduce new dependencies without documenting them.

---

## Testing

Unit tests live in files prefixed with `test_` (e.g., `test_calculator.py`). Run tests with:

```bash
python -m pytest
```

- Place new unit tests alongside the source files or in a `tests/` directory.
- Run all tests before submitting a pull request.
- Ensure no existing tests are broken by your changes.

---

## Getting Help

- Open a GitHub Issue using the templates in `.github/ISSUE_TEMPLATE/`.
- Tag the issue with the appropriate label (`bug`, `enhancement`, `question`).
