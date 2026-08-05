# 07 — UAT Plan and Test Scenarios

## Purpose

Confirm that the prototype supports the agreed business workflow and that each critical requirement is demonstrable using fictional data.

## Entry criteria

- Requirements and simulated rules are baselined.
- Working build is available on GitHub Pages.
- Test data and expected results are reviewed.
- No open blocker prevents testing.

## Exit criteria

- All Must requirements have executed scenarios.
- 100% of critical scenarios pass.
- No open Severity 1 or Severity 2 defects.
- Remaining lower-severity defects have an accepted response.

## Roles

| Role | Responsibility |
|---|---|
| Product Owner | Approves scope and final acceptance |
| Business Analyst | Prepares scenarios, supports users and manages traceability |
| Loan Operations SME | Validates operational workflow |
| Risk / Compliance SME | Reviews disclosures and simulated controls |
| QA / Developer | Investigates and resolves defects |

## Test scenarios

| ID | Scenario / test data | Expected result | Priority |
|---|---|---|---|
| UAT-01 | Submit valid data: score 705, income 7200, debt 1900 | Submission succeeds; unique reference appears | Critical |
| UAT-02 | Leave a required name or email blank | Submission blocked; field identified | Critical |
| UAT-03 | Do not select fictional-data confirmation | Submission blocked | Critical |
| UAT-04 | Income 7200, debt 1900 | DTI displays 26.4% | High |
| UAT-05 | Score 720, DTI 30% | Low risk and officer route displayed | High |
| UAT-06 | Score 660, DTI 40% | Medium risk and officer route displayed | High |
| UAT-07 | Score 590 or DTI 50% | High risk and underwriter route displayed | Critical |
| UAT-08 | Open Officer Queue | Reference, applicant, amount, risk and status are visible | High |
| UAT-09 | Open Status | Current stage and timeline are visible | High |
| UAT-10 | Open Analytics | KPIs, funnel and risk distribution display | Medium |
| UAT-11 | Review app and README disclosure | Independent, fictional and simulated labels are visible | Critical |
| UAT-12 | Navigate by keyboard | Interactive controls receive visible focus and are operable | Medium |
| UAT-13 | Test desktop and 375 px mobile width | Content remains readable and usable | High |

## Test evidence

For each execution, record browser, date, tester, actual result, pass/fail result, screenshot reference and defect ID when applicable.

## Sign-off template

| Approver role | Name | Decision | Date | Comments |
|---|---|---|---|---|
| Product Owner | Portfolio simulation | Accepted / Rejected | YYYY-MM-DD | |
