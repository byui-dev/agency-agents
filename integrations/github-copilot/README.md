# GitHub Copilot Integration

The Agency works with GitHub Copilot out of the box. No conversion needed —
agents use the existing `.md` + YAML frontmatter format.

## Repository-Level Agents

All agents are available directly within this repository via `.github/agents/`.
When you open this repo in VS Code with GitHub Copilot, you can use any agent
immediately without any installation.

To regenerate `.github/agents/` after adding or modifying agents:

```bash
./scripts/convert.sh --tool github-copilot
```

## User-Wide Install

Install agents to your local GitHub Copilot agents directory so they are
available across all your projects:

```bash
# Copy all agents to your GitHub Copilot agents directories
./scripts/install.sh --tool copilot

# Or manually copy a category
cp engineering/*.md ~/.github/agents/
cp engineering/*.md ~/.copilot/agents/
```

## Activate an Agent

In any GitHub Copilot session, reference an agent by name:

```
Activate Frontend Developer and help me build a React component.
```

```
Use the Reality Checker agent to verify this feature is production-ready.
```

## Agent Directory

Agents are organized into divisions. See the [main README](../../README.md) for
the full current roster.
