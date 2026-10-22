# Skills

## do-less

Complete the task with the least complexity needed.

[`do-less`](do-less/SKILL.md) favors existing code and simple structure. It covers the full change and its checks. It keeps safety checks. Replies stay short and direct.

The skill is one Markdown file. It has no hooks or runtime scripts.

## Install

Requires Node.js, npm, and Git. This example uses a POSIX shell.

Run this command from your project's root folder:

```sh
DISABLE_TELEMETRY=1 npx skills add spa5k/skills --skill do-less
```

Select your agent when prompted. Add `--global` to install for all your projects.

`DISABLE_TELEMETRY=1` disables the CLI's telemetry and security-audit requests. [Details](https://github.com/vercel-labs/skills/blob/main/docs/troubleshooting.md#telemetry).

## Use

**Codex CLI or IDE**

```text
$do-less Fix the login error. Keep the existing API.
```

**Claude Code**

```text
/do-less Fix the login error. Keep the existing API.
```

If the skill does not appear, start a new session.
