# Safety reporting

AeroKing's Safety Management System (SMS) lets anyone raise an occurrence, hazard or
near-miss in seconds, and gives the safety team a register to triage, investigate and close
reports out.

## Raise a report

1. Open **Safety → My Reports** and select **Raise a report**.
2. Pick the **type** — occurrence, hazard or observation.
3. Describe **what happened** (the only required field), plus when, where and the aircraft if
   relevant.
4. Optionally add people involved and how serious it felt.
5. Submit — it reaches the safety team straight away.

!!! tip "Report straight from a flight or booking"
    You can start a report from a **flight close-out** or a **booking** — the aircraft and the
    people are linked for you automatically, so there's less to type.

??? question "I'd rather not be named"
    Tick **Submit confidentially**. Your name is hidden from everyone except the safety team.

## The safety register (safety team)

Holders of the safety **view/manage** capability get the register under **Safety → Reports**:

- **Triage** incoming reports and set a status.
- **Classify** likelihood × severity on the **risk matrix**.
- Record the **investigation** and any actions.
- **Close out** the report when it's resolved.

## Who sees what

- **Reporters** (`safety.report`) see and raise their own reports under *My Reports*.
- The **safety team** (`safety.view` / `safety.manage`) sees the full register and can triage,
  investigate and close. Confidential reporters' names are only visible to this group.
