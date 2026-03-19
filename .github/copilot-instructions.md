# GitHub Copilot Instructions

These instructions apply to all GitHub Copilot interactions and automated code reviews in this repository.

## Project Overview

This is a sandbox/test repository used to evaluate and develop AI coding agent workflows. It contains Python and C++ source files along with supporting documentation.

## Coding Standards Reference

All code in this repository must follow the conventions defined in [`docs/coding-standards.md`](docs/coding-standards.md). Key highlights:

- **Indentation:** 4 spaces for Python and C/C++; 2 spaces for YAML, JSON, and HTML.
- **Max line length:** 100 characters.
- **Line endings:** LF (`\n`).
- **Naming:** `snake_case` for Python variables and functions; `PascalCase` for classes; `UPPER_SNAKE_CASE` for constants.
- **Documentation:** All public functions and classes must have docstrings or doc comments.
- **No dead code:** Remove commented-out code rather than leaving it in place.
- **No secrets:** Never commit credentials, API keys, or tokens.

## Code Review Priorities

When reviewing pull requests, focus on the following areas in order of importance:

1. **Correctness** — Does the code do what it claims to do? Are edge cases handled?
2. **Security** — Are all external inputs validated? Are there any exposed secrets or credentials?
3. **Error handling** — Errors must be handled explicitly; do not silently swallow exceptions.
4. **Readability** — Is the code easy to understand? Are naming conventions followed?
5. **Test coverage** — Are new code paths covered by tests?
6. **Documentation** — Are public APIs documented with docstrings or doc comments?

## Review Boundaries

- Only address code and files included in the pull request.
- Do **not** suggest large refactors unless the PR explicitly asks for them.
- Do **not** flag pre-existing issues that are unrelated to the PR changes.
- Keep review comments concise and actionable.

## Commit Message Convention

Commit messages must follow the format:

```
<type>: <short description>
```

Types: `feat`, `fix`, `docs`, `refactor`, `test`, `chore`
