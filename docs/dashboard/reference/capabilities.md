# Capabilities & permissions

AeroKing controls access with **capabilities** — small, specific permissions such as "view
the calendar" or "create invoices". Your **role** comes with a default set, and an owner or
an administrator holding *permissions.manage* can grant or remove individual capabilities —
either for a whole role or for one person.

This page is a reference for administrators and owners. Everyday users don't need it, but
it explains exactly why you can (or can't) see a given area.

!!! info "How access is decided"
    1. Start with the defaults for your **role** (or, for flying members, your **rank** —
       each rung inherits the ones below it).
    2. Apply any **school-wide** changes the owner made to those defaults.
    3. Apply any **per-person** grants or removals.

    The result is your effective set of capabilities. The **owner always has every
    capability.**

## Capability catalogue

Capabilities are grouped by area. Most areas have a **view** level and a **manage** level
(view = see it, manage = change it).

| Capability | What it allows |
|------------|----------------|
| `aircraft.view` | View the aircraft fleet list |
| `aircraft.manage` | Edit aircraft details & the fleet |
| `maintenance.view` / `maintenance.manage` | View / manage maintenance records |
| `logbook.view` / `logbook.manage` | View / manage the aircraft logbook |
| `users.view` | View members & user records |
| `users.manage` | Create/edit users & assign roles |
| `calendar.view` | View the booking calendar |
| `calendar.manage` | Create/edit any booking |
| `invoicing.view` / `invoicing.manage` | View / create & edit invoices |
| `accounts.view` / `accounts.manage` | View / manage member accounts |
| `vouchers.view` / `vouchers.manage` | View / create & redeem vouchers |
| `training.view` | Access training material |
| `training.manage` | Build courses, lessons & learning materials |
| `grading.submit` | Submit exam / assessment scores |
| `grading.manage` | Conduct exams / manage assessments |
| `ppr.view` / `ppr.manage` | View / manage PPR requests, spots & rate card *(add-on)* |
| `documents.view` / `documents.manage` | View & download / upload, verify & delete documents |
| `forms.view` / `forms.manage` | View / build digital form templates |
| `hr.view` | Self-service leave, permits & policies |
| `hr.manage` | Approve leave & administer HR |
| `compliance.view` / `compliance.manage` | View / build the compliance programme |
| `reports.view` | View dashboards, overview & reports |
| `settings.manage` | Edit school settings |
| `permissions.manage` | Edit roles & access permissions |
| `plugins.view` / `plugins.manage` | Use / enable & configure add-ons |
| `bookings.request` | Request a booking (held by flying members) |
| `lesson_summaries.view` / `lesson_summaries.comment` | View / comment on lesson summaries |

## Default capabilities by role

These are the **platform defaults**. Your school may have adjusted them.

=== "Administrator"

    Members, calendar, invoicing & accounts, vouchers, aircraft (view), training (build),
    PPR, documents, forms, HR (view **and** manage), compliance (view **and** manage) and
    reports. **Not** grading by default (can be granted).

=== "Staff"

    Calendar (view & manage), PPR (view & manage), documents (view & manage), forms (view),
    HR self-service and compliance (view). **No finance** by default — an owner typically
    extends this for a front desk that takes payments.

=== "Engineer"

    Aircraft (view & manage), maintenance (view & manage), aircraft logbook (view & manage),
    HR self-service and compliance (view). Operational areas like calendar/members/finance
    are granted as needed.

=== "Instructor (qualified)"

    Builds up the ladder: calendar (view → manage), **grading.submit**, HR self-service,
    compliance (view), documents (view) and forms (view).

=== "Student"

    Training (view), request bookings, and view/comment on their own lesson summaries.

=== "Social"

    Training (view) only — a non-flying club membership.

## The membership rank ladder

Flying members hold a **rank**, and each rank inherits everything below it:

```
student → qualified_pilot → trainee_instructor → qualified_instructor → examiner
```

| Rank | Adds on top of the rank below |
|------|-------------------------------|
| `student` | Training view, request bookings, own lesson summaries |
| `qualified_pilot` | (rents aircraft — inherits student access, used without the training pages) |
| `trainee_instructor` | Calendar view, **grading.submit**, HR & compliance self-service, documents & forms view |
| `qualified_instructor` | Calendar **manage** |
| `examiner` | **grading.manage** (conduct exams) |

**Social** sits outside the ladder and doesn't accumulate.

## Changing permissions (administrators)

Go to **Settings → Permissions**:

- **Change a role preset** to adjust the default for everyone in that role or rank.
- **Open an individual** to grant or remove specific capabilities for just that person —
  these per-person overrides win over the preset.

!!! tip "Least surprise"
    Prefer adjusting the **preset** when a change should apply to everyone in a role, and
    **per-person overrides** only for genuine exceptions. It keeps the model easy to reason
    about later.

!!! note "Add-ons still gate their pages"
    Even with `ppr.manage`, the Handling pages only appear if the **Handling/PPR add-on** is
    enabled for the school. Add-ons and capabilities both have to line up.

---

**Related:** [Overview — core concepts](../overview.md#core-concepts) ·
[Role matrix](../roles/index.md) · [Administrator manual](../roles/admin.md)
