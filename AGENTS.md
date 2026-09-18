# Documentation project instructions

## About this project

- This is a documentation site built on [Mintlify](https://mintlify.com)
- Pages are MDX files with YAML frontmatter
- Configuration lives in `docs.json`
- Run `mint dev` to preview locally
- Run `mint broken-links` to check links

## Terminology

- "Coverbase", never "CoverBase". "Organization" and US spelling throughout.
- "Vendor" is the default term; orgs can rename it, so never build a claim on the label.
- "Finding" is the vendor-side problem; "obligation" is what your organization owes; "commitment" is a promise attached to either.
- "Signal" is one Radar event as it affects the organization; "alert" is one detector's verdict on it.
- "User guide" for a how-to page, "product page" for a `products/` page, "reference" for fields, placeholders and the control library.

## Style preferences

- **Never use an em dash (`—`).** Rewrite as two sentences, or use a comma, a
  colon, or parentheses. Keep other dashes rare too. The `Prose` workflow in
  `.github/workflows/prose.yml` fails any PR that adds one, with no exemptions.
- No dramatic or self-important phrasing. Say what the screen does and what
  happens if the reader gets it wrong. Cut sentences whose job is to sound
  weighty: "the part an auditor reads", "the moment the signature is committed",
  "what makes the record worth something". A sentence that survives losing its
  flourish did not need it.
- Use active voice and second person ("you")
- Keep sentences concise: one idea per sentence
- Use sentence case for headings
- Bold for UI elements: Click **Settings**
- Code formatting for file names, commands, paths, and code references

## Field reference pages

`fields/overview.mdx` and `fields/catalog.mdx` are maintained by hand, but their
content mirrors the platform rather than being free prose. The catalog's rows come
from the filterable field registries in the IRM repo
(`common/common/schema/filterable/`), and the labels come from the dashboard's
matching label tables (`dashboard/src/common/filter-labels/`), which are what the
product actually renders in the **Add filter** menu.

When editing:

- Keep a field's **Filter path** exactly as the registry spells it. It is the
  identifier customers put in saved views, workflow conditions, and API calls, so a
  typo here is a broken integration, not a typo.
- Keep the **Field** label matching the dashboard label table, and the **Group**
  matching that field's submenu.
- Use default Coverbase terminology for labels. Workspaces can rename core terms,
  and the overview page already explains that labels vary while paths do not.
- Add or remove rows when fields are added or removed from a registry. The per-module
  field counts in the catalog need updating alongside.

## Content boundaries

- Document what the product does today, from the product source. Do not describe a feature that is not shipped or that lives only in seed data.
- Do not document Coverbase-staff tooling (the `radar_admin` and `internal/` routes, gates, fork environments, the alert purge).
- Do not name customers.
- Heading text on a published page is a URL anchor customers may already hold. Add headings freely; rename one only on purpose.
- Screenshots come from the demo workspace, never from a customer's.

## User guide structure

Every guide under `user-guides/` opens with the `AgentDirective` snippet and an `<Info>` banner naming its neighbours, states in one sentence the mistake people most often make, and ends with a `## Troubleshooting` table and a `## Related` card group. Groups in `docs.json` mirror the product's left navigation, and `user-guides/overview.mdx` is the directory: a new guide needs a card, a row in the complete directory table, and a row in the lookup table.
