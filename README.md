# khao-pad-skills

Marketplace for Claude Code plugins focused on khao-pad based web development.

See the [Plugins Reference](https://code.claude.com/docs/en/plugins-reference) for general information on Claude Plugins.

## Available Plugins

| Plugin                     | Description                                           |
| -------------------------- | ----------------------------------------------------- |
| `khao-pad-dev-mcp-servers` | Recommended MCP servers for khao-pad based web dev    |
| `khao-pad-dev-skills`      | Khao-pad web development skills (UI components & CSS) |

## Installation

### Add the Marketplace

```bash
claude plugin marketplace add https://github.com/Der-Reiskoch/khao-pad-skills
```

### Install a Plugin

```bash
claude plugin install khao-pad-dev-skills@khao-pad-skills --scope project
claude plugin install khao-pad-dev-mcp-servers@khao-pad-skills --scope project
```
