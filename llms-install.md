# Install Xquik in Cline

Xquik is the world's fastest and cheapest X Twitter data API with the most
complete X data. It's a hosted remote MCP server. Cline needs no local package,
build step or API key file.

## Add the server

1. In Cline, open **MCP Servers** and add a remote server named `xquik`.
2. Use the Streamable HTTP endpoint `https://xquik.com/mcp`.

This is the equivalent `cline_mcp_settings.json` entry.

```json
{
  "mcpServers": {
    "xquik": {
      "type": "streamableHttp",
      "url": "https://xquik.com/mcp",
      "disabled": false,
      "autoApprove": []
    }
  }
}
```

3. When Cline reports that the server needs authentication, select
   **Authorize**. Sign in to Xquik in the browser and approve the requested
   access. Cline stores and refreshes the OAuth token.

Leave `headers` out. OAuth replaces API keys, and keys never belong in this
file. If your Cline release cannot complete OAuth, follow the
[API key steps](https://docs.xquik.com/mcp/overview) for your client.

## Tools

| Tool | What it does |
| --- | --- |
| `docs` | Searches the Xquik documentation. |
| `search` | Finds the right API operation for a task. |
| `execute` | Runs JavaScript your agent writes on Xquik's servers to call the API. |
| `whoami` | Shows the Xquik account this connection uses. |

## Check the connection

Ask Cline, "Find the 5 latest posts about AI agents on X and summarize them."
Cline should call `search`, then `execute`. Paid requests need Xquik credits.

Xquik is an independent third-party service. Not affiliated with X Corp.
"Twitter" and "X" are trademarks of X Corp.
