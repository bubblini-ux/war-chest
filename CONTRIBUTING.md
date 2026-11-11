# Contributing to War Chest

All team members and contractors must sign [`Templates/Contractor Confidentiality Template.md`](./Templates/Contractor%20Confidentiality%20Template.md) and read [`Compliance/Confidentiality Standard.md`](./Compliance/Confidentiality%20Standard.md) before accessing client material or contributing to this repository.

## 1. Non-Negotiable Rules

1. **Never commit Restricted data:** Do not include full firearm serial numbers, licence numbers/scans, transfer forms, identity documents, storage locations, or credentials in any commit, branch, or pull request.
2. **Do not assume unknown facts:** Anything not yet confirmed by the client or their firearms attorney must be marked `To confirm` or tagged `status: needs-attorney-review`.
3. **Evidence-backed claims only:** Follow the terminology in [`Inventory/Provenance and Authentication.md`](./Inventory/Provenance%20and%20Authentication.md) (`Documented`, `Attributed`, `Family history`, `Unknown`). Never overstate an item's history.
4. **Follow Brand and Voice:** Keep all copy knowledgeable, plain, calm, and historical per [`Marketing/Brand and Voice.md`](./Marketing/Brand%20and%20Voice.md) and [`Compliance/Listing Rules.md`](./Compliance/Listing%20Rules.md).

## 2. Vault Note Standards

- **YAML Frontmatter:** Every Markdown note in the vault must start with valid YAML frontmatter containing at least `tags` and `status`:
  ```yaml
  ---
  tags: [category]
  status: draft
  ---
  ```
- **Navigation:** Include `Back to [[Home]].` immediately below the H1 heading on vault reference notes, and link new notes from [`Home.md`](./Home.md).
- **Formatting:** Follow [`.editorconfig`](./.editorconfig) (UTF-8, LF line endings, 2-space indentation, final newline).

## 3. Adding or Updating Inventory Notes

When creating an item record from [`Templates/Item Template.md`](./Templates/Item%20Template.md):

1. Name files using year, nation, model, and stock number (e.g., `1943 US M1 Garand A1042`).
2. Complete a matching [`Templates/Provenance Record Template.md`](./Templates/Provenance%20Record%20Template.md).
3. Verify that all public descriptions state legal status, buying requirements, and shipping restrictions in plain words.
4. Confirm that full serial numbers are hidden in text and images, EXIF/GPS metadata is stripped from photos, and descriptive alt text is written per [`Website/Accessibility Standard.md`](./Website/Accessibility%20Standard.md).

## 4. Pull Request Process

- Open a branch for your changes and use [`PULL_REQUEST_TEMPLATE.md`](./PULL_REQUEST_TEMPLATE.md) when submitting a pull request.
- Any change affecting [`Compliance/`](./Compliance/), [`Operations/Sale Workflow.md`](./Operations/Sale%20Workflow.md), or legal templates in [`Templates/`](./Templates/) must retain `status: needs-attorney-review` until cleared in writing by counsel.
