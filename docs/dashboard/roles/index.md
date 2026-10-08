# Role manuals

Each role below has its own manual with features and step-by-step walkthroughs. Open the
one that matches you. If your menu doesn't match your manual exactly, it's because an
administrator has adjusted your [capabilities](../reference/capabilities.md) — the extra
or missing items are expected.

<div class="grid cards" markdown>

-   :material-account-tie: **[Administrator](admin.md)**

    Runs the school: members, fleet, finance, training setup, handling, settings and
    permissions.

-   :material-human-male-board: **[Instructor](instructor.md)**

    Teaches: bookings, student progress, lesson & ground assessments, flight logs.

-   :material-account-school: **[Student & Pilot](student.md)**

    Learns and flies: calendar, courses, progress, quizzes, logbook, account. Includes
    **qualified pilot** and **social member** variants.

-   :material-desk: **[Front Desk / Staff](staff.md)**

    Runs the front desk: the calendar, handling, payments and documents.

-   :material-wrench: **[Engineer](engineer.md)**

    Keeps aircraft airworthy: fleet, maintenance log and aircraft documents.

</div>

## Who can see what (at a glance)

This shows the **default** areas for each role. Owners/administrators can grant extra
capabilities, so treat it as the starting point, not a hard limit.

| Symbol | Meaning |
|:------:|---------|
| :white_check_mark: | **On by default** — full access to everyone's records |
| :bust_in_silhouette: | **Own records only** — on by default, but limited to the user's own data |
| :large_orange_diamond: | **Off by default** — commonly granted, but not included to start |
| *(blank)* | Not available to this role |

| Area | Admin | Instructor | Student | Pilot | Staff | Engineer |
|------|:-----:|:----------:|:-------:|:-----:|:-----:|:--------:|
| Home dashboard | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: | |
| Bookings calendar | :white_check_mark: | :white_check_mark: | :bust_in_silhouette: | :bust_in_silhouette: | :white_check_mark: | :large_orange_diamond: |
| Manage any booking | :white_check_mark: | | | | :white_check_mark: | :large_orange_diamond: |
| Members list | :white_check_mark: | | | | :large_orange_diamond: | :large_orange_diamond: |
| Fleet (view) | :white_check_mark: | :large_orange_diamond: | | | :large_orange_diamond: | :white_check_mark: |
| Fleet & maintenance (edit) | :large_orange_diamond: | | | | | :white_check_mark: |
| Training / courses | :white_check_mark: | :white_check_mark: | :white_check_mark: | | | |
| Assessments (submit) | :large_orange_diamond: | :white_check_mark: | | | | |
| Student progress | :white_check_mark: | :white_check_mark: | :bust_in_silhouette: | | | |
| Pilot's logbook | :white_check_mark: | :bust_in_silhouette: | :bust_in_silhouette: | :bust_in_silhouette: | | |
| Quizzes | :white_check_mark: | | :white_check_mark: | :white_check_mark: | | |
| Finance / billing | :white_check_mark: | | | | :large_orange_diamond: | :large_orange_diamond: |
| Vouchers & packages | :white_check_mark: | | | | :large_orange_diamond: | :large_orange_diamond: |
| Handling / PPR *(add-on)* | :white_check_mark: | | | | :white_check_mark: | :large_orange_diamond: |
| Documents | :white_check_mark: | :bust_in_silhouette: | :bust_in_silhouette: | :bust_in_silhouette: | :large_orange_diamond: | :white_check_mark: |
| Office / HR self-service | :white_check_mark: | :white_check_mark: | | | :white_check_mark: | :white_check_mark: |
| HR administration | :white_check_mark: | | | | :large_orange_diamond: | |
| Compliance | :white_check_mark: | :bust_in_silhouette: | | | :bust_in_silhouette: | :bust_in_silhouette: |
| School settings | :white_check_mark: | | | | | |
| Permissions | :white_check_mark: | | | | | |

!!! note
    :bust_in_silhouette: means the person sees only their **own** records (their bookings,
    logbook, documents). For engineers, the **Documents** row covers **aircraft** documents
    rather than personal ones. Administrators and the relevant staff see everyone's.

For the precise permission keys behind each area, see
**[Capabilities & permissions](../reference/capabilities.md)**.
