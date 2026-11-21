# Plugin layout

The repository keeps the OpenCode package entrypoint at `index.js` and the Codex plugin manifest at `.codex-plugin/plugin.json`.

Both entrypoints are intentionally empty. The package does not currently register tools, commands, skills, MCP servers, or hooks. Add behavior only with a separately specified feature and update this page when the layout changes.
