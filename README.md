# AeroKing Help Centre

End-user documentation for the AeroKing Aviation platform, built with
[MkDocs Material](https://squidfunk.github.io/mkdocs-material/).

This is **customer- and staff-facing help documentation** — plain-English guides,
role manuals, walkthroughs and FAQs. It is deliberately kept separate from the
developer docs that live inside each product repo (`aeroking-dashboard/documentation/`,
`aeroking-warehouse/docs/`, etc.).

## What's inside

| Section | Folder | Status |
|---------|--------|--------|
| Dashboard (flying-school management) | `docs/dashboard/` | ✅ Live |
| Planner | `docs/planner/` | 🚧 Placeholder — product in planning |
| Warehouse (CMMS / inventory) | `docs/warehouse/` | 🚧 Placeholder — product in planning |

## Running the docs locally

Requires Python 3.9+.

```bash
pip install -r requirements.txt
mkdocs serve          # live preview at http://127.0.0.1:8000
```

To produce a static site for hosting:

```bash
mkdocs build          # output in ./site
```

## Adding a new product or role

The site is structured so a new product is a new top-level tab and a new role is a
new Markdown file — no code changes. Copy-paste templates live in `docs/_templates/`.

## Structure

```
aeroking-docs/
├── mkdocs.yml                    # site config + navigation (the one place nav lives)
├── requirements.txt
└── docs/
    ├── index.md                  # help-centre landing / product picker
    ├── getting-started.md        # login, navigation, settings — shared by every product
    ├── dashboard/
    │   ├── overview.md           # what the dashboard is + core concepts
    │   ├── roles/                # one manual per role (+ capability matrix index)
    │   ├── reference/            # capabilities catalogue, glossary
    │   └── faq.md
    ├── planner/                  # future product (placeholder)
    ├── warehouse/                # future product (placeholder)
    ├── contributing.md           # how to expand these docs
    └── _templates/               # copy-paste skeletons for new roles / products
```
