# claude-rules

Magnus Pladsen kit: personal global Claude Code rules, checked out at `~/.claude/rules/` as a
submodule of the [dotfiles](https://github.com/MagnusPladsen/dotfiles) repo. Companion to
[claude-skills](https://github.com/MagnusPladsen/claude-skills).

Frontmatter uses `description` / `globs` / `alwaysApply`, so the same files also work as
Continue (`~/.continue/rules`) and Crush (`~/.config/crush/rules`) rules via symlinks.

## Install

### Easiest: paste this into Claude Code

```text
Install my global Claude Code rules from the public GitHub repo MagnusPladsen/claude-rules into ~/.claude/rules.

1. If ~/.claude/rules is already a git repo or a submodule of my dotfiles repo (~/.dotfiles, used as `git --git-dir=$HOME/.dotfiles --work-tree=$HOME`), just pull or run `submodule update --init .claude/rules` and stop there.
2. If ~/.claude/rules does not exist, clone https://github.com/MagnusPladsen/claude-rules.git there.
3. If it exists with other content, don't overwrite anything: back it up to ~/.claude/rules.bak-<timestamp>, clone https://github.com/MagnusPladsen/claude-rules.git to a temp dir, move its .git into ~/.claude/rules, then run `git status`. List any tracked files that differ from what was already on disk and ask me before running `git checkout -- .` to take the repo's version.
4. Never push, and never delete the backup.
5. When done, list the rules now in ~/.claude/rules and tell me to start a new session so they load.
```

### Manual

```bash
# Fresh machine with the dotfiles repo
dotfiles submodule update --init .claude/rules

# Standalone, when ~/.claude/rules does not exist yet
git clone https://github.com/MagnusPladsen/claude-rules.git ~/.claude/rules
```

Update later with `git -C ~/.claude/rules pull`. Rules load at session start.

## Shared

| Rule | Purpose |
|------|---------|
| `code-quality` | Core code quality standards |
| `minimal-diff` | Only change what was requested |
| `no-phantom-code` | No commented-out code, dead paths or deprecated remnants |
| `reusable-code` | Prefer reuse over duplication |
| `naming-conventions` | Consistent naming across the codebase |
| `security` | No secrets in code, input sanitization, auth patterns |
| `logging` | Structured logging: levels, format, what to log |
| `database` | Naming, migrations, indexes, safety |
| `dependency-management` | Be intentional about adding dependencies |
| `design-consistency` | Spacing, typography, colors, radii, icons |
| `testing-conventions` | Testing standards |
| `commit-conventions` | Commit through the `/commit` skill |
| `pr-conventions` | Pull request standards |
| `no-auto-push` | Never push unless asked |
| `plan-refinement` | Plan quality in plan mode |
| `dotfiles-docs` | Keep the dotfiles README in sync |

## Integrations

| Rule | Purpose |
|------|---------|
| `github` | `gh` CLI conventions |
| `azure-devops` | `az` CLI conventions |
| `bitbucket` | Bitbucket PR flow without a CLI |
| `jira` | Jira via the Atlassian MCP server |

## React / TypeScript

| Rule | Purpose |
|------|---------|
| `typescript` | TypeScript conventions |
| `components` | Component structure and naming |
| `accessibility` | Accessibility for interactive UI |
| `api-integration` | API client patterns |
| `internationalization` | i18n for user-facing text |
| `no-hardcoded-colors` | Theme tokens, no hex literals |
| `responsive-web-ui` | Mobile-first responsive layout |

## .NET / C#

| Rule | Purpose |
|------|---------|
| `csharp` | C# style and conventions |
| `clean-architecture` | Layer boundaries |
| `cqrs-mediatr` | CQRS with MediatR |
| `domain-models` | Domain model design |
| `persistence-entities` | EF Core entity conventions |
| `repository-query-pattern` | Repository (write) vs query (read) split |
| `error-handling` | Result pattern |
