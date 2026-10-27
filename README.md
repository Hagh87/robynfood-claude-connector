# RobynFood Tables for Claude

A Claude plugin: one remote connector (`https://table.robynfood.com/claude/mcp`), one skill, one command.

## What the customer experiences

1. Adds the plugin in Claude and presses **Connect**.
2. Claude opens table.robynfood.com: **Continue with Google**.
3. No restaurant website yet? It is created (free demo) - then the customer lands on **Claude (AI)**, the AI settings page of the portal.
4. **AI Assistant add-on** not booked: the customer is asked to **Book the AI add-on** (Stripe) or taps **Not now** - then nothing is activated or stored.
5. Booked: **Connect Claude**. The portal switches the AI add-on on in the restaurant and adds a private Claude API key to the restaurant; Claude is connected.

Read-only tools: `restaurant_overview`, `list_reservations`, `list_tables`.

## Install

- Claude Code: `/plugin marketplace add <path-or-repo-of-this-folder>` then `/plugin install robynfood-tables@robynfood`
- Claude plugin directory: submit this folder (it contains `.claude-plugin/plugin.json`, `.mcp.json`, `skills/`, `commands/`).

The server side is the `robyfood-portal` theme (version 2.5.0+) on table.robynfood.com - see `inc/claude-connect.php` and the portal README.
