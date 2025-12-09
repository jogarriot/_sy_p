# workspace-mcp-server

Workspace management plugin for Vibespace workspaces - projects, integrations, mini apps, and n8n workflows.

## MCP Tools

This plugin provides the following MCP tools via the `workspace-mcp` server:

| Tool | Description |
|------|-------------|
| `list_workflows` | List all n8n workflows in a project |
| `get_workflow` | Get detailed workflow JSON by ID or name |
| `sync_workflows` | Pull workflows from remote n8n instance |
| `push_workflow` | Push local workflow changes to n8n |

## Commands

| Command | Description |
|---------|-------------|
| `/n8n-sync` | Sync all workflows from remote n8n instance |
| `/n8n-push` | Push a specific workflow to remote |
| `/n8n-list` | List all workflows with summary info |

## Agents

| Agent | Description |
|-------|-------------|
| `workflow-analyzer` | Analyze workflow structure and suggest improvements |
| `workflow-builder` | Interactive workflow creation assistant |

## Requirements

- n8n project with `N8N_API_KEY` and `externalUrl` configured in project-info.yml
- Workflows stored in `{project}/workflows/` directory

## Usage

1. Create an n8n project or sync an existing one
2. Use `/n8n-sync` to pull workflows from your n8n instance
3. Edit workflows locally as JSON files
4. Use `/n8n-push` to deploy changes

