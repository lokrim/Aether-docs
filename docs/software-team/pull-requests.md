---
id: pull-requests
title: PR Rules & Git Branching
sidebar_position: 2
---

# Pull Request Rules & Guidelines

To maintain a clean and understandable codebase, we follow a structured workflow for branching and Pull Requests (PRs) in Project Aether.

## 1. Git Branching Strategy

Never push directly to the `main` branch. Always create a new branch for your work. Here is how we name our branches:

- **Features:** `feature/your-feature-name` (e.g., `feature/login-page`)
- **Bug Fixes:** `bugfix/issue-description` (e.g., `bugfix/fix-header-alignment`)
- **Documentation:** `docs/what-was-documented` (e.g., `docs/add-pr-rules`)
- **Chores/Maintenance:** `chore/dependency-updates` (e.g., `chore/update-react`)

### Creating a Branch
Before creating a branch, make sure you have the latest changes from `main`:
```bash
git checkout main
git pull origin main
git checkout -b feature/your-feature-name
```

## 2. Opening a Pull Request

When your code is ready to be reviewed:
1. Push your branch to GitHub.
2. Go to the repository on GitHub and click **Compare & pull request**.
3. Fill out the PR template describing your changes.

## 3. Linking PRs to existing Issues

To automatically close the associated issue when your PR is merged, use GitHub's **linking keywords** in the PR description (not the title).

Examples of keywords you can use:
- `Close #1`
- `Closes #1`
- `Closed #1`
- `Fix #1`
- `Fixes #1`
- `Fixed #1`
- `Resolve #1`
- `Resolves #1`
- `Resolved #1`

When the PR gets merged, GitHub will automatically mark the linked issue as completed.

## 4. Review Process
- Ensure all CI/CD checks pass.
- At least one team member must approve your Pull Request before it can be merged.
- Once approved, "Squash and merge" is typically preferred to keep the `main` Git history clean.
