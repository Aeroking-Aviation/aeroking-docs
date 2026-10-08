# Dashboard overview

The **AeroKing Dashboard** is a complete management system for a flying school or club.
It replaces spreadsheets, paper diaries and legacy databases with one real-time system
that covers the whole student journey — from a first trial lesson through to a licence —
alongside the fleet, memberships, money and ground handling.

This page explains the **big-picture concepts** that everything else builds on. You don't
need to read it cover to cover, but understanding these ideas makes the role manuals much
easier to follow.

## What the Dashboard covers

<div class="grid cards" markdown>

-   :material-calendar-check: **Booking & scheduling**

    A shared calendar for lessons, rentals, trial flights, maintenance slots, ground
    school and simulator sessions — with automatic double-booking protection.

-   :material-school: **Student training**

    Syllabus-based courses, lesson assessments with grades and debrief notes, quizzes,
    and each pilot's logbook and progress.

-   :material-airplane: **Fleet**

    Every aircraft and simulator, with airworthiness, insurance and servicing reminders,
    plus a full maintenance log.

-   :material-card-account-details: **Members & memberships**

    Member records, tiered memberships, and each person's account balance.

-   :material-cash-multiple: **Finance**

    Invoices, payments, statements, VAT, gift vouchers and prepaid packages.

-   :material-sign-direction: **Ground handling (PPR)**

    Visiting-aircraft requests, parking, and a rate card — an optional add-on.

-   :material-briefcase: **Office / HR**

    Staff leave, work permits, policies, a team directory and compliance monitoring.

-   :material-file-document: **Documents**

    A single store for certificates and records, with expiry tracking.

</div>

## Core concepts

### 1. Each school is its own private portal (multi-tenant)

AeroKing can host many schools on one platform, but each school is completely separate.
You reach your school through **its own web address** (e.g.
`https://highland.aerokingaviation.com`), see only your school's data, and your school
controls its own branding, settings and members.

!!! info "Why this matters to you"
    You can't accidentally see — or be seen by — another school. If your school shares an
    aircraft with another school, that sharing is set up deliberately by an administrator.

### 2. Roles describe what you *are*

Your **role** is the broad description of who you are in the school. Each role has a home
dashboard and a default set of menus:

| Role | Who it's for | Home |
|------|--------------|------|
| **Student** | People training towards a licence or rating | Student dashboard |
| **Qualified pilot** | Licensed pilots who rent/hire aircraft (not training) | Student dashboard (no training) |
| **Social** | Non-flying club members | My Account |
| **Instructor** | Flying instructors | Instructor dashboard |
| **Staff** | Front-desk / operations team | Staff dashboard |
| **Engineer** | Aircraft maintenance | The Fleet |
| **Administrator** | Runs the school day to day | Admin dashboard |

See the **[role matrix](roles/index.md)** for a side-by-side comparison.

### 3. Capabilities describe what you *can do*

On top of your role, AeroKing uses **capabilities** — fine-grained permissions like
"view the calendar", "create invoices" or "submit assessments". Your role comes with a
sensible default set, and an owner or administrator can **grant or remove individual
capabilities** for any person.

This is why **two people with the same role might see slightly different menus**: one may
have been given an extra capability. The menu only ever shows areas you actually have
permission to use.

!!! example "A practical example"
    By default, instructors can submit assessments and admins can't. But an owner can grant
    the "submit assessments" capability to a specific administrator — and the Assessments
    menu then appears for that admin automatically.

The full list is on the **[Capabilities & permissions](reference/capabilities.md)** page.

### 4. The membership ladder (for flying members)

Flying members progress along a ladder, and each rung **inherits** everything below it:

```
student → qualified pilot → trainee instructor → qualified instructor → examiner
```

So a qualified instructor can still do everything a qualified pilot can. **Social** members
sit outside this ladder — they're club members who don't fly.

### 5. Add-ons (plugins)

Some features are **optional add-ons** your school can switch on, such as:

- **Handling / PPR** — visiting-aircraft parking and permission-to-land requests.
- **Departure Board** — a public lobby screen of the day's movements.

If your school hasn't enabled an add-on, you simply won't see its menu — there's nothing
to configure on your side.

## How a typical day flows

A quick mental model of how the pieces connect:

1. A **student** or **pilot** requests a booking from their calendar.
2. **Staff** or an **administrator** confirm it (double-booking is blocked automatically).
3. After the flight, the **instructor** records the lesson, grades it, and both the
   student's **logbook** and **progress** update.
4. Flight time and fees post to the member's **account**; **staff/admin** raise an
   **invoice** or take payment.
5. The **engineer** logs maintenance and the aircraft's hours tick towards its next
   **service reminder**.

Everyone is working on the same live data, so nothing has to be re-typed between systems.

---

**Next:** open **[your role manual](roles/index.md)**.
