# GitHub

A collection of GitHub-related configurations, scripts, and utilities.

## Contents

| File | Description |
|------|-------------|
| `main-branch-ruleset.json` | Branch protection ruleset for the `main` branch — enforces PRs, linear history, signed commits, and deletion protection |
| `dev-branch-ruleset.json` | Branch protection ruleset for the `dev` branch — allows direct pushes, no signatures or PR reviews required |

## Branch Rulesets

These files can be applied to any GitHub repository via the GitHub API or the repository settings UI.

### `main-branch-ruleset.json`

- **Deletion protection** — prevents the branch from being deleted
- **No force pushes** — requires fast-forward merges only (linear history)
- **Required linear history** — no merge commits allowed
- **Required signatures** — commits must be signed
- **Pull request reviews** — 1 approving review required, stale reviews dismissed on push, last push must be approved, all review threads must be resolved before merge

### `dev-branch-ruleset.json`

- **Deletion protection** — prevents the branch from being deleted
- **No force pushes** — force pushes are blocked
- Direct pushes allowed — no PR or review requirements
- No signature enforcement
