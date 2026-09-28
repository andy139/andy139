# Andy Tran

Software engineer in San Francisco. I founded The Yew Company and build it as the sole engineer: [Yew Business](https://biz.yew.cash), card payments set up at your counter plus the software behind them, and Yew Pay, the payment engine underneath. The terminal, the web app, the ledger, the deploys, and the AI tools around them. Before that: backend at Red Bull Media House, then the pricing engine at Supplyframe, a Siemens company.

## Talk to my AI

My site runs a read-only MCP server. Add it to your agent and ask about my work.

```sh
# Claude Code
claude mcp add --transport http andy-tran https://www.andytran.tech/api/mcp

# Codex CLI
codex mcp add andy-tran -- npx -y mcp-remote https://www.andytran.tech/api/mcp
```

Claude.ai or Claude Desktop: Settings > Connectors > Add custom connector > `https://www.andytran.tech/api/mcp`

Cursor and anything else that takes an `mcpServers` block:

```json
{ "mcpServers": { "andy-tran": { "url": "https://www.andytran.tech/api/mcp" } } }
```

Tools: `about`, `get_resume`, `get_projects`, `get_contact`, `search`. Full guide at [andytran.tech/AGENTS.md](https://www.andytran.tech/AGENTS.md).

## Elsewhere

[andytran.tech](https://www.andytran.tech) · [LinkedIn](https://www.linkedin.com/in/andy139/) · andytran1140@gmail.com
