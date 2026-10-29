# Spectr for Cursor

Cursor plugin that connects your agent to [Spectr](https://spectr.pm) through Spectr's own hosted
[Model Context Protocol](https://modelcontextprotocol.io/) server.

Spectr turns client meetings into requirements, spec sheets and stories for software teams. With this
plugin, Cursor's agent can read the story you are working on, its acceptance criteria, the requirement
behind it and the decisions recorded in its spec sheet, without you pasting them into the editor.

## Install

1. Open **Cursor Settings → Plugins**.
2. Search for **Spectr**.
3. Click **Install**, then sign in to Spectr when Cursor asks.

Or run `/add-plugin spectr` in chat.

## MCP

```json
{
  "mcpServers": {
    "spectr": {
      "type": "http",
      "url": "https://mcp.spectr.pm/mcp"
    }
  }
}
```

Sign-in is OAuth. Spectr's sign-in page shows what Cursor asks for, **read** or **read and write**, and lets
you choose which workspaces it can reach before you approve.

## What the agent can do

| Area | What it can do |
| --- | --- |
| Projects | Read projects, meetings, requirements, spec sheets and stories |
| Memory | Read a project's memory: product overview, features, architecture, glossary, open questions |
| Delivery | Read scope creep, budget, team and delivery progress, where your role allows |
| Development | Read workstreams and the coding-agent runs linked to them |
| Actions | With read and write access: create requirements, update or approve stories, process meetings and more, the same as Spectr's buttons |
| Help | Explain a part of Spectr, or how to connect an integration |

The full tool list is at [spectr.pm/docs/mcp/tools](https://spectr.pm/docs/mcp/tools/). The hosted server is
the source of truth for tool names and schemas.

## Notes

- The agent acts as you. It sees only what your role allows in each workspace, and can never do more than you
  can in the app.
- Writes need the **read and write** grant. Actions that run AI count toward the workspace's monthly usage,
  exactly as they do from the app.
- Connecting is free on every Spectr plan.
- Disconnect any time from **User Settings → Connections** in Spectr.

## Links

- Setup guide: https://spectr.pm/docs/mcp/
- Privacy policy: https://spectr.pm/privacy/
- Terms of service: https://spectr.pm/terms/
- Server URL: https://mcp.spectr.pm/mcp

## License

MIT
