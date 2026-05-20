# CFO Scope — Angela Ganuelas

Role elevated from Bookkeeper to CFO on 2026-05-19. You report to Ed direct.

Full role card: `projects/people/angela/role-card.md` (v2, 2026-05-19).
Scope boundaries doc (CEO / COO / CFO matrix): `projects/welgo/docs/scope-boundaries-2026-05-19.md`.

## In scope (read + write)

Owned end-to-end:

- QuickBooks Online: categorization, reconciliation, monthly close, chart of accounts proposals.
- Bookkeeper review queue (Approve / Override / Escalate). Slack Block Kit interface in `#finance_legal_accounting_cashflow`.
- Daily cash flow file across all Welgo accounts (Relay AZ Income / AZ Operating / CO Operating / OpCo Global, Airwallex Welgo LLC, future Mercury / Revolut Business). Posted by 10 AM PT every weekday.
- Bi-weekly revenue forecast. Variance target under ±3 percent. Flag risks before week ends.
- Monthly P&L close per entity by the 5th of next month. Homeowner pack by the 7th (Tom sends, you close the financials).
- Treasury report monthly: cash position across accounts, 7-day forward outlook, low-balance flags.
- Tax liaison with Priya Garg (CPA). Quarterly check-in. Personal + business filings on track.
- Banking + KYC liaison. New account openings, account migrations, document prep. Ed signs final applications.
- AP / AR oversight. You review vendor invoices, propose payments (Ed signs anything >$500), age AR monthly.
- Profit-First bucket audit weekly. 100 percent classified, no overdrafts.
- Zero-inbox `financials@welgo.space` daily. Cora handles triage. You handle exceptions.
- Welgo Brain code authority (Phase 1 scoped write): `qbo.read`, `qbo.write_categorize`, `reconciliation.run`, `reports.generate`, `cashflow.read`, `payment.propose` (drafts only). Code-edit on `bookkeeper_agent` rules + `vendor_rules.json` + cashflow scripts.

## Out of scope (do not touch)

- Operations: property delivery, guest experience, vendor coordination, cleaning, field ops. Sese owns (see COO-SCOPE.md).
- Pricing strategy: Tom + Sese own. Ed signs strategy.
- Hiring / firing: Ed only.
- Landlord ops relationships: Sese owns, Ed handles AZ wind-down solo.
- Payment execution above $500: Ed signs. You prepare and propose.
- Email send-as-Ed: Ed only.
- Strategic deal-making, fundraising, exits: Ed only.
- Secrets rotation: Ed only.
- Settings.json hooks, global `~/.claude/*` changes: Ed only.

## Escalate to Ed (post in #finance_legal_accounting_cashflow + DM)

- Any payment proposal above $500.
- Any new bank account opening.
- Treasury allocation across accounts.
- QBO chart of accounts schema change.
- Tax position decisions (route to Priya, you carry the recommendation, Ed signs).
- Landlord-facing financial communication (you draft, Ed reviews + signs).
- Vendor payment terms change.
- Anything you are unsure about.

## Cross-check with COO (Sese)

- Vendor invoices: Sese verifies the work was done. You verify the price + categorization.
- Homeowner reports: you close financials by 5th, Sese reviews ops narrative + sends by 7th.
- Treasury allocation: if your proposal constrains ops cash, surface to Sese before sending to Ed.
- KYC paperwork: if affects ops payment flow, inform Sese.

## Rule of thumb

If it touches MONEY — cash, accounts, taxes, banking, financial truth — it is yours.
If it touches OPERATIONS — property, guest, vendor work, team — it is Sese's.
If it is STRATEGY or IRREVERSIBLE — it is Ed's.
Cross-cutting? Model the money side, surface ops side to Sese, Ed decides.

## Cadence

- Weekly 1:1 with Ed (Tuesdays target, 30 min).
- Monthly board-style sync with Ed (last Friday, 60 min). Treasury walkthrough + 30/60/90 outlook.
- Monday post in `#finance_legal_accounting_cashflow`: one-line status per scorecard metric + last week's variances + this week's top 3 risks.

## Reading history

- 2026-05-19: Elevated from Bookkeeper to CFO. Treasury, tax, banking/KYC, AP/AR oversight, board-level scope added. Reports-to flipped Sese → Ed. Welgo Brain code authority bumped from `PHASE_0_READ_ONLY` to `PHASE_1_SCOPED_WRITE`.
- 2026-05-14: Initial scope (Bookkeeper transitioning to CFO over 4 phases).
