# 05 — Use Cases and Business Rules

## UC-01 — Submit loan application

**Primary actor:** Applicant  
**Precondition:** Application page is available.  
**Trigger:** Applicant selects Submit for KYC Review.

### Main flow

1. Applicant enters identity, contact, loan and financial information.
2. System validates required fields and ranges.
3. System calculates DTI and simulated risk.
4. Applicant confirms fictional-data consent.
5. System generates a reference and sets status to Submitted.
6. System displays the next workflow step.

### Alternate flows

- A1: Missing/invalid field — highlight the field and prevent submission.
- A2: Income equals zero — flag for manual review.
- A3: High simulated risk — route to Underwriter Review.

## UC-02 — Review application

**Primary actor:** Loan Officer  
**Precondition:** Application is in an actionable review status.

1. Officer opens the queue and selects an application.
2. System displays application summary, DTI, risk and current status.
3. Officer records review outcome or escalates the case.
4. System updates the timeline and reporting metrics.

## UC-03 — Track application

**Primary actor:** Applicant  
**Precondition:** A valid application reference exists.

1. Applicant opens Status.
2. System shows reference, current stage and progress timeline.
3. Applicant reviews completed, current and pending stages.

## Business rules

| ID | Demonstration rule |
|---|---|
| BRULE-01 | Requested amount must be at least CAD $1,000. |
| BRULE-02 | Simulated credit score must be between 300 and 900. |
| BRULE-03 | DTI = monthly debt payments ÷ monthly gross income × 100. |
| BRULE-04 | If income is zero, route to manual review. |
| BRULE-05 | Low risk: score ≥ 700 and DTI < 35%. |
| BRULE-06 | Medium risk: score ≥ 620 and DTI < 45%, unless BRULE-05 applies. |
| BRULE-07 | All other combinations are high risk. |
| BRULE-08 | High-risk applications require underwriter review. |
| BRULE-09 | Fictional-data confirmation is mandatory before submission. |
| BRULE-10 | A successful submission must receive a unique reference number. |
| BRULE-11 | Only permitted status transitions in the process model may occur. |
| BRULE-12 | Risk labels are informational simulations, not credit decisions. |

## Decision table

| Credit score | DTI | Simulated result | Route |
|---|---:|---|---|
| ≥ 700 | < 35% | Low | Loan Officer |
| 620–699 | < 45% | Medium | Loan Officer |
| ≥ 700 | 35–44.9% | Medium | Loan Officer |
| Any | ≥ 45% | High | Underwriter |
| < 620 | Any | High | Underwriter |
| Any | Undefined due to zero income | Exception | Manual Review |

> These thresholds are simplified fictional rules created only for portfolio demonstration.
