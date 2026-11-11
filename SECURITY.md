# Security & Confidentiality Policy

This policy summarizes the security, privacy, and operational safeguards defined in [`Compliance/Confidentiality Standard.md`](./Compliance/Confidentiality%20Standard.md), [`Compliance/Listing Rules.md`](./Compliance/Listing%20Rules.md), and [`Website/Tech and Payments.md`](./Website/Tech%20and%20Payments.md).

## Data Classification

Every piece of project information belongs to one of four tiers. When in doubt, treat data as the higher tier:

1. **Public:** Approved item listings, published articles, and the live website.
2. **Internal:** Working plans, drafts, and notes containing no client secrets. Permitted in this private repository.
3. **Confidential:** Unannounced client identity, unpublished inventory, acquisition costs, consignor and buyer identities, and project quotes. Shared only under a signed agreement ([`Templates/Mutual NDA Template.md`](./Templates/Mutual%20NDA%20Template.md), [`Templates/Contractor Confidentiality Template.md`](./Templates/Contractor%20Confidentiality%20Template.md), or [`Templates/Consignor Confidentiality Template.md`](./Templates/Consignor%20Confidentiality%20Template.md)).
4. **Restricted (NEVER stored in this repository or on the public website):**
   - Full firearm serial numbers
   - Federal Firearms License (FFL) or Special Occupational Tax (SOT) copies
   - Firearm transfer records (e.g., ATF Form 4473, NFA registration documents)
   - Buyer or consignor government identity documents
   - Physical collection storage locations, vault details, and security equipment
   - Passwords, API keys, and private credentials

## Mandatory Repository & Asset Rules

- **Private Repository Only:** This repository must never be made public.
- **No Credentials in Git:** Store all credentials in a password manager and local environment variables (see [`.env.example`](./.env.example)), never in tracked files.
- **Stock Numbers Over Serial Numbers:** Reference inventory using internal stock numbers (e.g., `A1042`) in notes and filenames.
- **Image Sanitization:** Before committing or publishing any photograph:
  1. Blur or crop out full serial numbers.
  2. Ensure no storage area locks, safes, alarms, or physical addresses appear in the frame.
  3. Strip all EXIF/GPS metadata so location coordinates are never leaked.
- **Third-Party & AI Tools:** Do not paste Confidential or Restricted client material into external services or AI tools without the client's prior written consent.
- **Two-Factor Authentication:** Require 2FA on all Git, hosting, DNS, CMS, and email accounts associated with the project.

## Incident & Leak Response

If Confidential or Restricted information is exposed or suspected to be exposed:

1. **Contain:** Immediately revoke affected credentials, access tokens, or public links and remove the exposed material.
2. **Document:** Record what information was exposed, when the exposure occurred, how it was discovered, and who is affected.
3. **Notify:** Inform the client promptly in accordance with the signed confidentiality agreement.
4. **Legal Escalation:** Consult legal counsel to determine whether regulatory or statutory breach notifications are required.
