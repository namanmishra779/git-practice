# Git Guidelines

## 1. Branching Model

- `main` is the protected production branch.
- Never commit directly to `main`.
- Create a separate branch for every feature, bug fix, or documentation change.
- Keep branches short-lived whenever possible.

## 2. Branch Naming

Use descriptive names:

- `feature/<name>`
- `bugfix/<name>`
- `fix/<name>`
- `docs/<name>`

Example:

`feature/login-api`

## 3. Commit Style

Use short and meaningful commit messages.

Good examples:

- `Add login validation`
- `Fix authentication timeout`
- `Update deployment documentation`

Avoid vague messages such as:

- `changes`
- `update`
- `stuff`

## 4. Pull Request Rules

- All changes to `main` must go through a Pull Request.
- CI checks must pass before merging.
- PRs should clearly describe the change.
- Review the changes before merging when another reviewer is available.
- Prefer Squash and Merge for small feature branches.

## 5. Protected Branches

The `main` branch is protected.

Direct pushes are not allowed.

Changes must enter `main` through a Pull Request.

## 6. Secrets Policy

Never commit passwords, API keys, access tokens, private keys, or other secrets.

Use GitHub Actions Secrets, environment variables, or an approved secret-management system.

If a secret is accidentally committed, immediately revoke or rotate it.

## 7. General Rules

- Pull the latest `main` before starting new work.
- Keep commits focused.
- Test changes before creating a PR.
- Do not force-push shared branches.
- Never rewrite the history of `main`.
