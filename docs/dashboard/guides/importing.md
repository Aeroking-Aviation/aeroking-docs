# Importing your data

Bring an existing school across — members, aircraft, bookings, billing, logbook and training —
in one guided import. Find it at **Import** (admin Overview tile; needs `users.manage` and the
school's **imports-enabled** switch). **Committing** an import is **owner-only**; anyone with
access can run a dry-run preview.

## The format

AeroKing uses one format, **AeroKing Data (AK_D)**. You can provide it two ways:

- **Spreadsheet (.xlsx):** download the **template** from the Import page — one tab per thing
  (members, aircraft, bookings, invoices, transactions, logbook, training) with an instructions
  tab. Fill in what you have; leave a tab blank to skip it.
- **Bundle (.zip):** the per-entity JSON plus a `files/` folder — use this when you also need
  to bring **documents** (medicals, ARCs) across, which a spreadsheet can't carry.

!!! note "Linking records"
    Use your **old system's id** (`legacy_id`) on each row, and reference other records by their
    natural key — member **email**, aircraft **registration**, invoice **number**. Never invent
    AeroKing ids. This also makes re-running an import safe (it updates, never duplicates).

## Run it

1. Open **Import** and upload your `.xlsx` or `.zip`.
2. It runs a **dry-run preview** first — a summary plus per-entity counts and any
   errors/unresolved references. **Nothing is saved yet.**
3. Check the preview, fix your file if needed, and re-upload.
4. When it looks right, the **owner** confirms to commit.

## What comes across

Imported in dependency order: **members → aircraft → invoices → transactions → bookings →
logbook → training** (enrolments + assessments), and **documents** from a bundle. Account
balances are recomputed from the imported transactions.

!!! info "Set up first / brought separately"
    **Courses** are set up in-app before importing (training enrolments attach to them).
    **Handling/PPR** has its own importer under Handling. Talk to AeroKing about your first
    migration — we'll do it with you.
