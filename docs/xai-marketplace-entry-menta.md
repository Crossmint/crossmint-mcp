# xAI Plugin Marketplace Entry for Menta by Crossmint

The entry for the `plugins` array in `.grok-plugin/marketplace.json` of `xai-org/plugin-marketplace`. Menta lives in the `menta/` folder of this repo, so the entry sets `source.path`. Pin `sha` to the full commit on `main` that contains `menta/` (`git ls-remote https://github.com/Crossmint/crossmint-mcp.git HEAD` after merge).

```json
{
  "name": "menta",
  "description": "Menta by Crossmint buys, orders, books, returns and cancels things at online stores for you, through Crossmint checkouts. You approve every spending limit yourself; the assistant never can. Sign in with your Menta account.",
  "category": "productivity",
  "source": {
    "source": "url",
    "url": "https://github.com/Crossmint/crossmint-mcp.git",
    "sha": "<full 40-char commit sha on main>",
    "path": "menta"
  },
  "homepage": "https://menta.crossmint.com",
  "keywords": ["menta", "menta by crossmint", "menta crossmint"],
  "domains": ["menta.crossmint.com"]
}
```

## Plugin components

- **MCP server:** remote Streamable HTTP at `https://menta.crossmint.com/mcp` (`menta/.mcp.json`)
- **Authentication:** OAuth with the user's Menta account; no API key
- **Logo:** `menta/assets/logo.png` (512×512)
- **License:** MIT (this repo)
