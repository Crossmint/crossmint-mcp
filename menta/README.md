# Menta by Crossmint

Remote MCP server that buys, orders, books, returns and cancels things at online stores for you, through Crossmint checkouts. You approve every spending limit yourself; the assistant never can. Card numbers, codes and passwords never go through the chat. Sign in with your Menta account (OAuth). No API key to paste.

**Server URL:** `https://menta.crossmint.com/mcp` (Streamable HTTP, OAuth)

- Website: https://menta.crossmint.com
- Help: https://menta.crossmint.com/help
- Privacy policy: https://menta.crossmint.com/privacy
- Terms: https://menta.crossmint.com/terms
- Support: agents@crossmint.com

## Network and credentials

The plugin connects only to `https://menta.crossmint.com/mcp`. It needs no API key or environment variable: you sign in to Menta in the browser the first time the server connects.

## Install

**Grok:** this folder is the plugin (`.grok-plugin/plugin.json` and `.mcp.json`).

**Claude:** Settings > Connectors > Add custom connector > paste `https://menta.crossmint.com/mcp`. Claude Code: `claude mcp add --transport http menta https://menta.crossmint.com/mcp`

**ChatGPT:** install Menta from the ChatGPT plugin directory.

**Cursor / VS Code / other MCP clients:**
```json
{"mcpServers":{"menta":{"url":"https://menta.crossmint.com/mcp"}}}
```
