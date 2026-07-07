# MCP Demo Runbook (Parent Repo)

Purpose: validate both MCP servers from one VS Code workspace.

## Preconditions

1. `../LoadMaster` exists and is configured
2. `../WhatsUp_Gold` exists and is configured
3. `.vscode/mcp.json` in this repo points to both servers

## Validation Prompts

LoadMaster:
1. `Test the LoadMaster connection and show connection info.`
2. `Get parameter hamode.`

WhatsUp Gold:
1. `List domains from the whatsup-gold-corpus MCP server.`
2. `Search API chunks for whoAmI token 10.0.0.40.`

## Manual Startup Checks

LoadMaster MCP:
```bash
cd ../LoadMaster/loadmaster-mcp && timeout 8s .venv/bin/python -m loadmaster_mcp.server
```

WhatsUp Gold MCP:
```bash
cd ../WhatsUp_Gold/mcp/server && timeout 8s npm run dev
```

Expected: both commands timeout with exit 124 while process remains healthy.
