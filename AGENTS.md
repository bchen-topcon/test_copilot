# AGENTS.md

This file provides guidance for AI coding agents (e.g., GitHub Copilot, Claude, GPT-based agents) working in this repository.

---

## Repository Overview

**Repository:** `bchen-topcon/test_copilot`
**Purpose:** A test/sandbox repository for evaluating and developing AI coding agent workflows.

---

## Directory Structure

```
test_copilot/
├── AGENTS.md                  # This file — AI agent guidance
├── README.md                  # Human-facing project overview
├── .gitignore                 # Files excluded from version control
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   ├── bug_report.md      # Template for bug reports
│   │   └── feature_request.md # Template for feature requests
│   └── PULL_REQUEST_TEMPLATE.md  # Template for pull requests
├── docs/
│   ├── architecture.md        # System architecture overview
│   ├── contributing.md        # Contribution guidelines
│   └── coding-standards.md   # Coding style and conventions
└── src/
    └── README.md              # Placeholder for source code
```

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

Use the following format for commit messages:

```
<type>: <short description>

[optional body with more detail]
```

Types: `feat`, `fix`, `docs`, `refactor`, `test`, `chore`

Examples:
- `feat: add user authentication endpoint`
- `fix: correct null pointer in parser`
- `docs: update architecture diagram`

### Pull Requests

- Fill in the pull request template at `.github/PULL_REQUEST_TEMPLATE.md`.
- Keep PRs small and focused on a single concern.
- Reference the related issue number in the PR description (e.g., `Closes #42`).

---

## Key Conventions

| Concern              | Convention                                      |
|----------------------|-------------------------------------------------|
| Branch naming        | `feature/<name>`, `fix/<name>`, `docs/<name>`  |
| File naming          | `kebab-case` for docs, language-native for code |
| Indentation          | 2 spaces (YAML/JSON), 4 spaces (Python/C/C++)  |
| Line endings         | LF (`\n`)                                       |
| Max line length      | 100 characters                                  |

---

## What NOT to Do

- Do **not** commit secrets, credentials, or API keys.
- Do **not** push directly to `main` — open a pull request.
- Do **not** leave large commented-out blocks of code.
- Do **not** introduce new dependencies without documenting them.

---

## Testing

There is currently no automated test suite. When tests are added:

- Place unit tests alongside the source files or in a `tests/` directory.
- Run all tests before submitting a pull request.
- Ensure no existing tests are broken by your changes.

---

## Getting Help

- Open a GitHub Issue using the templates in `.github/ISSUE_TEMPLATE/`.
- Tag the issue with the appropriate label (`bug`, `enhancement`, `question`).
