# Contributing to the documentation

## Two ways to make a change

**On GitHub.** Open the page, click the pencil icon, edit, and open a pull request.

**Locally.**

1. Clone the repository and install the Mintlify CLI: `npm i -g mint`.
2. Create a branch.
3. Run `mint dev` at the repository root and preview at `http://localhost:3000`.
4. Run `mint broken-links` before you push.
5. Open a pull request. The `Prose` workflow fails the PR if it adds an em dash.

## Adding a user guide

1. Create `user-guides/<slug>.mdx` with `title`, `description` and `icon` in the frontmatter.
2. Open with the `AgentDirective` snippet and an `<Info>` banner that says the page is part of the User Guides collection and names its neighbours.
3. Add the page to the matching group in `docs.json`. Groups mirror the product's left navigation.
4. Add a card for it in `user-guides/overview.mdx`, plus a row in the directory table and, if it answers a common question, a row in the lookup table.
5. Add screenshots under `images/user-guides/`, named after the guide.
6. End with a `## Troubleshooting` table and a `## Related` card group.

## Writing guidelines

- Active voice, second person, one idea per sentence.
- Lead with the goal, then the click path.
- Use the product's real labels, in bold.
- Keep information; cut flourish.
- Never rename a heading on a published page without a reason. Headings are URL anchors.

The complete style rules are in `AGENTS.md`.
