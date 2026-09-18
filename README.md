# Coverbase documentation

Source for [docs.coverbase.com](https://docs.coverbase.com), built on [Mintlify](https://mintlify.com). Pages are MDX files with YAML frontmatter; `docs.json` holds the navigation and site settings.

## What lives where

| Path | Content |
| --- | --- |
| `index.mdx` | The home page |
| `products/` | One page per product capability, grouped under **Get started** |
| `user-guides/` | Screen-by-screen guides, grouped the way the product's left navigation is grouped. `user-guides/overview.mdx` is the directory |
| `user-guides/supplier-countries/` | The generated country reference. Regenerated from the IRM repo; do not edit by hand |
| `reporting/` | Word report templates, placeholders, and the due-diligence file |
| `api-reference/`, `export*.mdx`, `import*.mdx`, `quickstart.mdx`, `conventions.mdx`, `changelog.mdx` | The developer surface |
| `fields/` | The filterable field catalog |
| `integrations/` | Integration patterns and platform-specific guides |
| `mcp/` | The MCP server |
| `security/` | Trust and security pages |
| `images/user-guides/` | Screenshots, taken from a demo workspace |
| `snippets/` | Shared MDX fragments |

## Working locally

```bash
npm i -g mint
mint dev            # preview at http://localhost:3000
mint broken-links   # check internal links
```

Pushes to the default branch deploy automatically through the Mintlify GitHub app.

## House style

The rules every page follows are in `AGENTS.md`: no em dashes (CI fails the PR), no dramatic phrasing, active voice, sentence-case headings, bold for UI labels. Heading text is a URL anchor that may already be in a customer's inbox, so rename a heading only with a redirect or a deliberate decision.

## Screenshots

Screenshots are 1440 by 900 captures of the running app against the demo workspace, saved as PNG under `images/user-guides/` and embedded with `<Frame caption="...">`. Name a file after the guide it belongs to (`findings-and-remediation-list.png`) so a re-shoot is easy to find.
