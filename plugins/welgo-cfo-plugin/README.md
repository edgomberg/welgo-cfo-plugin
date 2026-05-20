# welgo-cfo-plugin

Pre-packed Claude Code setup for the Welgo CFO role. Built for Angela Ganuelas.

## What it does

Bundles everything you need to run the CFO function inside Claude Code: scope docs (CFO + COO cross-reference), rules, skills, an MCP connection to Welgo Brain, and session-start hooks. One install command, full operator kit on your laptop.

## Prereqs (one-time per machine)

1. **Claude Code installed.** Free: https://claude.com/claude-code
2. **Tailscale installed and signed in** with your Google account (`lala.ganuelas@gmail.com`). Ed sends the tailnet invite. Accept it. Open the Tailscale app on your Mac.
3. **Your machine appears on Ed's tailnet** as a connected node (Ed verifies this from his side via `tailscale status`).

The Welgo Brain server has two auth paths:

- **Path A (preferred): tailnet identity.** If your Mac is signed into Ed's tailnet AND `mac-mini-brain.tail59326c.ts.net` resolves on your machine, no token is needed. The server reads your tailnet identity from the proxy header.
- **Path B (fallback): per-operator bearer token.** If you are off-tailnet (e.g., Tailscale install pending OR travel without VPN), Ed sends you a personal bearer token via secure channel. Paste it into `~/welgo/.env` (the plugin creates this file at session-start as a scaffold).

The plugin handles both paths automatically. You do not pick.

## Install

Inside Claude Code, run:

```
/plugin marketplace add edgomberg/welgo-cfo-plugin
/plugin install welgo-cfo-plugin@welgo-cfo-plugin
```

Claude Code prompts you to confirm. Hit yes. Restart Claude Code.

The session-start hook auto-downloads the Welgo Brain wrapper file to `~/welgo/welgo-brain-remote-mcp.js` on first run. No manual setup.

## Verify install

In a new Claude Code session, type:

```
Use welgo-brain to list my open tasks.
```

You should see real Welgo data — task IDs, titles, statuses. Not a generic AI answer. If you see an error or a generic answer, ping Ed in Slack DM and paste the error text.

## Updates

Every Claude Code session checks for plugin updates. If you see "update available" banner, run `/plugin update welgo-cfo-plugin@welgo-cfo-plugin`.

## What's bundled

- **Scope docs:** `CFO-SCOPE.md` (your full role per v2 elevation 2026-05-19) and `COO-SCOPE.md` (Sese's scope, so you can spot ops items that route to her).
- **Rules:**
  - `financial-delegation-finance-channel-with-cfo-cc.md` — every financial delegation goes to `#finance_legal_accounting_cashflow` with Sese CC'd.
  - `welgo-bookkeeper-review-flow.md` — Approve / Override / Escalate contract for QBO queue.
- **Skills:**
  - `/qbo-categorize` — clear today's flagged QBO transactions one by one with explanations.
  - `/bookkeeper-morning` — morning briefing for finance scope. Run first thing.
- **Agents:** `cfo-reviewer` — agent that reviews your proposed categorizations + flags inconsistencies before commit.
- **MCP server:** Welgo Brain remote via Tailscale identity auth. No token to manage.
- **Hooks:** Session-start auto-fetch of Welgo Brain wrapper. Auto-shows count of items waiting in your bookkeeper review queue.

## Daily flow

1. Open Claude Code.
2. Session-start hook surfaces: "N items pending in bookkeeper queue."
3. Run `/bookkeeper-morning` for full finance briefing.
4. Run `/qbo-categorize` to clear queue items.
5. Post Monday status to `#finance_legal_accounting_cashflow` (one-line per scorecard metric).

## Escalation

| Situation | Where |
|---|---|
| Anything above your scope (see CFO-SCOPE.md) | `#finance_legal_accounting_cashflow` + DM Ed |
| Tax / Priya | DM Ed first, then Priya direct via WhatsApp |
| Emergency (system down, wrong send, fraud) | DM Ed direct, immediate |
| Ops question (vendor scope, property issue) | DM Sese — not your channel |

## Questions

Ping Ed directly in Slack DM `D098N107KGX`. Reply in your DM thread on the CFO elevation announcement.

## Reading history

- 2026-05-19 v0.2 — CFO elevation. COO-SCOPE.md added as cross-reference. CFO-SCOPE.md updated to reflect treasury + tax + banking/KYC + AP/AR + board-level scope per role-card v2. README rewritten for tailnet-identity auth (bearer token removed from prereqs).
- 2026-05-14 v0.1 — Initial bookkeeper-era scaffold.
