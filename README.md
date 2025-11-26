# command-weekly-summary

A Claude Code slash command for generating weekly work summaries from git activity.

## Installation

```bash
# Clone to your preferred location
git clone git@github.com:claude-commands/command-weekly-summary.git <clone-path>/command-weekly-summary

# Symlink (use full path to cloned repo)
ln -s <clone-path>/command-weekly-summary/weekly-summary.md ~/.claude/commands/weekly-summary.md
```

## Usage

```text
/weekly-summary      # Current week (since Monday)
/weekly-summary 1    # Last week
/weekly-summary 2    # Two weeks ago
```

## What it does

1. Gathers commits from the specified week
2. Aggregates PRs merged and work completed
3. Calculates productivity metrics
4. Groups accomplishments by category and project
5. Generates status report ready for sharing

## Output Format

```markdown
# Weekly Summary

**Week of**: January 15 - 21, 2024

## Highlights

- Shipped user authentication feature (#123)
- Fixed critical payment processing bug (#456)
- Completed API rate limiting implementation

## By Category

### Features (8 commits)
- User authentication with JWT tokens
- Password reset flow

### Bug Fixes (5 commits)
- Payment processing edge case (#456)

## Metrics

| Metric | Value |
|--------|-------|
| Commits | 23 |
| PRs Merged | 4 |
| Lines Added | 1,245 |
| Files Changed | 34 |
```

## Features

- **Week navigation**: Current week, last week, or N weeks back
- **Multi-repo support**: Aggregates from multiple repos in parent dir
- **Category grouping**: Features, fixes, maintenance
- **Project grouping**: By repo or module
- **Metrics**: Commits, lines, PRs, files changed

## Use Cases

| Audience | Focus |
|----------|-------|
| Team standup | Highlights only |
| Manager 1:1 | Metrics + blockers |
| Status report | Full detail with PRs |

## Requirements

- Git repository with commits
- Claude Code with Sonnet model access

## Updates

```bash
cd <clone-path>/command-weekly-summary && git pull
```
