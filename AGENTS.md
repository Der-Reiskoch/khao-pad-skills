# Repository Guidelines

## Project Structure & Module Organization

This repository is a Claude Code plugin marketplace for khao-pad web development. The top-level `README.md` describes marketplace installation, while `plugins/` contains the distributable plugins.

- `plugins/khao-pad-dev-skills/` contains skill definitions.
- `plugins/khao-pad-dev-skills/skills/<skill-name>/SKILL.md` is the entry point for each skill.
- `plugins/khao-pad-dev-skills/skills/<skill-name>/resources/` stores supporting Markdown references.
- `plugins/khao-pad-dev-mcp-servers/.mcp.json` defines recommended MCP server configuration.
- Each plugin keeps metadata in `.claude-plugin/plugin.json`.

## Build, Test, and Development Commands

There is no application build pipeline in this repository. Validate changes with lightweight checks:

```bash
rtk rg --files
rtk git status --short
rtk cat plugins/khao-pad-dev-skills/.claude-plugin/plugin.json
```

Use the installation commands in `README.md` to test plugin consumption from a Claude Code project:

```bash
claude plugin marketplace add https://github.com/Der-Reiskoch/khao-pad-skills
claude plugin install khao-pad-dev-skills@khao-pad-skills --scope project
```

## Coding Style & Naming Conventions

Use Markdown for skill instructions and references. Keep `SKILL.md` front matter valid YAML with `name`, `description`, and `invocation`. Skill and plugin directory names use lowercase kebab-case, for example `khao-component-rendering`. JSON files use two-space indentation and stable key ordering.

Keep guidance direct and imperative. Reference concrete packages such as `@der-reiskoch/khao-ui` and `@der-reiskoch/khao-malet` rather than inventing generic alternatives.

## Testing Guidelines

No automated test framework is currently configured. Before opening a change, verify JSON validity, check Markdown rendering, and inspect all changed skill files. For MCP changes, confirm `.mcp.json` remains valid and that command arguments are explicit.

## Commit & Pull Request Guidelines

Current history uses short, imperative commit subjects such as `added plugins`. Keep commit messages concise and focused on one logical change.

Pull requests should include a brief summary, the affected plugin or skill paths, and manual validation steps. Link related issues when available. Include screenshots only when a change affects rendered documentation or plugin marketplace presentation.

## Agent-Specific Instructions

Run shell commands through `rtk` in this workspace. Do not overwrite an existing `AGENTS.md`; update it only when explicitly requested.
