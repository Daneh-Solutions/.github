# Daneh Solutions — Organization-Wide Standards

This repository contains organization-wide GitHub configuration, templates, and documentation for **Daneh Solutions**.

## 📚 Contents

| File / Folder | Purpose |
|---|---|
| [`CONTRIBUTING.md`](./CONTRIBUTING.md) | Git conventions: repository naming, branch naming, and commit messages |
| [`PULL_REQUEST_TEMPLATE.md`](./PULL_REQUEST_TEMPLATE.md) | Default pull request template |
| [`ISSUE_TEMPLATE/`](./ISSUE_TEMPLATE/) | Standard issue templates |

## Quick Reference

### Repository Naming
`lowercase-with-hyphens` — e.g. `api-payment-gateway`, `ui-customer-dashboard`

### Branch Naming
`<type>/<issue-id>-<short-description>` — e.g. `feature/PROJ-123-add-auth`, `bugfix/PROJ-456-login-crash`

### Commit Messages
Follow **[Conventional Commits](https://www.conventionalcommits.org/)**:
```
<type>[optional scope]: <description>
```
e.g. `feat(auth): implement JWT token refresh mechanism`

See [CONTRIBUTING.md](./CONTRIBUTING.md) for the full specification.