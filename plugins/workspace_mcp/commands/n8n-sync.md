---
description: Sync workflows from remote n8n instance to local project
argument-hint: <project_name>
allowed-tools: ["mcp__plugin_workspace_mcp__sync_workflows", "mcp__plugin_workspace_mcp__list_workflows"]
---

# n8n Sync Workflows

Sync all workflows from a remote n8n instance to the local project directory.

## Instructions

Project name: $ARGUMENTS

1. If no project name provided, ask the user which n8n project to sync

2. Call `mcp__plugin_workspace_mcp__sync_workflows` with the project name

3. After sync completes:
   - Report how many workflows were synced
   - List the workflow names
   - Mention any errors encountered

4. Optionally call `mcp__plugin_workspace_mcp__list_workflows` to show the current state

## Requirements

The project must have:
- `N8N_API_KEY` configured in envSettings
- `externalUrl` set in project-info.yml

If sync fails due to missing configuration, guide the user to set these values.

