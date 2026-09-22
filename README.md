# Flip Logic

Run the numbers. Win the deal.

A single-page fix & flip (and wholesale) deal analyzer for residential real estate. Enter a property's purchase
price, rehab budget and after-repair value, and it tells you whether the deal clears the 75% rule
and what you'd actually walk away with.

**Live:** https://pintorjosere-prog.github.io/Flip-Logic/

## The 75% rule

The core check. A deal passes when everything you put into the property stays at or below 75% of
what it's worth once repaired:

```
All-In       = Purchase Price + Rehab Budget
Max Offer    = (ARV x 0.75) - Rehab Budget
Deal passes  when All-In / ARV <= 0.75
```

The verdict panel shows your all-in cost, your actual percentage of ARV, the maximum you could
offer and still qualify, and how much room you have left below that number (or how far over
you are).

## What it calculates

**Deal inputs** — Purchase Price, Rehab Budget, After Repair Value (ARV)

**Financing** — Down Payment (defaults to 5%), Earnest Money Deposit, Closing / Origination Fees,
annual Interest Rate, Closing Costs to Buy

**Holding costs** — monthly Insurance and Property Taxes, carried over the hold period

**Exit** — Seller Commission, Closing Costs to Sell as a percentage of ARV

**Outputs** — 75% rule verdict, Total Costs, Net Profit and ROI, plus a print/export view for
sharing with a client or partner.


**Wholesale mode** — Toggle Flip / Wholesale. Wholesale shows Buyer MAO, Offer to Seller,
assignment fee as % of ARV, and end-buyer profit guidance.

**Share Link / Export PDF** — Copy a read-only share URL that restores the deal numbers, or
export a cleaner print/PDF report for clients and buyers.

## Running it locally

No build step, no dependencies, no server. Clone the repo and open `index.html` in any browser:

```bash
git clone https://github.com/pintorjosere-prog/Flip-Logic.git
cd Flip-Logic
start index.html
```

Everything runs in the browser. Deal numbers stay on your device unless you copy a Share Link
(which encodes the inputs in the URL for the recipient). The only outbound request the page
makes on its own is to Google Fonts for typography.

## Notes

Estimates are for analysis only and are not a lender quote, an appraisal, or investment advice.
Confirm every figure with your lender, contractor and title company before making an offer.
