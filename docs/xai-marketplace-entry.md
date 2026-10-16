# xAI Plugin Marketplace Entry for Crossmint

This document contains the exact JSON entry to add to the xAI plugin marketplace (`xai-org/plugin-marketplace`) for the Crossmint MCP plugin.

## Marketplace Entry

Add the following entry to the `plugins` array in `.grok-plugin/marketplace.json`:

```json
{
  "name": "crossmint",
  "description": "Manage Crossmint organizations, projects, environments and API keys from your AI assistant. Sign in with your Crossmint account to access the platform directly from Grok.",
  "category": "development",
  "source": {
    "source": "url",
    "url": "https://github.com/Crossmint/crossmint-mcp.git",
    "sha": "e0fc0a072ad4a6f2f4f6dce92f78d35f854155f4"
  },
  "homepage": "https://docs.crossmint.com/mcp-server/connect",
  "keywords": ["crossmint", "nft", "blockchain", "web3"],
  "domains": ["crossmint.com"]
}
```

## Validation Commands

After adding the entry to the marketplace, run these commands in the `xai-org/plugin-marketplace` repository:

```bash
# Regenerate the plugin component index
python3 scripts/generate-plugin-index.py

# Validate the catalog
python3 scripts/validate-catalog.py

# Check that the index is up to date (this is what CI runs)
python3 scripts/generate-plugin-index.py --check
```

## Pinned Commit Details

- **Repository**: https://github.com/Crossmint/crossmint-mcp
- **Commit SHA**: `e0fc0a072ad4a6f2f4f6dce92f78d35f854155f4`
- **Commit Message**: "Add xAI Grok plugin manifest and MCP config"
- **Verification**: 
  ```bash
  git ls-remote https://github.com/Crossmint/crossmint-mcp.git HEAD
  ```

## Plugin Components

The Crossmint plugin includes:

- **MCP Server**: Remote streamable HTTP server at `https://mcp.crossmint.com/mcp`
- **Authentication**: OAuth flow with Crossmint account (email + one-time code)
- **Logo**: `assets/logo-plate.svg` (square logo with background plate)
- **License**: MIT

## MCP Tools Provided

The Crossmint MCP server provides the following tools:

- `whoami` - Get current user information
- `env_select` - Select environment (staging/production)
- `orgs_list` - List organizations
- `orgs_current` - Get current organization
- `orgs_select` - Select organization
- `projects_list` - List projects
- `projects_create` - Create new project
- `projects_details` - Get project details
- `keys_list` - List API keys
- `keys_create` - Create API key
- `keys_edit` - Edit API key
- `keys_delete` - Delete API key

## Submission Checklist

- [x] Plugin manifest (`.grok-plugin/plugin.json`) added to source repo
- [x] MCP configuration (`.mcp.json`) added to source repo
- [x] JSON files validated successfully
- [x] Full 40-character commit SHA pinned
- [x] Repository is public and reachable
- [x] Homepage and clear description provided
- [x] Brand-scoped keywords and domains specified
- [x] License stated (MIT)
- [x] Category assigned (development)
