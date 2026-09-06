# Xero Price Guard Paid Validation

Source artifact last verified: 2026-08-31

Xero request, release, pricing, scope, API, webhook, and App Store facts were
rechecked on 2026-09-06. See `OFFICIAL-FACTS.md`. Prospect routes and payment-
provider approval remain launch checks rather than assumed facts.

## What this test answers

We do not know whether buyers will pay. Votes, comments, interviews, waitlist
signups, and statements such as "I would use this" prove interest, not
willingness to pay.

The test is:

`public complaint -> qualified workflow -> own-data preview -> A$59 payment`

Build only after three qualified businesses make cleared payments. A promise,
letter of intent, meeting booking, trial request, or unpaid invoice counts as
zero.

## Offer a deliverable, not an empty deposit

Sell a **Cost-Change Risk Audit** for A$59. It gives the buyer immediate value
before software exists:

1. The buyer supplies one redacted, base-currency supplier bill containing Xero
   item codes and the current purchase and sale defaults for those items.
2. Within two business days, manually return a source-linked report showing old
   cost, bill cost, percentage change, current sale price, margin impact, and the
   sale price required to preserve the current gross margin.
3. Include the interactive Price Guard concept preview.
4. If Price Guard is built, credit the full A$59 to the first month. If the bill
   contains no qualifying cost change, refund the full A$59.

This tests whether the outcome is worth money, avoids pretending unfinished
software exists, and produces the representative inputs needed to design the
product safely. Do not update the buyer's Xero data during validation.

## Qualification gate

A prospect receives the payment offer only when all answers are yes:

1. Do you use native Xero Products and Services as the default-price source?
2. Do supplier bills normally contain Xero item codes?
3. Do at least 20 bill lines per month arrive with changed item costs?
4. Do you maintain at least 100 purchased-and-sold items?
5. Is the affected bill in the Xero organisation's base currency?
6. Would approving future purchase and optional sale defaults solve the current
   problem without FX, landed costs, pack conversions, or multiple price lists?

Record the current workaround, time spent per month, one recent margin incident,
and whether another inventory system owns the item master. If another system
owns prices, the prospect is not qualified.

## Eight Australian prospects and two backups

Use only the public business route shown below. Mention the public Xero comment
that made the message relevant. Do not use personal email addresses, scrape
private details, imply a relationship with Xero, or add anyone to a mailing
list.

The public routes below were rechecked on 2026-09-06. Rows 8 and 10 are
international, non-counting workflow checks. Source two additional Australian
prospects before treating this as a ten-prospect Australian cohort.

| Priority | Prospect | Why the message is relevant | Public business route |
| ---: | --- | --- | --- |
| 1 | David Raymer, Carton Concepts / Derrimut Trophies & Gifts | In July 2026 he requested a bill-time prompt and noted that sale price may also need updating. His public Xero history describes tracked items, five suppliers for one ribbon, and leaving a separate inventory package. | <https://cartonconcepts.com.au/trophies/CONTACT.html> or `sales@derrimuttrophies.com.au` |
| 2 | Ian Forsyth, Forsyth Management Group | He described a client with more than 2,000 items, regular price changes, and updates left undone because they take too long. | <https://www.fmgpl.com.au/contact-us/> |
| 3 | Emma Rosenblatt, Alliance Industries Australia | She described constantly changing prices, a frustrated stock controller, thousands of component parts, and large invoices. | <https://www.allianceindustries.com.au/contact-us> or `admin@allianceindustries.com.au` |
| 4 | UDO Systems Accounts | The manufacturer supplies more than 250 stores and publicly described painful manual bulk-buy pricing and stock-control needs. | <https://udosystems.com/contact-us/> or `info@udosystems.com` |
| 5 | Lori Notman, LN Bookworkz | In June 2026 she requested automatic last-cost updates from bills, supplier visibility, and correct future purchase-order defaults. She advises retail, wholesale, and trade clients. | <https://www.lnbookworkz.com.au/> |
| 6 | Russell Spurrell, AIRE / GP HVAC Group | He described manual bill/PO price updates as laborious. The current business distributes HVAC units, spare parts, plumbing, tools, and accessories through eight branches. | <https://gphvac.com.au/about-us/> or `campbellfield@gphvac.com.au` |
| 7 | Ben Kampschoer, Omnium Cargo Australia | He called last-cost handling essential for an import business exposed to changing AUD costs. | <https://omniumcargo.au/> or `info@omniumcargo.au` |
| 8 | Stephanie Halcro, Halcro Heating and Cooling | In November 2025 she requested markup rules because frequent cost updates across products are slow and error-prone. | <https://halcrohc.com/contact/> or `hhc@halcrohc.com` |
| 9 | Chris Lloyd-Parker, Boat Names Australia | He requested time-saving sale-price updates when material prices rise. His company manufactures physical products in Australia. | <https://www.boatnames.com.au/contact/> |
| 10 | Matthew Abelheim, Coffee Unplugged | He publicly described manual bill-to-item price updates as archaic. The company imports and distributes coffee equipment, parts, beans, and accessories. | <https://www.coffeeunplugged.co.za/enquiry/index.html> or `sales@coffeeunplugged.co.za` |

Prospects 1-7 and 9 are Australian targets. Stephanie is US-based and Matthew is
South African; they are useful English-speaking workflow checks, but they do not
count toward the Australian validation cohort. Keep them as backups until two
Australian replacements with public business routes are verified. Country-
specific tax and currency details remain excluded from version one.

## First message

Subject: Your Xero comment about supplier cost changes

```text
Hi [First name],

I found your public Xero Product Ideas comment about [one exact pain from their
comment]. I am researching a small Xero add-on for businesses that use native
Products and Services.

When an authorised supplier bill contains a different item cost, it would show
the old cost, new cost, current sale price and margin impact. A person could then
approve updating the future purchase default, or both the purchase and sale
defaults. It would never change an existing bill or price without approval.

I made an interactive concept preview. Would you be willing to answer six short
fit questions and tell me whether this matches your current process? This is
research for an unbuilt product, and I am not affiliated with Xero.

[PUBLIC MOCKUP URL]

Regards,
[Sender name]
[Business name and reply address]
```

Do not include a payment link in the first message. The goal is to establish
relevance and qualify the workflow, not surprise a stranger with a checkout.

## Follow-up after qualification

```text
Thanks. Based on what you shared, your workflow fits the narrow first version.

Before writing software, I am taking payment from at most ten design partners
so I do not mistake polite interest for demand. The A$59 offer is a manual
Cost-Change Risk Audit using one redacted supplier bill and its current Xero item
defaults. Within two business days I will return the changed costs, margin
impact and suggested margin-preserving sale prices. No Xero connection or write
access is required.

The full A$59 will be credited to month one if the software is built. If your
bill contains no qualifying change, I will refund it. The proposed software,
scope, timing and limitations are shown before payment.

Would you like the one-time A$59 business invoice?
```

Send the private invoice only after the prospect explicitly asks for it.

## If they say "I will use it when it is built"

Reply once:

```text
Thank you. I am deliberately using payment as the build decision because many
useful-sounding products never become important enough to buy.

The A$59 is for a manual audit delivered now, and it is credited to the first
software month if I build it. If that is not worth paying for today, no problem;
I will record your response as interest, but not as paid validation.
```

Then stop selling. Record the response as `Interested / unpaid`, which counts as
zero. Do not lower the price, offer a fake deadline, promise that development is
certain, or build to persuade them later.

If several qualified buyers refuse because they do not trust an unknown vendor
rather than because the outcome lacks value, that is still a real go-to-market
failure. A product that requires trust we cannot currently earn is not yet a
business opportunity.

## Payment route

Use a private **Razorpay International Invoice or Payment Link in AUD** after all
of these are complete:

1. Razorpay approves international payments and the exact audit/credit wording
   in writing.
2. The account owner completes KYC, bank verification, and any export-purpose
   documentation Razorpay requires.
3. A public HTTPS page shows the deliverable, price, refund rule, contact
   details, privacy notice, and that the software is not built.
4. The invoice is one-time, A$59, has no automatic renewal, and expires after
   seven days.

Razorpay supports hosted links without an app, AUD international payments, and
source refunds. Its international-card fee can be up to 3% plus Indian GST on
the fee. The original processing fee is not reversed on a refund, so keep a
refund and FX cushion available and never spend the audit payment before the
deliverable and refund window are complete.

Do not use Gumroad for this test: its current policy prohibits payment for
services performed in the future. Do not use Paddle before software exists: it
can reject transactions with no bona fide software or service and requires an
approved product site. A manual audit is a real service, but Razorpay is the
cleaner India-based route after written approval.

Rechecked on 2026-09-06: Razorpay requires account activation and KYC before an
account can accept payments. It supports individual/unregistered businesses and
proprietorships, but account approval is case-specific. International cards need
a separate Dashboard request and approval from Razorpay's banking partners after
security and risk checks. Australian dollar (`AUD`) is listed as a supported
presentment currency, while settlement to an Indian business is in INR.
International cards cost up to 3% per successful transaction plus 18% GST on
the fee, with no setup fee or annual maintenance charge on the published
standard rate card.

A normal full refund returns the captured amount to the original payment method
and has no separate refund-processing fee. Razorpay explicitly says the original
transaction fee and GST are **not** reversed to the merchant. Keep that amount
available in addition to the customer's A$59. Public documentation does not
approve the Price Guard audit, future month-one credit, or refund wording; obtain
that approval in writing before offering an invoice. Do not open or activate a
provider account from this repository without owner authorization.

Fallback: a Wise Business AUD invoice paid by Australian bank transfer, but only
after Wise confirms in writing how an Indian account can return the full AUD
amount after mandatory conversion and payout.

Provider sources:

- <https://razorpay.com/docs/payments/international-payments/>
- <https://razorpay.com/docs/payments/payment-links/>
- <https://razorpay.com/docs/payments/invoices/create/>
- <https://razorpay.com/docs/payments/refunds/>
- <https://razorpay.com/docs/payments/refunds/normal/>
- <https://razorpay.com/docs/payments/set-up/>
- <https://razorpay.com/docs/payments/business-types-kyc-documents/>
- <https://razorpay.com/docs/payments/international-payments/international-debit-credit-cards/>
- <https://razorpay.com/pricing/>
- <https://gumroad.com/prohibited>
- <https://www.paddle.com/help/start/account-verification/what-am-i-not-allowed-to-sell-on-paddle>

## Invoice description

```text
Cost-Change Risk Audit for Xero Products and Services

One-time A$59 business service. The buyer supplies one redacted base-currency
supplier bill containing Xero item codes and the current item purchase and sale
defaults. Within two business days, the supplier will deliver a source-linked
report of qualifying cost changes, margin impact and suggested sale prices.

No software, Xero connection, subscription or future launch is included or
guaranteed. If Price Guard software is later offered, A$59 will be credited to
the buyer's first month only with the buyer's written approval. If the supplied
bill contains no qualifying cost change, A$59 will be refunded to the original
payment method. Processor fees will not be deducted from the buyer's refund.
```

Have an Indian chartered accountant confirm whether the payment requires a GST
receipt voucher, export/LUT treatment, invoice, refund voucher, or credit note.

## Tracker

For each prospect, append dates and notes after these fields:

```text
Prospect:
Contacted:
Replied:
Qualified:
Audit offered:
Invoice requested:
Payment cleared:
Audit delivered:
Result:
```

Create one copy for each prospect in this order: David Raymer, Ian Forsyth,
Emma Rosenblatt, UDO Systems Accounts, Lori Notman, Russell Spurrell, Ben
Kampschoer, Stephanie Halcro, Chris Lloyd-Parker, and Matthew Abelheim.

## Decision rules

Build only when all conditions hold:

- At least 3 of the first 10 **qualified audit offers** produce cleared A$59
  payments. The denominator is qualified offers, not cold messages.
- At least two paying buyers document A$708 or more in annual labor or margin
  exposure.
- All paying buyers accept base-currency item-coded bills, human approval, no
  existing-document repricing, no tracked-stock revaluation, and the required
  Xero write scope.
- The three audit inputs can be handled without FX, landed costs, packs/unit
  conversion, credits, negative quantities, or multiple price lists.

Kill or revise when any condition occurs:

- Fewer than three payments after ten qualified offers.
- Fewer than ten prospects qualify after twenty relevant conversations.
- Most prospects have fewer than twenty changed item lines per month.
- Two of the first three paying buyers require an excluded workflow.
- Buyers want only a one-time audit and do not value ongoing monitoring.
- Xero announces a native bill-time update prompt with a delivery date.

No code is written because of positive interviews. Paid audits create permission
to run the technical Xero contract probes; they do not remove the need to prove
the API, webhook, item-update preservation, idempotency, and rollback behavior.

## Outreach limits

- Send one relevant message and one follow-up after five business days.
- Stop immediately after a decline or unsubscribe request.
- Use individual messages, not a bulk campaign.
- Keep a record of source, date, response, and opt-out.
- Never attach a bill, expose customer data, or ask for Xero credentials.
- Ask buyers to redact supplier bank details, tax identifiers, addresses, and
  personal information before sharing an audit sample.
