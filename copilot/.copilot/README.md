# GitHub Copilot CLI Configurations

This directory contains specialized configurations and custom tools for the GitHub Copilot CLI.

## Structure
- `.copilot/skills/` - Custom agent skills. Each skill is a folder containing a `SKILL.md` file with YAML frontmatter.
- `.copilot/agents/`: Custom agent profiles for specialized tasks.
  - `java-modernizer.agent.md`: Expert Java application modernization specialist.

## Agent Format

Each custom agent is defined by a Markdown file with an `.agent.md` extension containing:

- **YAML frontmatter**: Agent metadata including `name`, `description`, `tools`, and optional `model`
- **Markdown body**: Detailed instructions for the agent's behavior and expertise

### Usage

Agents can be invoked in several ways:

- **Slash command**: `/agent` in interactive mode
- **Explicit instruction**: "Use the java-modernizer agent on..."
- **By inference**: Copilot automatically selects based on your prompt
- **Programmatically**: `copilot --agent java-modernizer --prompt "..."`

## Adding New Agents

To create a new agent:

1. Create a new `.agent.md` file in `.copilot/agents/`
2. Add YAML frontmatter with `name` and `description` (required)
3. Specify tool access with `tools` array (optional, defaults to all tools)
4. Write detailed instructions in the Markdown body

Restart the Copilot CLI to load new agents.