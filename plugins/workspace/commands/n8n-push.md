---
description: Push a local workflow to the remote n8n instance
argument-hint: <project_name> <workflow_id>
allowed-tools: ["mcp__plugin_workspace__push_workflow", "mcp__plugin_workspace__get_workflow", "mcp__plugin_workspace__list_workflows"]
---

# n8n Push Workflow

Push a local workflow to the remote n8n instance.

## Instructions

Arguments: $ARGUMENTS

1. Parse arguments for project name and workflow ID
   - If missing, ask user to provide them
   - Can use `mcp__plugin_workspace__list_workflows` to help identify workflows

2. Before pushing, optionally show the user what will be pushed:
   - Use `mcp__plugin_workspace__get_workflow` to preview the workflow
   - Confirm with user if they want to proceed

3. Call `mcp__plugin_workspace__push_workflow` with project name and workflow ID

4. Report the result:
   - Success: show workflow name and updated timestamp
   - Failure: explain the error and suggest fixes

## Safety

- Pushing overwrites the remote workflow entirely
- Recommend syncing first to avoid losing remote changes
- If workflow doesn't exist remotely, it will be created

