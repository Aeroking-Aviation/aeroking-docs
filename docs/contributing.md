# Contributing to these docs

These docs are designed to grow. This page shows how to add a **new role** or a whole **new
product** without touching any application code — just Markdown and one navigation file.

## The two things you ever edit

1. **Markdown files** in `docs/` — the content.
2. **`mkdocs.yml`** → the `nav:` block — the single place the sidebar/tabs are defined.

Preview your changes live at any time:

```bash
mkdocs serve        # http://127.0.0.1:8000, auto-reloads on save
```

## Writing style

Keep it for **end users**, not developers:

- Lead with the task ("Request a lesson"), then the numbered steps.
- Use **admonitions** for asides — `!!! note`, `!!! tip`, `!!! warning`, `!!! info`.
- Use `??? question` for collapsible FAQ entries.
- Use `=== "Tab"` blocks to compare variants (e.g. roles) side by side.
- Describe what the user **sees and clicks**, not database tables or endpoints.
- Cross-link generously with relative links so people can hop between manuals.

The existing [Dashboard](dashboard/overview.md) section is the reference for tone and depth.

## Add a new role

Say a new **"Dispatcher"** role appears in the Dashboard.

1. Copy the template:
   ```bash
   cp docs/_templates/role-manual.md docs/dashboard/roles/dispatcher.md
   ```
2. Fill in the menu table and walkthroughs (check the app's nav and capabilities for what
   the role actually sees — see the note below).
3. Add it to `mkdocs.yml` under the Dashboard → Role manuals list:
   ```yaml
   - Dispatcher: dashboard/roles/dispatcher.md
   ```
4. Add a row to the role matrix in `docs/dashboard/roles/index.md` and the capability
   defaults in `docs/dashboard/reference/capabilities.md`.
5. `mkdocs serve` and check it.

!!! tip "Where the role facts live in the app"
    A role's real menu is defined in the dashboard frontend at
    `frontend/src/components/layout/TopNav.jsx` (the `NAV_LINKS` map), and its default
    capabilities in `backend/src/db/migrate.js` (`DEFAULT_PRESETS`). Mirror those so the
    docs match what users actually see.

## Add a new product

Say **Planner** or **Warehouse** is ready to document.

1. Create the folder and starter pages (copy the whole template set):
   ```bash
   cp -r docs/_templates/product docs/planner   # already exists as a placeholder — merge
   ```
   At minimum you want an `overview.md`, a `roles/` folder and a `faq.md`, matching the
   Dashboard shape.
2. Expand that product's section in `mkdocs.yml` → `nav:`. Because
   `navigation.tabs` is enabled, each top-level entry is a tab, so the product already has
   its own tab:
   ```yaml
   - Planner:
       - planner/overview.md
       - Role manuals:
           - planner/roles/index.md
           - Some Role: planner/roles/some-role.md
       - FAQ: planner/faq.md
   ```
3. Update the product cards on the **[home page](index.md)** (`docs/index.md`) — change the
   status from "in planning" to a link into the new section.
4. `mkdocs serve` and review.

That's it — a new product is a new top-level `nav:` entry plus a folder of Markdown.

## Templates

Copy-paste skeletons live in `docs/_templates/`:

- `role-manual.md` — a single role manual.
- `product-overview.md` — a product's overview/landing page.
- `faq.md` — a FAQ page with example collapsible entries.

!!! note "`_templates` is excluded from the built site"
    The folder isn't in `nav:`, so it won't appear in the sidebar. MkDocs may log a harmless
    "not included in nav" warning for these files — that's expected.

## Publishing

`mkdocs build` produces a static site in `./site/` that can be hosted anywhere (e.g.
GitHub Pages, Netlify, an internal web server). Set `site_url` in `mkdocs.yml` to the final
address first so links and the sitemap are correct.
