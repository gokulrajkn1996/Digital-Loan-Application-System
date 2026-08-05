# 08 — Defect Management and Log

## Severity definitions

| Severity | Definition | Target response |
|---|---|---|
| S1 — Critical | Application unavailable, data exposure or critical workflow cannot complete | Immediate |
| S2 — High | Major function fails and no reasonable workaround exists | Same business day |
| S3 — Medium | Function is impaired but a workaround exists | Planned fix |
| S4 — Low | Cosmetic, wording or minor usability issue | Backlog / planned fix |

## Lifecycle

New → Triaged → Assigned → In Progress → Ready for Retest → Closed  
Alternative outcomes: Duplicate, Deferred, Not a Defect, Cannot Reproduce.

## Sample defect log

| ID | Scenario | Summary | Severity | Status | Expected resolution |
|---|---|---|---|---|---|
| DEF-001 | UAT-04 | DTI displayed more than one decimal place | S3 | Closed | Round result to one decimal |
| DEF-002 | UAT-03 | Form allowed submission without demonstration consent | S2 | Closed | Enforce required checkbox |
| DEF-003 | UAT-13 | Navigation wrapped incorrectly at mobile width | S3 | Closed | Apply responsive navigation layout |
| DEF-004 | UAT-11 | Simulated-rule disclosure not visible on every workflow | S3 | Closed | Add persistent disclosure banner |
| DEF-005 | UAT-07 | High-DTI application showed standard routing | S2 | Closed | Correct rule order and retest boundaries |

## Defect record template

- **Defect ID:**
- **Title:**
- **Environment/browser:**
- **Related requirement and UAT scenario:**
- **Preconditions:**
- **Steps to reproduce:**
- **Expected result:**
- **Actual result:**
- **Severity / priority:**
- **Evidence:**
- **Owner:**
- **Resolution and retest result:**

## Triage principles

- Severity describes business impact; priority describes repair order.
- A resolved defect is closed only after independent retesting.
- Rule-boundary defects require regression tests for adjacent thresholds.
- Any privacy or disclosure issue is escalated immediately.
