# MCP Workspace (Parent Repo)

Purpose: hold cross-project documentation and shared VS Code MCP configuration for running both repositories together.

Projects referenced:
1. `../LoadMaster`
2. `../WhatsUp_Gold`

## What This Repo Contains

1. Parent-level runbook for dual MCP operation
2. Parent-level VS Code MCP config (`.vscode/mcp.json`)
3. Workspace guidance for Copilot/VS Code usage

## Expected Local Layout

```text
/home/chef/repos/
  LoadMaster/
  WhatsUp_Gold/
  MCP_Workspace/
```

## Quick Start

1. Open VS Code at `MCP_Workspace/`
2. Reload window (`Developer: Reload Window`)
3. Ensure both referenced repos exist one level up
4. Use Copilot Chat prompts from `MCP_DEMO_RUNBOOK.md`

## Notes

1. This is a meta-repo. It does not contain the full source of LoadMaster or WhatsUp_Gold.
2. Keep project-specific code/docs in their own repos.
