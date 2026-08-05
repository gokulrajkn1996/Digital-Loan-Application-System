# 03 — User Stories and Acceptance Criteria

## US-01 — Submit an application

**As an applicant, I want to enter my personal and loan information so that I can request a loan review.**

Acceptance criteria:

- Given the application form is open, when mandatory fields are empty, then submission is blocked.
- Given valid fictional data and consent confirmation, when the applicant submits, then a reference number is displayed.
- Given an invalid email or out-of-range score, when submitted, then the invalid field is identified.

## US-02 — View affordability

**As an applicant, I want to see an indicative DTI calculation so that I understand the affordability assessment.**

Acceptance criteria:

- DTI updates when income or debt changes.
- DTI is rounded to one decimal place.
- If income is zero, the application is flagged for review rather than dividing by zero.

## US-03 — Route by simulated risk

**As a loan officer, I want applications classified and routed consistently so that I can prioritize reviews.**

Acceptance criteria:

- Low-, medium- and high-risk labels follow approved demonstration rules.
- High-risk records are flagged for manual underwriting review.
- The displayed result states that it is simulated and not a credit decision.

## US-04 — Review the queue

**As a loan officer, I want a prioritized application queue so that I know which cases need action.**

Acceptance criteria:

- Queue rows show reference, applicant, amount, risk and status.
- Higher-risk and exception cases are visually identifiable.
- Selecting a record shows the available review details.

## US-05 — Track status

**As an applicant, I want to see the progress of my application so that I know what happens next.**

Acceptance criteria:

- The timeline shows submitted, KYC, assessment, decision and completion stages.
- The current stage is distinguished from completed and pending stages.
- A reference number identifies the application.

## US-06 — Monitor performance

**As an operations manager, I want portfolio KPIs so that I can identify volumes and bottlenecks.**

Acceptance criteria:

- KPIs include application volume, approval rate and turnaround time.
- Funnel and risk distribution are visible.
- Values use fictional demonstration data.

## US-07 — Understand the project boundary

**As a recruiter or reviewer, I want transparent project disclosures so that I can assess the work accurately.**

Acceptance criteria:

- The application and repository identify the project as independently created.
- No employer, banking client or confidential implementation is claimed.
- All rules and records are labelled fictional or simulated.
