# Coding Standards

This document defines the coding style and conventions for this repository.

---

## General Principles

- **Readability first** — Write code for humans to read, not just machines to execute.
- **Consistency** — Follow the established patterns in the existing codebase.
- **Minimal footprint** — Only change what is necessary; avoid unrelated edits.
- **No dead code** — Remove commented-out code instead of leaving it in place.

---

## Formatting

| Setting | Value |
|---------|-------|
| Indentation (Python, C, C++) | 4 spaces |
| Indentation (YAML, JSON, HTML) | 2 spaces |
| Max line length (code) | 100 characters |
| Line endings | LF (`\n`) |
| Trailing whitespace | Not allowed |
| Final newline | Required |

---

## Naming Conventions

| Context | Convention | Example |
|---------|------------|---------|
| Files (docs) | `kebab-case` | `coding-standards.md` |
| Files (Python) | `snake_case` | `user_service.py` |
| Files (C/C++) | `snake_case` or `PascalCase` | `user_service.cpp` |
| Variables | `snake_case` (Python), `camelCase` (JS) | `user_id`, `userId` |
| Constants | `UPPER_SNAKE_CASE` | `MAX_RETRY_COUNT` |
| Classes | `PascalCase` | `UserService` |
| Functions/Methods | `snake_case` (Python), `camelCase` (JS) | `get_user()`, `getUser()` |

---

## Documentation

- Public functions and classes **must** have docstrings or doc comments.
- Use inline comments sparingly — prefer self-documenting code.
- Keep comments up-to-date with the code they describe.

---

## Error Handling

- Always handle errors explicitly; do not silently swallow exceptions.
- Provide meaningful error messages that help diagnose the problem.
- Log errors at the appropriate level.

---

## Dependencies

- Prefer standard library solutions before adding third-party dependencies.
- Document any new dependency and the reason it was added.
- Pin dependency versions in lock files for reproducible builds.

---

## Security

- Never commit secrets, credentials, API keys, or tokens.
- Validate all external inputs.
- Follow the principle of least privilege.

---

## Language-Specific Standards

Detailed, language-specific coding standards are maintained in separate documents:

- **Python** — [`python-coding-standards.md`](python-coding-standards.md)
- **C/C++** — [`cpp-coding-standards.md`](cpp-coding-standards.md)
