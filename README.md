# khao-pad-skills

Marketplace for Claude Code and Codex plugins focused on khao-pad based web development.

See the [Plugins Reference](https://code.claude.com/docs/en/plugins-reference) for general information on Claude Plugins.

## Design Philosophy

This marketplace prioritizes skill-based plugins for common khao-pad development guidance. The MCP server plugin is available for workflows that need browser or Storybook tool access.

## Available Plugins

| Plugin                     | Description                                           |
| -------------------------- | ----------------------------------------------------- |
| `khao-pad-dev-mcp-servers` | Recommended MCP servers for khao-pad based web dev    |
| `khao-pad-dev-skills`      | Khao-pad web development skills (UI components & CSS) |

## Installation

### Add the Marketplace

Claude Code:

```bash
claude plugin marketplace add https://github.com/Der-Reiskoch/khao-pad-skills
```

Codex:

```bash
codex plugin marketplace add Der-Reiskoch/khao-pad-skills --ref main
```

For local development:

```bash
codex plugin marketplace add /path/to/khao-pad-skills
```

### Install a Plugin

Claude Code:

```bash
claude plugin install khao-pad-dev-skills@khao-pad-skills --scope project
claude plugin install khao-pad-dev-mcp-servers@khao-pad-skills --scope project
```

Codex:

```bash
codex plugin add khao-pad-dev-skills@khao-pad-skills
```

Or install the MCP helpers when tool access is needed:

```bash
codex plugin add khao-pad-dev-mcp-servers@khao-pad-skills
```
