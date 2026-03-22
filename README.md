# tiktok-trends-mcp

[![TikTok Trends](https://img.shields.io/badge/TikTok%20Trends-010101?style=flat-square)](https://trendsmcp.ai/tiktok-trends)
[![MCP](https://img.shields.io/badge/MCP-compatible-blue?style=flat-square)](https://modelcontextprotocol.io)
[![Works with Claude](https://img.shields.io/badge/Claude-supported-orange?style=flat-square)](https://trendsmcp.ai/mcp-server-for-claude)
[![Works with Cursor](https://img.shields.io/badge/Cursor-supported-purple?style=flat-square)](https://trendsmcp.ai/mcp-server-for-cursor)

> **TikTok trend data for AI assistants**
> Spot TikTok trends before they go mainstream. Track hashtag volume growth, viral spikes, and platform-specific demand signals - all accessible from your AI in plain language.

**Full docs and live demo:** [https://trendsmcp.ai/tiktok-trends](https://trendsmcp.ai/tiktok-trends)

Part of **[Trends MCP](https://trendsmcp.ai)** -- the MCP server for live trend data across 12+ sources.
See the main repo: [https://github.com/trendsmcp/trends-mcp](https://github.com/trendsmcp/trends-mcp)

---

## Get started in 2 steps

**Step 1:** Get your free API key at **[trendsmcp.ai](https://trendsmcp.ai)**
100 requests/day, no credit card required.

**Step 2:** Add to your AI client (replace `YOUR_API_KEY`):

[**+ Add to Cursor (one click)**](cursor://anysphere.cursor-deeplink/mcp/install?name=trends-mcp&config=eyJ1cmwiOiAiaHR0cHM6Ly9hcGkudHJlbmRzbWNwLmFpL21jcCIsICJ0cmFuc3BvcnQiOiAiaHR0cCJ9)

**Cursor / Windsurf / Cline** &nbsp; (`~/.cursor/mcp.json` or equivalent)
```json
{
  "mcpServers": {
    "trends-mcp": {
      "url": "https://api.trendsmcp.ai/mcp",
      "transport": "http",
      "headers": { "Authorization": "Bearer YOUR_API_KEY" }
    }
  }
}
```

**VS Code / GitHub Copilot** &nbsp; (`.vscode/mcp.json`)
```json
{
  "servers": {
    "trends-mcp": {
      "type": "http",
      "url": "https://api.trendsmcp.ai/mcp",
      "headers": { "Authorization": "Bearer YOUR_API_KEY" }
    }
  }
}
```

**Claude Desktop** &nbsp; (`claude_desktop_config.json`)
```json
{
  "mcpServers": {
    "trends-mcp": {
      "url": "https://api.trendsmcp.ai/mcp",
      "transport": "http",
      "headers": { "Authorization": "Bearer YOUR_API_KEY" }
    }
  }
}
```

**Claude.ai** (browser) &nbsp; Settings -> Connectors -> Add custom connector:
```
https://api.trendsmcp.ai/mcp
```

---

## Example query

After connecting, ask your AI:
```
get_trends(keyword='booktok', source='tiktok', data_mode='weekly')
```

---

## Available tools

| Tool | What it does |
|------|-------------|
| `get_trends` | Time-series for a keyword on this source |
| `get_growth` | Growth % over 1W, 1M, 3M, 6M, 1Y periods |
| `get_top_trends` | What is trending right now on this source |
| `get_ranked_trends` | Top topics ranked by volume |

---

## FAQ

### What TikTok data does Trends MCP provide?

TikTok hashtag trend volume - normalized interest, growth rate, and historical time series. This reflects how frequently a hashtag appears and grows on the platform over time.

### How early can I detect a TikTok trend?

Trends MCP returns weekly and daily data. Daily data (last 30 days) lets you spot early-stage growth spikes before a hashtag reaches mainstream saturation.

### Can I compare TikTok trends against Google Search?

Yes. Query both sources in one call. TikTok often shows spikes 2-4 weeks before the same topic rises on Google Search, making cross-platform comparison a leading indicator strategy.

### Does this work for brand monitoring on TikTok?

Yes. Track a brand name or product hashtag over time to measure TikTok presence growth relative to competitors.

### Are TikTok hashtags case-sensitive?

No. The query is normalized before lookup. You can use 'booktok', 'BookTok', or '#booktok' - all return the same signal.

---

## All data sources

Trends MCP covers 12+ sources in one connection:
Google Search, YouTube, TikTok, Reddit, Amazon, Wikipedia,
News Sentiment, Web Traffic, App Downloads, Steam, npm, and more.

Browse all: [https://trendsmcp.ai/data-sources](https://trendsmcp.ai/data-sources)

---

## License

MIT &copy; [Trends MCP](https://trendsmcp.ai)