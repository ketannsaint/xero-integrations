# Xero integrations

Canonical monorepo for independent Xero integrations. The first product under
validation is **Price Guard**.

## Current stage

**Paid validation only. Do not build the OAuth integration yet.**

Price Guard proposes this narrow workflow:

`authorised supplier bill -> changed item unit cost -> margin-impact proposal -> human approval -> update future item defaults -> immutable receipt and rollback`

It must never change a price without human approval. No outreach has been sent,
no payment has been accepted, and no production Xero organisation has been
connected from this repository.

## Target buyer

An Australian wholesaler, trade supplier, manufacturer, or small distributor
that meets every condition below:

- Uses native Xero Products and Services as the authoritative item master.
- Maintains at least 100 items that are both purchased and sold.
- Enters base-currency supplier bills containing Xero item codes.
- Encounters at least 20 changed-cost bill lines per month.
- Uses Xero item defaults on later purchase orders, quotes, or invoices.
- Does not use another inventory system as the authoritative price master.

## Paid test

Sell a one-time **A$59 Cost-Change Risk Audit**. The buyer supplies one redacted,
base-currency, item-coded supplier bill and the current purchase and sale
defaults. Within two business days, return a source-linked report of old and new
costs, percentage changes, current sale prices, resulting gross margins, and the
sale prices needed to preserve the previous gross margins.

The audit requires no Xero credentials and makes no Xero changes. Refund A$59 if
the input contains no qualifying cost change. Credit A$59 to month one only if
software is later built and the buyer agrees in writing.

## Build gate

Build only when all conditions hold:

- At least 3 of the first 10 qualified audit offers produce cleared, unrefunded
  A$59 payments.
- At least 2 paying buyers document A$708 or more in annual labour or margin
  exposure.
- Every paying buyer accepts human approval, the narrow exclusions, and the
  required Xero permissions.
- The paid inputs need no FX, landed costs, pack conversions, credits, negative
  quantities, tax advice, or multiple price lists.
- Paying buyers value recurring monitoring, not only the one-time audit.

The three-payment rule is intentionally retained because the kill rule requires
three payments after ten qualified offers. Paid validation permits small Xero
contract probes; it does not prove the API behavior.

## Kill or revise

- Fewer than 3 payments after 10 qualified offers.
- 20 relevant conversations cannot produce 10 qualified prospects.
- Most prospects have fewer than 20 changed-cost lines per month.
- 2 of the first 3 paying buyers require excluded functionality.
- Buyers reject the required Xero permissions.
- Xero announces the native workflow with a credible delivery date.

## Launch blockers

| Blocker | Needed before | Status |
| --- | --- | --- |
| Real sender name | First outreach | Supplied: Leopold Saint |
| Business or trading identity | First outreach and public page | Supplied for research: Leopold Saint; legal invoicing identity and country still required before payment |
| Monitored business reply address | First outreach and public page | Supplied: leo.saint.dior@gmail.com |
| Public HTTPS URL | First outreach | GitHub Pages selected; GitHub remote still required |
| Two replacement Australian prospects | Completing the 10-prospect AU cohort | 8 AU targets ready; 2 international drafts retained as non-counting backups |
| Provider approval and owner KYC for the exact audit terms | Offering an invoice or accepting payment | Status unknown; treat as not started |
| Written Xero answer on certification for a non-listed Core commercial integration | Any production API onboarding | Not requested yet |

The first action required to contact prospect 1 is now to publish the static
page at a public HTTPS URL and replace the remaining URL placeholder. Sending
the message still requires explicit owner authorization.

## Publish blocker

The public repository is <https://github.com/ketannsaint/xero-integrations> and
the expected validation URL is
<https://ketannsaint.github.io/xero-integrations/>. The included workflow
publishes `apps/price-guard-validation/`. In GitHub, set **Settings -> Pages ->
Build and deployment -> Source** to **GitHub Actions** if it is not already the
selected source.

## Repository map

- `apps/price-guard-validation/` - static public validation page and interactive
  concept; this is not the application.
- `products/price-guard/PAID-VALIDATION.md` - qualification, offer, delivery,
  payment, and decision rules.
- `products/price-guard/OUTREACH.md` - ten individual messages and one follow-up.
- `products/price-guard/OUTREACH-TRACKER.csv` - source, qualification, outreach,
  payment, delivery, and outcome ledger.
- `products/price-guard/OFFICIAL-FACTS.md` - dated fact/inference/unknown register.
- `products/price-guard/DECISION-LOG.md` - dated decisions and revisit triggers.
- `.github/workflows/deploy-validation.yml` - A$0 static GitHub Pages deployment.

No paid infrastructure or Xero App Store listing is needed during validation.
If the build gate passes, stay on Starter through 5 connections and Core through
50 connections, subject to written clarification from Xero.