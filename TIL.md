# Today I Learned (TIL)

Domain knowledge, regulatory nuances, and technical constraints captured while researching and building `war-chest`.

---

## Firearms Compliance & Legal Nuances

- **Type 03 (C&R) vs. Type 01 FFL:** A Type 03 Curio & Relic license is strictly for collecting and cannot be used to operate a firearms dealing business. Dealing requires a Type 01 FFL (plus Class 3 SOT status to deal in National Firearms Act items). See [`Compliance/Compliance Overview.md`](./Compliance/Compliance%20Overview.md).
- **Wartime "Bring-Back" Papers Do Not Legalize Unregistered Machine Guns:** Period capture papers are valuable provenance evidence, but an unregistered NFA machine gun cannot be legally sold or transferred regardless of family history or wartime paperwork. See [`Inventory/Provenance and Authentication.md`](./Inventory/Provenance%20and%20Authentication.md).
- **Deactivated Machine Guns Often Remain NFA Items:** Unless a machine gun receiver has been completely destroyed according to ATF specifications, a "deactivated" or welded firearm may still be legally classified as a machine gun under federal law.
- **US Military Decorations:** Federal law restricts the sale of certain US military medals and decorations (such as the Medal of Honor). Always verify before listing medals under [`Inventory/Item Categories.md`](./Inventory/Item%20Categories.md).

## Operational Security & Cataloging

- **Why Public Serial Numbers Are Redacted:** Publishing full serial numbers on public listings makes it easier for bad actors to forge provenance paperwork or falsify ownership claims. Only partial numbers should ever appear publicly, with stock numbers used in internal notes. See [`Compliance/Listing Rules.md`](./Compliance/Listing%20Rules.md) and [`Inventory/Cataloging Standard.md`](./Inventory/Cataloging%20Standard.md).
- **Provenance Confidence Tiers:** Using strict vocabulary (`Documented`, `Attributed`, `Family history`, `Unknown`) protects both the collector and the dealer from reputation damage and legal liability over unverified family stories.

## Platform & Technical Constraints

- **Deplatforming & Payment Freezes:** Mainstream processors (Stripe, PayPal, Square) and ad networks (Google, Meta) prohibit firearm sales and promotion. Architecture must rely on static generation, portable hosting with written acceptable-use approval, off-host backups, and invoice/wire or firearms-friendly merchant accounts. See [`Compliance/Platform Restrictions.md`](./Compliance/Platform%20Restrictions.md) and [`Website/Tech and Payments.md`](./Website/Tech%20and%20Payments.md).
- **Accessible Spam Prevention:** Visual CAPTCHAs violate screen-reader usability goals under WCAG 2.2 AA. Enquiry forms must use non-visual spam protection alongside full keyboard and screen-reader support. See [`Website/Accessibility Standard.md`](./Website/Accessibility%20Standard.md).
