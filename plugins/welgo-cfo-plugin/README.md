# welgo-cfo-plugin

Pre-packed Claude Code setup for the Welgo CFO / Bookkeeper role.

## What it does

Bundles everything you need to do bookkeeper work inside Claude Code: rules, skills, an MCP connection to Welgo Brain, hooks, and your agent definitions.

## Prereqs (one-time per machine)

1. Claude Code installed.
2. Tailscale installed and signed in with your work Google account.
3. You've been added to the Welgo tailnet via Ed's share link.
4. `WELGO_BRAIN_TOKEN` set in your shell (Ed sends this privately, paste into `~/.zshrc` as `export WELGO_BRAIN_TOKEN=...`, then `source ~/.zshrc`).

## Install

Inside Claude Code:

```
/plugin install https://github.com/edgomberg/welgo-cfo-plugin
```

That's it. Claude Code prompts you to confirm. Hit yes. Restart Claude Code.

## Updates

Every time you start Claude Code, it checks for plugin updates. If new version available, you'll see a banner. Run `/plugin update welgo-cfo-plugin` to apply.

## Daily use

- `/qbo-categorize` — clear today's flagged QBO transactions.
- `/bookkeeper-morning` — morning briefing for finance scope.
- Session-start auto-shows count of items in your review queue.

## Escalation

Anything outside your scope, post in Slack `#finance_legal_accounting_cashflow` and tag Ed.

## Questions

Ping Ed directly in Slack DM.
