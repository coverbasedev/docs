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

## Generated pages

`fields/overview.mdx` and `fields/catalog.mdx` are generated. Do not edit them by
hand — the next regeneration overwrites the change. They are produced from the
IRM repo's filterable field registries and dashboard label tables by
`common/scripts/generate_field_reference.py`:

```bash
uv run common/scripts/generate_field_reference.py --out-dir <path-to-docs>/fields
```

Prose changes belong in the `OVERVIEW` and `CATALOG_HEADER` constants in that
script; field rows follow the registries and cannot be edited here at all.

## Content boundaries

{/* Define what should and shouldn't be documented */}
{/* Example: Don't document internal admin features */}
