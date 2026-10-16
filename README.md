# Crossmint MCP

Remote MCP server to manage your Crossmint organizations, projects, environments and API keys from AI assistants. Sign in with your Crossmint account (email + one-time code, OAuth). No API key to paste.

**Server URL:** `https://mcp.crossmint.com/mcp` (Streamable HTTP)

- Docs: https://docs.crossmint.com/mcp-server/connect
- Privacy policy: https://www.crossmint.com/legal/privacy-policy
- Terms: https://drive.google.com/file/d/1gRiomgH2J_IYz3Qtsfvo3qR_NryrIxHd/view

## Tools
whoami, env_select, orgs_list, orgs_current, orgs_select, projects_list, projects_create, projects_details, keys_list, keys_create, keys_edit, keys_delete

## Install

**Cursor:** [Add to Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=crossmint&config=eyJ1cmwiOiJodHRwczovL21jcC5jcm9zc21pbnQuY29tL21jcCJ9) or add to `~/.cursor/mcp.json`:
```json
{"mcpServers":{"crossmint":{"url":"https://mcp.crossmint.com/mcp"}}}
```

**Claude:** Settings > Connectors > Add custom connector > paste `https://mcp.crossmint.com/mcp`. Claude Code: `claude mcp add --transport http crossmint https://mcp.crossmint.com/mcp`

**ChatGPT:** Settings > Apps > Advanced > Developer mode > Create app > paste `https://mcp.crossmint.com/mcp`, auth OAuth.

**Gemini CLI:** `gemini extensions install https://github.com/Crossmint/crossmint-mcp` or `gemini mcp add --transport http crossmint https://mcp.crossmint.com/mcp`

**VS Code:** Command Palette > MCP: Add Server > HTTP > `https://mcp.crossmint.com/mcp`, or `.vscode/mcp.json`:
```json
{"servers":{"crossmint":{"type":"http","url":"https://mcp.crossmint.com/mcp"}}}
```

## License
MIT
