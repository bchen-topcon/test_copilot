# Contributing Guidelines

Thank you for contributing to `test_copilot`! Please read this guide before opening issues or submitting pull requests.

---

## Reporting Issues

1. Search existing issues to avoid duplicates.
2. Use the appropriate issue template:
   - **Bug:** `.github/ISSUE_TEMPLATE/bug_report.md`
   - **Feature:** `.github/ISSUE_TEMPLATE/feature_request.md`
3. Provide as much detail as possible.

---

## Development Workflow

1. **Fork** the repository (external contributors) or create a **branch** (team members).
2. Branch naming convention:
   - `feature/<short-description>` — new functionality
   - `fix/<short-description>` — bug fixes
   - `docs/<short-description>` — documentation-only changes
   - `chore/<short-description>` — maintenance tasks
3. Make your changes following the conventions in `docs/coding-standards.md`.
4. **Commit** with descriptive messages (see commit format below).
5. **Push** your branch and open a **pull request** using the PR template.

---

## Commit Message Format

```
<type>: <short description (imperative, max 72 chars)>

[optional body — explain why, not what]
```

| Type | When to use |
|------|-------------|
| `feat` | Adding new functionality |
| `fix` | Fixing a bug |
| `docs` | Documentation changes only |
| `refactor` | Code restructuring without behavior change |
| `test` | Adding or updating tests |
| `chore` | Build process, dependency updates, etc. |

---

## Pull Request Guidelines

- Keep PRs **small and focused** — one concern per PR.
- Fill in **all sections** of the PR template.
- Link to the related issue (e.g., `Closes #42`).
- Ensure all checks pass before requesting review.

---

## Code Review

- Respond to review comments promptly.
- Mark conversations as resolved once addressed.
- Squash or clean up commits if asked by a reviewer.

---

## Code of Conduct

Be respectful and constructive. This is a collaborative environment.
