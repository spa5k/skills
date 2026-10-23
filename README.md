# Skills

## do-less

Complete the task with the least complexity needed.

[`do-less`](do-less/SKILL.md) favors existing code and simple structure. It covers the full change and its checks. It keeps safety checks. Replies stay short and direct.

The skill is one Markdown file. It has no hooks or runtime scripts.

## stay-in-scope

[`stay-in-scope`](stay-in-scope/SKILL.md) keeps work within the user's request. It asks before extra work. It allows the changes and checks needed to finish the task.

## Install

Requires Node.js, npm, and Git. These examples use a POSIX shell.

Run the command for the skill you want from your project's root folder.

**do-less**

```sh
DISABLE_TELEMETRY=1 npx skills add spa5k/skills --skill do-less
```

**stay-in-scope**

```sh
DISABLE_TELEMETRY=1 npx skills add spa5k/skills --skill stay-in-scope
```

Select your agent when prompted. Add `--global` to install for all your projects.

`DISABLE_TELEMETRY=1` disables the CLI's telemetry and security-audit requests. [Details](https://github.com/vercel-labs/skills/blob/main/docs/troubleshooting.md#telemetry).

## Use

Include the skill name in your task.

| Agent | do-less | stay-in-scope |
| --- | --- | --- |
| Codex CLI or IDE | `$do-less` | `$stay-in-scope` |
| Claude Code | `/do-less` | `/stay-in-scope` |

For example, in Codex:

```text
$stay-in-scope Fix the login error. Keep the existing API.
```

If the skill does not appear, start a new session.
