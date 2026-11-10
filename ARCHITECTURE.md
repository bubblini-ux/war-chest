# Architecture

This document describes both the current **Knowledge Vault Architecture** and the planned **Website & Catalog Architecture** defined in [`Website/Site Plan.md`](./Website/Site%20Plan.md) and [`Website/Tech and Payments.md`](./Website/Tech%20and%20Payments.md).

## 1. Knowledge Vault Architecture

The repository is structured as an interconnected Markdown / Obsidian vault anchored at [`Home.md`](./Home.md).

```
war-chest/
├── Home.md                     # Vault index and navigation hub
├── Client/                     # Discovery, client profile, and task tracking
├── Compliance/                 # Legal guardrails, listing rules, platform policies, data classification
├── Inventory/                  # Taxonomy, cataloging standards, and provenance criteria
├── Operations/                 # Enquiry, FFL verification, and transfer workflows
├── Website/                    # Information architecture, stack requirements, WCAG 2.2 AA standards
├── Marketing/                  # Editorial voice, organic channels, and article concepts
└── Templates/                  # Item, provenance, meeting, and legal agreement templates
```

### Frontmatter & Linking Conventions

- **YAML Frontmatter:** Every vault note includes frontmatter with `tags` and `status` (`draft`, `active`, `needs-attorney-review`, `verify-before-use`, or `intake`).
- **Wikilinks:** Internal cross-references use Obsidian `[[Note Name]]` links, with each child note linking back to `[[Home]]`.
- **Legal Gatekeeping:** Any document tagged `status: needs-attorney-review` cannot be treated as final operational policy until reviewed by the client's firearms counsel.

## 2. Target Website Architecture

Per [`Website/Tech and Payments.md`](./Website/Tech%20and%20Payments.md), the public website is designed for portability, resilience against deplatforming, and strict separation between public and restricted data.

### Core Principles

1. **Static Site Generation (SSG):** Pages are built from a structured catalog into static assets so the site is fast, secure, inexpensive to run, and trivial to redeploy if a hosting provider changes its acceptable use policy.
2. **Enquiry-First Flow (No Instant Checkout):** High-value and regulated items (especially National Firearms Act items) use a structured enquiry workflow that captures the item stock number and the prospective buyer's state of residence before any payment or transfer steps occur.
3. **Strict Data Boundary:**
   - **Public Website:** Approved descriptions, partial/redacted serial numbers, metadata-stripped photographs with detailed alt text, documented provenance summaries, and plain-language transfer requirements.
   - **Client's Offline/Private Records:** Full serial numbers, acquisition costs, consignor identities, FFL/SOT copies, ATF forms, Form 4473 records, and buyer identity documents never touch the public web server.
4. **Accessibility by Default:** Every template targets **WCAG 2.2 Level AA** ([`Website/Accessibility Standard.md`](./Website/Accessibility%20Standard.md)), including full keyboard navigation, screen-reader announcements for collection filters, and non-visual spam protection on forms.
5. **Vendor Portability:** Domain registration and DNS stay in the client's own name, and off-host backups of both the site and mailing list are maintained continuously ([`Compliance/Platform Restrictions.md`](./Compliance/Platform%20Restrictions.md)).
