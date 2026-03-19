# Python Coding Standards

This document defines Python-specific coding conventions for this repository.
For general standards that apply to all languages, see [`coding-standards.md`](coding-standards.md).

---

## Style

- Follow **PEP 8** conventions.
- Use **4 spaces** for indentation (no tabs).
- Maximum line length is **100 characters**.
- Use `snake_case` for variables, functions, and module names.
- Use `PascalCase` for class names.
- Use `UPPER_SNAKE_CASE` for module-level constants.

---

## Documentation

- Every public function and class **must** have a docstring.
- Use Google-style or reStructuredText-style docstrings consistently within a file.

---

## Type Hints

- Use type hints for all function signatures where practical.
- Avoid using `Any` unless it is genuinely unavoidable.

---

## Error Handling

- Use specific exception types rather than bare `except:` or `except Exception:`.
- Provide informative error messages that help diagnose the problem.
- Do not silently swallow exceptions.

---

## Imports

- Order imports: standard library → third-party → local, each group separated by a blank line.
- Do not use wildcard imports (`from module import *`).

---

## Testing

- Unit tests live in files prefixed with `test_` (e.g., `test_calculator.py`).
- Run tests with: `python -m pytest` (or `python -m unittest discover` if pytest is unavailable).
- New functions and classes must have corresponding tests.
