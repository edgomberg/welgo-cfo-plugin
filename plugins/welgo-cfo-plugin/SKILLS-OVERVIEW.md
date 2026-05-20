# Skills you have access to (Welgo CFO)

Inside Claude Code, type `/<skill-name>` to invoke any of these. Many are universal Life OS skills; some are Welgo-specific.

## CFO daily-use (CRITICAL)

| Skill | When |
|---|---|
| `/bookkeeper-morning` | First thing each day: review queue summary, daily cash position. |
| `/qbo-categorize` | Clear flagged QBO transactions one at a time. |
| `/capture` | Anything you do outside Claude Code (bank portal action, manual reconcile, Priya call). Claude logs to Welgo Brain. |
| `/voice-check` | MANDATORY before any landlord / vendor / Priya-facing outbound. |
| `/pre-delegate` | Before delegating a task to anyone (e.g., bookkeeper VA, AP clerk): spec deliverable + deadline + fallback. |

## Welgo Brain MCP queries (English, no skill prefix needed)

You ask the brain in plain English. Examples:

- "List my open tasks"
- "Show me the task summary"
- "Search comms for `Priya` in the last 60 days"
- "How many vendor payments over $500 in last 30 days"
- "Get the canonical rent state for unit X"
- "Show Airwallex balances"
- "Create a finance task for me titled 'X' with priority high"
- "Get the canonical pricing rules"

Claude routes to the right MCP tool.

## Finance-specific (Ed has built these for personal finance; useful for CFO too)

| Skill | When |
|---|---|
| `/fin` / `/fin-import` | Import bank/card statement CSV (Revolut, Chase, Airwallex, Wise). Categorize. Reconcile. |
| `/fin-era` | Era Context MCP (Plaid feeds, balance lookups, transaction search). |
| `/finance-expert` | Reference for FinTech, banking, payments, financial tech questions. |
| `/finance-manager` | Quarterly financial planning, multi-entity oversight. |
| `/coupon-scout` | Audit SaaS / vendor spend for stackable discounts. |

## Work flow / quality

| Skill | When |
|---|---|
| `/grill-me` | Pressure-test any financial decision (treasury allocation, payment timing, vendor pick) before you commit. |
| `/clarify-before-solve` (built-in) | Ed's house rule: before any multi-step action, restate what you know + ask one clarifying question. |
| `/preserve-evidence` | Any financial dispute, fraud event, audit trail: preserve before you act. |

## Coordination

| Skill | When |
|---|---|
| `/pre-call` | Before a 1:1 with Ed: pulls role card + recent context. |
| `/one-on-one` | Structured weekly 1:1 with Ed. |
| `/role-card` | View / update your own role card. |
| `/goals-card` | Quarterly goals (Cagan-style outcomes + KPIs). |
| `/follow-up-track` | Tag any outbound (email to Priya, vendor invoice ask, KYC submission) you expect a reply on. Receipt watch auto-fires. |

## DON'T use these (Ed-personal contexts)

- `/morning-briefing`, `/power-down`, `/weekly-review`, `/post-therapy`, `/atg-analyze`, `/health-photo-track`, `/learn`, `/dashboard`
- `/buy`, `/grocery` (Ed's personal purchasing)
- `/file-police-report`, `/file-insurance-claim` (Ed-direct)

## Discovery

Type `/` inside Claude Code to see the full slash-command palette.

## Rule of thumb

Claude Code is your CFO surface. Welgo Brain is your system of record. If you did the work but Brain does not know, the work did not happen.
