# BridgeNode for Claude Code

Version 1.0.0 · Publisher: NAXT LLC

Connect to the existing BridgeNode service over remote HTTP MCP with browser OAuth. Each customer signs in to their own BridgeNode account; no customer credentials are bundled. Access depends on the account, OAuth scopes, enabled server profiles and operating-system permissions. Commands may change remote systems and execute immediately; BridgeNode records command results and activity.

## Install from GitHub

```sh
claude plugin marketplace add naxtllc/claudeplugin
claude plugin install bridgenode@naxtllc-bridgenode
```

Restart Claude Code, then use `/mcp` to authenticate to BridgeNode privately.

## Try locally

Extract the ZIP into a folder, then run:

```sh
claude --plugin-dir /absolute/path/to/bridgenode
```

In Claude Code, open `/mcp`, select BridgeNode and authenticate in the browser. If BridgeNode is already configured manually, disable that duplicate entry before testing this plugin.

Start with: “List my BridgeNode servers and connections. Do not run any commands.”

## Included workflows

- `/bridgenode:discover`: inventory servers, profiles and connections.
- `/bridgenode:run-commands`: carry out a requested server command and retrieve its recorded result.
- `/bridgenode:deploy-check`: inspect a deployment with read-only diagnostics.

Workflows do not add new backend tools or grant permissions. Database and file capabilities are limited to those advertised by the authenticated service. There are no hooks, local executables, API keys or embedded passwords in this bundle.

## Links

- Website: https://bridgenode.ai
- Setup: https://bridgenode.ai/claude
- Support: https://bridgenode.ai/contact
- Privacy: https://bridgenode.ai/privacy
- Terms: https://bridgenode.ai/terms

## Validation and publication

Run `claude plugin validate --strict /absolute/path/to/bridgenode` before publishing. Then test OAuth and inventory in a signed-in Claude Code session. Use an isolated test server for a command test; do not test against customer workloads without authorization. Public directory acceptance is separate from local manifest validation. This archive is not evidence of approval or publication.
