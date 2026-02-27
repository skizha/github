# GitHub

A collection of GitHub-related configurations, scripts, and utilities.

## Contents

| File | Description |
|------|-------------|
| `main-branch-ruleset.json` | Branch protection ruleset for the `main` branch — enforces PRs, linear history, signed commits, and deletion protection |

## Branch Ruleset

`main-branch-ruleset.json` can be applied to any GitHub repository via the GitHub API or the repository settings UI. It enforces the following on `main`:

- **Deletion protection** — prevents the branch from being deleted
- **No force pushes** — requires fast-forward merges only (linear history)
- **Required linear history** — no merge commits allowed
- **Required signatures** — commits must be signed
- **Pull request reviews** — 1 approving review required, stale reviews dismissed on push, last push must be approved, all review threads must be resolved before merge
