# Skills

Small skills for coding agents.

## do-less

Complete the task with the least complexity needed.

[`do-less`](do-less/SKILL.md) asks the agent to:

- Reuse code and patterns that the project already has.
- Omit features, options, and layers that the task does not need.
- Finish all required changes, including affected callers and tests.
- Keep validation, error handling, security, and accessibility.
- Use focused checks for the behavior that can break.
- Write short, direct replies that state the result, checks, and known risks.

The skill is one Markdown file. It has no hooks, runtime scripts, dependencies, or persistent modes. It applies to the current task and follows the user's requirements and project rules.

## Install

### With the skills CLI

This method requires Node.js, npm, and Git. These examples use a POSIX shell.

The CLI sends usage telemetry by default. Each command below sets `DISABLE_TELEMETRY=1`. This disables usage telemetry and security-audit requests. See the [CLI telemetry documentation](https://github.com/vercel-labs/skills/blob/main/docs/troubleshooting.md#telemetry).

Run this command from your project's root folder:

```sh
DISABLE_TELEMETRY=1 npx skills add spa5k/skills --skill do-less
```

Follow the prompts to select your agent and install method. The default scope is the current project.

To install for all your projects, use `--global`:

```sh
DISABLE_TELEMETRY=1 npx skills add spa5k/skills --skill do-less --global
```

Use `--agent codex` to select Codex. Use `--agent claude-code` to select Claude Code. See the [skills CLI reference](https://github.com/vercel-labs/skills/blob/main/docs/commands.md#skills-add) for other options.

### Manual install

These commands use a POSIX shell and `curl`. They install the skill for your user account. Choose the command block for your agent.

**Codex**

```sh
mkdir -p "$HOME/.agents/skills/do-less"
curl --fail --location https://raw.githubusercontent.com/spa5k/skills/main/do-less/SKILL.md \
  --output "$HOME/.agents/skills/do-less/SKILL.md"
```

**Claude Code**

```sh
mkdir -p "$HOME/.claude/skills/do-less"
curl --fail --location https://raw.githubusercontent.com/spa5k/skills/main/do-less/SKILL.md \
  --output "$HOME/.claude/skills/do-less/SKILL.md"
```

For a project install, use `.agents/skills/do-less/` for Codex. Use `.claude/skills/do-less/` for Claude Code. Put `SKILL.md` in that folder at the project root.

The install paths follow the [Codex skill guide](https://developers.openai.com/codex/skills#where-to-save-skills) and the [Claude Code skill guide](https://code.claude.com/docs/en/skills#choose-where-skills-load).

## Use

In Codex CLI or the IDE extension, include the skill in your prompt:

```text
$do-less Fix the login error. Keep the existing API.
```

In Claude Code, use:

```text
/do-less Fix the login error. Keep the existing API.
```

In an app with a skill menu, select `do-less` before you enter the task. Your agent can also select the skill when you ask it to simplify code or avoid overengineering.

If the skill does not appear, start a new session. Check that the file is named `SKILL.md` and is inside a `do-less` folder in a supported skill path.

## Update or remove

For a project install made with the skills CLI, run:

```sh
DISABLE_TELEMETRY=1 npx skills update do-less --project
```

To remove that install, run:

```sh
DISABLE_TELEMETRY=1 npx skills remove do-less
```

Use `--global` instead of `--project` to update a user install. Add `--global` to the remove command to remove a user install.

For a manual install, run the download command again to update the file. Delete the installed `do-less` folder to remove it. Start a new session after removal to clear instructions that the agent already loaded.

## Design

The skill keeps the useful aim of Ponytail: finish the whole task with a simple solution. It uses a short set of instructions in place of a hook system. It has no levels or session-wide mode.

Read the [full skill](do-less/SKILL.md) before you install it. Its communication rules use ASD-STE100 Simplified Technical English. Code names and commands stay exact.
