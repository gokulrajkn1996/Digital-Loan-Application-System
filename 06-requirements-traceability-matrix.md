# 06 — Requirements Traceability Matrix

| Business req. | Functional / non-functional req. | User story | Rule | UAT scenario | Status |
|---|---|---|---|---|---|
| BR-01 | FR-01, FR-02, FR-03, FR-04 | US-01 | BRULE-01, BRULE-02 | UAT-01, UAT-02 | Covered |
| BR-02 | FR-01, FR-02, FR-03, FR-04, FR-07 | US-01 | BRULE-01, BRULE-02, BRULE-09 | UAT-02, UAT-03 | Covered |
| BR-03 | FR-05, FR-06 | US-02, US-03 | BRULE-03–BRULE-07 | UAT-04–UAT-07 | Covered |
| BR-04 | FR-06, FR-09, FR-10 | US-03, US-04 | BRULE-08, BRULE-11 | UAT-07, UAT-08 | Covered |
| BR-05 | FR-08, FR-11 | US-05 | BRULE-10, BRULE-11 | UAT-09 | Covered |
| BR-06 | FR-12 | US-06 | — | UAT-10 | Covered |
| BR-07 | All requirements | US-07 | BRULE-12 | UAT-11 | Covered |
| BR-02 | NFR-03 | US-01 | — | UAT-12 | Covered |
| BR-01 | NFR-02, NFR-04 | US-01 | — | UAT-13 | Covered |
| BR-07 | NFR-05, NFR-06 | US-07 | BRULE-12 | UAT-11 | Covered |

## Traceability controls

- Requirement IDs remain stable after baseline approval.
- Changes must document impact to stories, rules, design and UAT.
- A requirement is considered validated only when its mapped UAT scenario passes.
- Defects reference the failed scenario and affected requirement.

## Change record template

| Change ID | Requested change | Reason | Impacted IDs | Priority | Decision |
|---|---|---|---|---|---|
| CR-001 | Example: revise DTI threshold | Policy clarification | FR-05, FR-06, BRULE-05–07, UAT-04–07 | High | Pending |
