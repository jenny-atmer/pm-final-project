# A/B Experiment Brief, Riverty business-unit case

## Parameters
| Parameter | Decision |
|---|---|
| Feature under test | Pay-after-you-decide invoice (Major Project): the only thing that makes this more than a Riverty-branded debit card, |
| Persona | Lena, 32, Cologne: a salaried, phone-first shopper on a middling income with no financial cushion, who uses BNPL on most non-trivial purchases and takes whichever option appears at checkout. |
| Expected outcome | Expected behaviour change: Lena stops taking whichever BNPL option appears at checkout and starts reaching for the Riverty card first, online and in store, for the purchases where she wants to decide before she pays. On payday she checks one Riverty view for her card spend, instead of rebuilding it across apps. |
| Primary success metric | Lena uses a Riverty card for purchases where she wants to decide before she pays, including at merchants and shops that don't offer Riverty today, so Riverty becomes something she carries, not a button that may appear. |
| Baseline rate | Scale if activation reaches the brief's modeled 70% or higher, the repeat-use target above is met, and the guardrail holds. Pivot if activation is fine but repeat use is weak. That would mean users like the card but it isn't winning the everyday purchase. Kill if activation falls below about 50%, or if the volume cannibalized from integrated checkout costs more margin than the card earns. |
| Guardrail metric | Riverty checkout transactions at partner merchants. Track them among card holders against a comparable group of non-holders, and they must not fall once someone gets the card. This is the product signal that the card is adding to the merchant-first model, not replacing it. |
| Guardrail boundary | · |
| Second guardrail | · |
| Minimum Detectable Effect | 2 percentage points absolute |
| Sample size per arm | 4,144 |
| Traffic split | 50/50 |
| Test duration | 14 days |
| Significance threshold | < 0.05 |

## Control vs. Variant
- **Control (A):** Riverty is only available where a partner merchant offers it, so Lena can't pay later everywhere, and she has no reason to prefer Riverty when Klarna and PayPal are already on her phone.
- **Variant (B):** Screen 1: Entry point (Card home)

Header with the Riverty virtual card visual (Mastercard mark, last four digits).
Remaining limit: “€X von €500” with a progress bar (€500 is a synthetic demo value, not a Risk-approved limit).
Prototype-only panel labelled “Demo controls”: merchant dropdown with 3 fictional non-partner shops, an amount field, and a “Simulate purchase” button.
“Open invoices” list (empty state: “No open invoices”). Each row has a merchant, amount and due date, and taps through to Screen 2.
Inline error for over-limit purchases.

Screen 2: Feature core (Invoice detail)

Merchant, purchase date, amount.
Status chip: Open / Paused / Refunded.
Due date with days remaining, or “Paused” in place of the countdown.
“Leaves your account today: €0,00” line.
Legal copy block, visibly marked [Placeholder, pending Legal], covering the due date, fees and consequences of missing payment.
Primary button “Report return”. After the report it becomes disabled and reads “Return reported”.
Secondary link “Cancel return report”, which restores the original due date.
Demo control “Simulate merchant refund”, with a full/partial toggle (partial is a Should).
Not built: “Pay now” (Should).

Screen 3: Success / confirmation (Refund confirmed)

Check icon and the headline “Your invoice was updated”.
Old amount crossed out, new amount (or €0,00), status “Cancelled” or “Reduced”.
“Amount that left your account: €0,00”.
“Limit restored: +€X” with the new remaining limit.
“Back to card” button, returning to Screen 1 with the list and limit updated.
- **Held constant (isolation check):** app version

## Hypothesis
> I believe that Pay-after-you-decide invoice (Major Project): the only thing that makes this more than a Riverty-branded debit card, for Lena, 32, Cologne: a salaried, phone-first shopper on a middling income with no financial cushion, who uses BNPL on most non-trivial purchases and takes whichever option appears at checkout. will result in Expected behaviour change: Lena stops taking whichever BNPL option appears at checkout and starts reaching for the Riverty card first, online and in store, for the purchases where she wants to decide before she pays. On payday she checks one Riverty view for her card spend, instead of rebuilding it across apps., as measured by a 2 percentage points absolute change in Lena uses a Riverty card for purchases where she wants to decide before she pays, including at merchants and shops that don't offer Riverty today, so Riverty becomes something she carries, not a button that may appear. within 14 days. We will protect Riverty checkout transactions at partner merchants. Track them among card holders against a comparable group of non-holders, and they must not fall once someone gets the card. This is the product signal that the card is adding to the merchant-first model, not replacing it. throughout the test.

## Shipping criteria
> We will **ship** if Lena uses a Riverty card for purchases where she wants to decide before she pays, including at merchants and shops that don't offer Riverty today, so Riverty becomes something she carries, not a button that may appear. improves by ≥ 2 percentage points absolute at < 0.05 and Riverty checkout transactions at partner merchants. Track them among card holders against a comparable group of non-holders, and they must not fall once someone gets the card. This is the product signal that the card is adding to the merchant-first model, not replacing it. does not reach _(not filled in)_ after 14 days.
> We will **iterate** if direction is positive but lift is below the MDE.
> We will **kill** if the primary metric shows no improvement or moves negatively.
> The read date is fixed at the end of 14 days, no results reviewed before this date.
