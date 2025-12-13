---
description: List all n8n workflows in a project
argument-hint: <project_name>
allowed-tools: ["mcp__plugin_workspace_mcp__list_workflows"]
---

# n8n List Workflows

List all workflows in an n8n project with summary information.

## Instructions

Project name: $ARGUMENTS

1. If no project name provided, ask which n8n project to list

2. Call `mcp__plugin_workspace_mcp__list_workflows` with the project name

3. Present the results in a readable format:
   - Workflow name and ID
   - Active/inactive status
   - Node count
   - Last updated timestamp

4. If no workflows found, suggest:
   - Using `/n8n-sync` to pull workflows from remote
   - Creating a new workflow manually

## Output Format

Present as a table or list:

| Name | ID | Status | Nodes | Updated |
|------|-----|--------|-------|---------|
| Example Workflow | abc123 | Active | 5 | 2024-01-15 |

