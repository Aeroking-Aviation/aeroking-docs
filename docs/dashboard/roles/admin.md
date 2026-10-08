# Administrator manual

Administrators run the school day to day. You have the broadest access in the Dashboard:
members, the fleet, finance, training setup, ground handling, the office/HR area, and the
school's own settings and permissions.

!!! info "Owner vs administrator"
    The **owner** is the school's account holder and automatically has *every* capability.
    An **administrator** has a broad default set that the owner can extend or trim. In
    everyday use the two look almost identical; only the owner can manage the subscription
    itself (via the separate owner portal).

## Your menu

| Menu | Pages | What it's for |
|------|-------|---------------|
| **Home** | Admin dashboard | Today's snapshot: bookings, approvals, alerts |
| **Schedule** | Bookings Calendar · Pending Requests · Flight Summary | Run the diary and approve requests |
| **Members** | Members · Add Member | The people directory and onboarding |
| **Fleet** | Aircraft list & detail | Aircraft, reminders, maintenance |
| **Training** | Courses · Syllabus Frameworks | Build the training programme |
| **Assessments** | *(if granted)* | Grade lessons — off by default for admins |
| **Handling** | PPR console *(add-on)* | Visiting-aircraft requests and parking |
| **Finance** | Billing & Accounts · Vouchers & Packages | Invoices, payments, statements, vouchers |
| **Office** | Leave, permits, policies, directory, compliance, HR Admin | Staff administration |
| **Settings** | School Settings · Forms · Permissions · add-on config | Configure the school |
| **Overview** | Overview | High-level activity view |

## Key tasks

### Add a new member

1. Go to **Members → Add Member**.
2. Enter the person's name and email, and choose their **role** (student, qualified pilot,
   instructor, staff, engineer or social).
3. For flying members, set the **membership tier** and **rank** if applicable.
4. Save. The member receives an email invitation to set their password.

!!! tip "Bringing people over in bulk"
    Moving from spreadsheets or a legacy system? Use **Members → import** to upload many
    members at once, and the document importer to attach their existing files. Ask your
    AeroKing contact if you need the import templates.

### Confirm or decline a booking request

1. Open **Schedule → Pending Requests** (the badge shows how many are waiting).
2. Review each request — aircraft, instructor, time.
3. **Confirm** to place it on the calendar, or **Decline** with a reason.

AeroKing blocks double-bookings automatically, so you can't confirm a slot that clashes
with another aircraft or instructor booking.

### Raise an invoice or take a payment

1. Go to **Finance → Billing & Accounts**.
2. Find the member, or choose **ad-hoc** for a walk-in / non-member.
3. Add line items (the rate card fills in net / VAT / gross).
4. Issue the invoice, then record the payment method when it's paid.

Every charge, payment, refund and adjustment is kept in an append-only ledger, so a
member's **statement** always reconciles.

### Sell a gift voucher or package

1. Go to **Finance → Vouchers & Packages**.
2. Choose a product from the rate card (e.g. a trial-flight experience) or build a package.
3. Generate the voucher — it can be printed from a branded template for the customer.

When the voucher is redeemed against a booking, its value is drawn down automatically.

### Set up a training course

1. Go to **Training → Syllabus Frameworks** to pick or review the syllabus (e.g. the EASA
   framework ships built in).
2. Go to **Training → Courses** to create a course and its lessons/exercises.
3. Enrol students; their **progress** then tracks against the course automatically as
   instructors grade lessons.

### Manage the fleet

1. Go to **Fleet** and open an aircraft.
2. Keep **airworthiness, insurance, radio licence and pitot-static** expiries current.
3. Set **servicing reminders** by date or by Hobbs hours, and add custom reminder labels.

Day-to-day maintenance logging is usually done by the [Engineer](engineer.md); as an
administrator you can view it and configure the reminders.

### Adjust someone's permissions

1. Go to **Settings → Permissions**.
2. Choose a **role preset** to change the defaults for everyone in that role, **or**
3. Open an individual member and grant/remove specific capabilities just for them.

See **[Capabilities & permissions](../reference/capabilities.md)** for what each one does.

### Configure the school

**Settings → School Settings** is where you set branding (logo, name), membership tiers,
VAT, weight classes, and toggle add-ons like **Handling/PPR** and the **Departure Board**.
**Settings → Forms** lets you build digital forms (e.g. membership waivers) that members
sign online.

## The Office (HR) area

As an administrator you typically hold **HR administration**, which lets you:

- Approve or decline **leave** requests and view the **team calendar**.
- Manage **work permits**, **policies** and the **noticeboard**.
- Run **compliance** monitoring and receive expiry reminders.

Staff and instructors use the same area for self-service (booking their own leave, reading
policies). See the [Staff manual](staff.md#your-own-leave-and-policies) for the
self-service side.

## Good habits

- **Approve promptly** — members can't fly until a request is confirmed.
- **Keep expiries green** — the Fleet and Compliance areas flag what's due; acting early
  avoids a grounded aircraft or a lapsed certificate.
- **Use statements to answer billing questions** — a member's statement is the single
  source of truth for what they owe or hold in credit.

---

**Related:** [Instructor](instructor.md) · [Staff](staff.md) · [Engineer](engineer.md) ·
[Capabilities](../reference/capabilities.md) · [FAQ](../faq.md)
