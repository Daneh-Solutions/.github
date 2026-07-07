# 📖 Organization Git Conventions

To maintain a clean, readable, and highly automated development workflow, our organization follows strict naming conventions for repositories, branches, and commits. 

## 📦 Repository Naming

Repository names should be easily recognizable, descriptive, and consistent across the organization.

* **Format:** `lowercase-with-hyphens` (kebab-case).
* **Prefixes:** Use prefixes if your organization has multiple microservices or distinct layers (e.g., `api-`, `ui-`, `svc-`, `pkg-`).
* **Keep it concise:** Avoid redundant words like `project` or `app`.

**Examples:**
* ✅ `api-payment-gateway`
* ✅ `ui-customer-dashboard`
* ❌ `PaymentGatewayProject` *(PascalCase, redundant word)*
* ❌ `user_service` *(snake_case)*

---

## 🌿 Branch Naming

Branch names should immediately communicate their purpose and tie back to an issue tracker (like Jira or GitHub Issues).

* **Format:** `<type>/<issue-id>-<short-description>`

### Branch Types

| Type | Purpose | Example |
| :--- | :--- | :--- |
| **feature** | Developing a new feature. | `feature/PROJ-123-add-auth` |
| **bugfix** | Fixing an issue in standard development. | `bugfix/PROJ-456-login-crash` |
| **hotfix** | Urgent fix directly on the production branch. | `hotfix/PROJ-789-memory-leak` |
| **release** | Preparing a new release (version bumping). | `release/v1.2.0` |
| **chore** | Maintenance, dependencies, or tooling updates. | `chore/update-webpack-config` |

> **Note:** If an issue ID is not applicable, simply omit it: `feature/user-profile-page`.

---

## 💬 Commit Messages

We strictly follow the [Conventional Commits](https://www.conventionalcommits.org/) specification. This allows us to auto-generate changelogs and automate semantic versioning.

* **Format:** 
  ```text
  <type>[optional scope]: <description>

  [optional body]

  [optional footer(s)]
  ```
* **Rules:**
  * Limit the subject line to **50 characters**.
  * Use the **imperative mood** in the subject line (e.g., "add", not "added" or "adds").
  * Do not end the subject line with a period.
  * Wrap the body at **72 characters** and use it to explain *what* and *why* (vs. *how*).

### Commit Types

| Type | Purpose |
| :--- | :--- |
| **feat** | A new feature |
| **fix** | A bug fix |
| **docs** | Documentation only changes |
| **style** | Changes that do not affect the meaning of the code (formatting, etc) |
| **refactor** | A code change that neither fixes a bug nor adds a feature |
| **test** | Adding missing tests or correcting existing tests |
| **chore** | Changes to the build process, auxiliary tools, or libraries |

### Examples

**Standard Feature Commit:**
```text
feat(auth): implement JWT token refresh mechanism

Added a silent refresh endpoint to prevent users from being
logged out abruptly after 15 minutes.

Closes #124
```

**Standard Bug Fix:**
```text
fix(ui): resolve button alignment on mobile view
```
