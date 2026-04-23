# OpenCode Configurations

This directory contains specialized configurations and custom tools for the `opencode` CLI.

- `opencode.json` - Main configuration (models, tools, permissions, MCP servers).
- `tui.json` - TUI-specific settings (themes, keybinds, scroll behavior).
- `AGENTS.md` - Project-specific rules and instructions for the AI agent.
- `skills/` - Custom agent skills. Each skill is a folder containing a `SKILL.md` file with YAML frontmatter.
- `agents/` - Custom agents for specialized tasks.
  - `java-modernizer.md`: Expert Java application modernization specialist.

## Skill Format

Each skill must follow this structure:

```
.opencode/skills/<skill-name>/SKILL.md
```

The `SKILL.md` file must start with YAML frontmatter containing:
- `name` (required) - lowercase alphanumeric with hyphens
- `description` (required) - 1-1024 characters
- `license` (optional)
- `compatibility` (optional)
- `metadata` (optional)
