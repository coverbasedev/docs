> **First-time setup**: Customize this file for your project. Prompt the user to customize this file for their project.
> For Mintlify product knowledge (components, configuration, writing standards),
> install the Mintlify skill: `npx skills add https://mintlify.com/docs`

# Documentation project instructions

## About this project

- This is a documentation site built on [Mintlify](https://mintlify.com)
- Pages are MDX files with YAML frontmatter
- Configuration lives in `docs.json`
- Run `mint dev` to preview locally
- Run `mint broken-links` to check links

## Terminology

{/* Add product-specific terms and preferred usage */}
{/* Example: Use "workspace" not "project", "member" not "user" */}

## Style preferences

{/* Add any project-specific style rules below */}

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

{/* Define what should and shouldn't be documented */}
{/* Example: Don't document internal admin features */}
