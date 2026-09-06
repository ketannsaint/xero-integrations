# Price Guard official fact check

Checked: **2026-09-06**

Labels used below:

- **Fact** - directly supported by the linked official source.
- **Inference** - a bounded conclusion from the checked facts.
- **Unknown** - requires a written answer or a post-gate contract probe.

## Demand request

**Fact:** Xero's request, "Inventory - Option to automatically update Purchase
Price from bills," remains **Submitted** with **195 votes**. Its four comment
pages contain 20, 20, 20, and 11 comments respectively, or **71 comments**. The
newest visible comments are from 12 August 2026; the latest says the commenter
may change accounting packages because of the omission. Xero's latest visible
admin response remains dated 27 April 2023.

Source:
<https://productideas.xero.com/forums/967139-purchase-orders-bills-inventory/suggestions/44988598-inventory-option-to-automatically-update-purchas>

**Inference:** This is strong evidence of persistent pain, not evidence that a
buyer will pay Price Guard.

## Native product releases

**Fact:** The official release log checked through September 2026 does not
announce the requested item-default workflow. It does list an adjacent September
change: when saving a bill for a **new supplier**, bill details can be saved as
that supplier's purchase default settings. The same month adds backorder reports;
July and August add other inventory and purchase-order improvements.

Source: <https://central.xero.com/s/article/Xero-product-releases>

**Inference:** Supplier/contact defaults are not the same object as a Product and
Services item's `PurchaseDetails.UnitPrice` or `SalesDetails.UnitPrice`. The
September wording therefore does not satisfy the Price Guard workflow, and the
item-price request remaining Submitted supports that reading.

**Unknown:** The anonymous release page returned its New Zealand localization.
Australian-account behavior must be rechecked in an Australian demo organisation
after the payment gate; do not infer parity from the release summary alone.

## App Store competition

**Fact:** Current Australian App Store searches for `last cost`, `cost price
update`, `supplier price update`, and `margin markup`, plus the Inventory
category, did not return a focused listing advertising this complete chain:

`authorised supplier bill -> changed native item cost -> margin preview -> human approval -> native item default update`

The visible matches are broad inventory, order, restaurant, rental, CRM, and
reporting products such as Workhorse, Unleashed, Cin7 Core, and Peach Software.
The `margin markup` query returned no matches.

Sources:

- <https://apps.xero.com/au/search?q=last%20cost>
- <https://apps.xero.com/au/search?q=cost%20price%20update>
- <https://apps.xero.com/au/search?q=supplier%20price%20update>
- <https://apps.xero.com/au/search?q=margin%20markup>
- <https://apps.xero.com/au/function/inventory>

**Inference:** No focused listed competitor was found. Search results do not
prove that no unlisted, private, or newly named competitor exists.

## Developer pricing

**Fact:** Xero publishes these tax-exclusive AUD tiers:

| Tier | Maximum connections | Monthly fee | Certification prerequisite | App Store |
| --- | ---: | ---: | --- | --- |
| Starter | 5 | A$0 | None shown | Not available |
| Core | 50 | A$35 | None shown | Not available |
| Plus | 1,000 | A$245 | App certification | Optional |

Core includes 10 GB monthly API egress; Plus includes 50 GB. Overage is A$2.40
per GB. A payment method is required when moving from Starter to Core. Xero says
connections and usage are measured per app and cannot be shared between apps.

Sources:

- <https://developer.xero.com/pricing>
- <https://developer.xero.com/faq/pricing-and-policy-updates>

**Fact:** At A$59 per organisation per month, 17 customers equal A$1,003 MRR and
50 equal A$2,950 MRR. Those are arithmetic scenarios, not revenue forecasts.

## Certification ambiguity

**Fact:** The pricing matrix shows no certification prerequisite for Starter or
Core. However, section 2.1 of the current Commercial Terms says that to offer an
integration to Xero users, the app and partner need certification "unless we
advise you otherwise." The pricing FAQ also phrases one question as a
certification requirement for "Core, Plus, Advanced, and Enterprise," while its
tier table shows certification only from Plus.

Sources:

- <https://developer.xero.com/pricing>
- <https://developer.xero.com/faq/pricing-and-policy-updates>
- <https://developer.xero.com/xero-developer-platform-commercial-terms>

**Unknown:** Whether an unlisted, commercial Core-tier Price Guard may onboard
production customers before certification. Obtain a written Xero support answer
before the first production API customer. Do not resolve this by interpretation.

## OAuth scopes

**Fact:** Since March 2026, Web and PKCE apps have granular Accounting API scopes.
The current scope table lists `Items` under both:

- `accounting.invoices` / `accounting.invoices.read` (new granular scopes), and
- `accounting.settings` / `accounting.settings.read` (unchanged scopes).

`offline_access` is required to receive a refresh token. The August 2026
changelog says broad scopes remain available only until September 2027.

Sources:

- <https://developer.xero.com/documentation/guides/oauth2/scopes>
- <https://developer.xero.com/changelog>

**Unknown:** Whether `offline_access accounting.invoices` alone reliably permits
reading authorised bills and reading/writing both tracked and untracked Items for
this app. Confirm in Xero's API Explorer or a demo organisation after the paid
gate, then request only the minimum proven scopes.

## API and webhook contract

**Fact:** The Invoices endpoint represents purchase bills as `Type=ACCPAY` and
approved bills as `Status=AUTHORISED`. Invoice `CREATE` and `UPDATE` webhook
events are available. Xero requires consumers to implement idempotency and
replayability; failed deliveries can be retried and retained for replay.

**Fact:** The Items endpoint can read and update `PurchaseDetails.UnitPrice` and
`SalesDetails.UnitPrice`. `TotalCostPool`, `QuantityOnHand`, and related tracked
inventory quantities are read-only through Items and change through accounting
transactions instead.

Sources:

- <https://developer.xero.com/documentation/api/accounting/invoices>
- <https://developer.xero.com/documentation/api/accounting/items>
- <https://developer.xero.com/documentation/guides/webhooks/overview>

**Unknown:** The public documentation does not prove all contract details Price
Guard depends on: webhook behavior for every transition into authorised ACCPAY,
preservation of omitted Item fields during a partial update, concurrent-change
detection, or safe rollback behavior. These remain post-payment contract probes.

## Data use

**Fact:** Xero's current developer terms prohibit using data obtained through
Xero APIs to train or contribute to an AI or machine-learning model.

Source: <https://developer.xero.com/faq/pricing-and-policy-updates>

Price Guard does not need AI for its controlling calculations or write path.

## Payment-provider gate

**Fact:** Razorpay supports no-code Payment Links and invoices in supported
international currencies; its live currency list includes Australian dollar
(`AUD`). Indian-business settlements are made in INR. International card
acceptance requires a Dashboard application and approval by Razorpay's banking
partners after security and risk checks.

**Fact:** Razorpay requires account activation and KYC. Its documentation lists
individual/unregistered businesses and proprietorships as supported business
types, but approval remains account-specific. The published international-card
fee is up to 3% per successful transaction plus 18% GST on the fee, with no setup
fee or annual maintenance charge.

**Fact:** A normal refund returns funds to the original payment method and has
no separate processing fee. The original transaction fee and GST are not
reversed to the merchant.

Sources:

- <https://razorpay.com/docs/payments/set-up/>
- <https://razorpay.com/docs/payments/business-types-kyc-documents/>
- <https://razorpay.com/docs/payments/international-payments/>
- <https://razorpay.com/docs/payments/international-payments/international-debit-credit-cards/>
- <https://razorpay.com/docs/payments/payment-links/>
- <https://razorpay.com/docs/payments/invoices/create/>
- <https://razorpay.com/docs/payments/refunds/normal/>
- <https://razorpay.com/pricing/>

**Unknown:** Whether Razorpay will approve Leopold Saint's identity/business
type and the exact A$59 audit, future-credit, and full-refund terms. Treat the
provider as unavailable until KYC and written approval are complete. Do not
accept payment meanwhile.