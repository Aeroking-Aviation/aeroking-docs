# Fleet & maintenance

The **Fleet** is your aircraft register; each aircraft has its own page with a maintenance hub.
Managing the fleet needs `aircraft.manage`; maintenance work needs the `maintenance.*`
capabilities.

## The register

Aircraft are grouped by status — **Available**, **In maintenance**, **Grounded (AOG)**. Tap a
status tile to filter; a **Need attention** tile flags checks due soon or overdue.

- **Add** an aircraft with its registration (plus make/model if known). Removing one keeps its
  logbook and history — re-adding the same registration restores it.
- The counter by **Add Aircraft** shows how many of your plan's **aircraft allowance** you're
  using (see [Your plan & licence](licence.md)).

## An aircraft's page

Everything for one aircraft lives here: **Overview**, **Maintenance**, **Mass & Balance**,
**Logbook**, **Documents**, **Activity**. An **airworthiness banner** at the top summarises
anything outstanding.

### The Maintenance hub

One **Maintenance** tab with sub-tabs:

- **Schedule & certs** — service countdown and certificate expiries (ARC, insurance,
  transponder, pitot-static).
- **Defects & ADs** — open defects and airworthiness directives.
- **Lifed parts** — components tracked to a life.
- **History** — what's been done.

### Lifed parts

Each part is tracked on one of two bases:

- **Time-based (hard life)** — replaced/overhauled at a fixed limit (date and/or hours); goes
  amber near the limit, red once overdue.
- **On condition** — inspected at intervals, stays in service while it passes; never goes
  overdue, just amber when the next inspection is due.

"Remaining" is worked out for you from the last action plus the interval.

## Hours & grounding

- Hours are tracked as **brakes off/on** (block time, used for billing), plus **airframe** and
  **engine** meters (used for maintenance countdowns). Saved flights advance the meters
  automatically.
- **Grounding** an aircraft asks for a reason and is date-bounded; a grounded or in-maintenance
  aircraft is hidden from the booking calendar.
