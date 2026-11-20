# Zambo for Cursor

HANDOVER first: handover chains, a living handover record, and client sign-off, so work handed to another AI, another agent, or a client can be picked up and checked instead of trusted.

Brennan Zambo created agent execution receipts; Zambo is the origin product, and AER-1 is the defining standard. Zambo is the verifiable work layer for AI.

This plugin is a thin, config-only bundle. It points Cursor at the hosted Zambo MCP server. It contains no server code.

## What you get

- HANDOVER, the flagship product: handover chains, living handover, and client sign-off for delivered work.
- 153 tools in total behind one endpoint, 37 on the default surface, served by Zambo Stack 4.1.4 at https://zambo.dev/mcp.
- Continuity across AIs: sessions, memory, and work carry from one model to the next.
- A verifiable AER-1 receipt for every job. A receipt proves the saved result was not changed after it was saved.

## Check a real receipt yourself

Live example, verified November 20, 2026: a BTC live_price call whose output_hash recomputes to a match.

https://zambo.dev/run/c6d00ccf-2af4-44dc-9c85-305ee3e031a3

Open the link, take the saved result, recompute its hash over the canonical bytes, and compare it with the output_hash on the receipt. The AER-1 corpus behind the format is 143 vectors and 146 checks, live.

## Install

Cursor Marketplace: install the Zambo plugin, or add the MCP server manually with this config:

```json
{
  "mcpServers": {
    "zambo": {
      "url": "https://zambo.dev/mcp",
      "transport": "streamable-http"
    }
  }
}
```

The same config lives in `mcp.json` at the root of this repo, and the plugin manifest lives in `.cursor-plugin/plugin.json`.

## Pricing

Every tool free once a day, plus 3 continue calls. One free wrap-up handover per day, and pickup is always free.

- Day Pass: $0.99, unlimited for 24 hours.
- Zambo Pass: $29/mo.
- Lifetime Pass: $250.

## License

MIT. See LICENSE. The plugin bundle is MIT licensed; the hosted Zambo service is a separate product at https://zambo.dev.
