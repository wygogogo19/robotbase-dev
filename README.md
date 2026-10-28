# RobotBase Dev MCP

Read-only MCP server for developer ecosystem trends plus the shared RobotBase web toolbox.

- Endpoint: `https://dev.robotbase.cc/mcp`
- Tools: **18** — `dev_trending` (GitHub / Hugging Face / npm / PyPI / Hacker News) + all 17 web tools.
- Transport: Streamable HTTP, MCP protocol `2025-06-18`.
- No API keys. Free daily web allowance per IP, then x402 USDC credits.
- Version: `0.32.2`.

This is a thin distribution repository. The implementation, tests and full documentation live in
[`wygogogo19/robotbase-mcp`](https://github.com/wygogogo19/robotbase-mcp).

## Connect

Claude Code:

```bash
claude mcp add --transport http robotbase-dev https://dev.robotbase.cc/mcp
```

Any Streamable HTTP MCP client:

```json
{
  "mcpServers": {
    "robotbase-dev": {
      "type": "http",
      "url": "https://dev.robotbase.cc/mcp"
    }
  }
}
```

## Notes

- Read-only: no writes, no accounts, no API keys.
- `dev_trending` aggregates public signals with attribution and fallback.
- Web tools share the same 17-tool surface as the Web3 and Content editions.
- Paid calls settle in USDC on Base or Solana over x402; there is no subscription.
