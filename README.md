📖 Organization Git ConventionsTo maintain a clean, readable, and highly automated development workflow, our organization follows strict naming conventions for repositories, branches, and commits.📦 Repository NamingRepository names should be easily recognizable, descriptive, and consistent across the organization.Format: lowercase-with-hyphens (kebab-case).Prefixes (Optional but recommended): Use prefixes if your organization has multiple microservices or distinct layers (e.g., api-, ui-, svc-, pkg-).Keep it concise: Avoid redundant words like project or app.Examples:✅ api-payment-gateway✅ ui-customer-dashboard❌ PaymentGatewayProject (PascalCase, redundant word)❌ user_service (snake_case)🌿 Branch NamingBranch names should immediately communicate their purpose and tie back to an issue tracker (like Jira or GitHub Issues) whenever possible.Format: <type>/<issue-id>-<short-description>Casing: kebab-case for the description.Branch TypesTypePurposeExamplefeatureDeveloping a new feature.feature/PROJ-123-add-authbugfixFixing an issue in standard development.bugfix/PROJ-456-login-crashhotfixUrgent fix directly on the production branch.hotfix/PROJ-789-memory-leakreleasePreparing a new release (version bumping).release/v1.2.0choreMaintenance, dependencies, or tooling updates.chore/update-webpack-configNote: If an issue ID is not applicable, simply omit it: feature/user-profile-page.💬 Commit MessagesWe strictly follow the Conventional Commits specification. This allows us to auto-generate changelogs and automate semantic versioning.Format:Plaintext<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
Rules:Limit the subject line to 50 characters.Use the imperative mood in the subject line (e.g., "add", not "added" or "adds").Do not end the subject line with a period.Wrap the body at 72 characters and use it to explain what and why (vs. how).Commit TypesTypePurposefeatA new feature (correlates with MINOR in Semantic Versioning).fixA bug fix (correlates with PATCH in Semantic Versioning).docsDocumentation only changes.styleChanges that do not affect the meaning of the code (formatting, etc).refactorA code change that neither fixes a bug nor adds a feature.testAdding missing tests or correcting existing tests.choreChanges to the build process, auxiliary tools, or libraries.ExamplesStandard Feature Commit:Plaintextfeat(auth): implement JWT token refresh mechanism

Added a silent refresh endpoint to prevent users from being
logged out abruptly after 15 minutes.

Closes #124
Standard Bug Fix:Plaintextfix(ui): resolve button alignment on mobile view
Breaking Change:Plaintextfeat(api): overhaul payment processing logic

BREAKING CHANGE: The /charge endpoint now requires a `currency` field.
