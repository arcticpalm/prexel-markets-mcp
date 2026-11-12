# Prexel Markets Free for Cursor

Read Bitcoin Synthesis and the saved Daily Brief, at least 24 hours delayed. The server is read-only; its observations are not trading recommendations. Source clocks can differ from the capture time.

This package connects Cursor to `https://markets.prexel.xyz/mcp/free` and includes two skills:

- `morning-read` builds a dated market overview from captured evidence.
- `thesis-check` tests a user's stated thesis against supporting and conflicting captured observations.

After the plugin is installed and enabled, ask Cursor to use a skill or invoke `/morning-read` or `/thesis-check`. The assistant may need multiple reads to inspect the requested evidence. It should keep capture and edition IDs separate, report missing or stale inputs, and say when the requested evidence cannot be retrieved.

For connection information and support, visit [Prexel Markets MCP](https://prexel.xyz/mcp/) or email mcp@prexel.xyz.

## Direct MCP connection

[Add Prexel Markets Free to Cursor](https://cursor.com/link/mcp/install?name=prexel-markets-free&config=eyJ1cmwiOiJodHRwczovL21hcmtldHMucHJleGVsLnh5ei9tY3AvZnJlZSJ9). Cursor asks you to confirm the connection. This link installs the MCP connection only; it does not install the bundled skills. No account or API key is required.

You can also merge the following entry into Cursor’s MCP settings without replacing your existing servers:

```json
{
  "mcpServers": {
    "prexel-markets-free": {
      "url": "https://markets.prexel.xyz/mcp/free"
    }
  }
}
```

Try: “Give me a concise Bitcoin market read: the main observation, one counterpoint, and gaps that matter.”

For a thesis check: “Do Bitcoin positioning and ETF flows support the same reading? Show evidence on both sides, its timing and any gaps.”

The Synthesis source link is a rolling view and may show a different capture. A returned Daily Brief source link identifies a saved edition. Free captures are retained for follow-ups for up to two hours; an expired capture cannot be reconstructed by silently replacing it.

[Privacy](https://prexel.xyz/privacy/) · [Terms](https://prexel.xyz/terms/) · [Support](https://prexel.xyz/support/)
