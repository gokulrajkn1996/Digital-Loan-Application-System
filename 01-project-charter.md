# 01 — Project Charter

## Project

Digital Loan Application & Approval System

## Business problem

Manual loan intake can create incomplete applications, inconsistent affordability assessments, limited status visibility and longer review times. A standardized digital workflow is needed to collect required information, apply consistent validation and route applications for review.

## Objective

Deliver a demonstrable web application that supports application intake, KYC review, simulated risk classification, loan-officer review, status tracking and management reporting.

## Success measures

- 100% of submitted applications contain mandatory information.
- Debt-to-income ratio is calculated consistently.
- Every application receives a unique reference number and status.
- Applications are routed according to documented simulated rules.
- Reviewers can see a prioritized queue and decision history.
- Managers can view application, approval and risk metrics.

## In scope

- Personal-loan application intake
- Applicant, employment, income, debt and requested-loan information
- Consent confirmation and input validation
- Simulated KYC and credit-risk routing
- Loan-officer queue and decision capture
- Customer-facing application status
- Operational dashboard
- BA requirements, traceability and UAT artifacts

## Out of scope

- Real credit bureau, identity, sanctions or banking integrations
- Production authentication and authorization
- Electronic signatures, fund disbursement and payment servicing
- Real regulatory reporting or automated credit decisions
- Storage or processing of real personally identifiable information

## Stakeholders

| Stakeholder | Interest / responsibility |
|---|---|
| Applicant | Submit accurate information and track status |
| Loan Officer | Review applications, evidence and exceptions |
| Underwriter | Assess higher-risk or exceptional applications |
| Operations Manager | Monitor volumes, turnaround and bottlenecks |
| Compliance / Risk SME | Validate consent, KYC and decision controls |
| Product Owner | Prioritize scope and accept delivered outcomes |
| Business Analyst | Elicit, document, trace and validate requirements |
| Development / QA | Build and test the solution |

## Assumptions and constraints

- The prototype uses fictional data and simulated rules.
- GitHub Pages provides static hosting, so data is not persisted to a database.
- Rules illustrate workflow behaviour and are not lending policy.
- The design must work on modern desktop and mobile browsers.

## Key risks and responses

| Risk | Response |
|---|---|
| Prototype mistaken for a real decision engine | Display disclosure in app and repository |
| Inconsistent rule interpretation | Maintain a numbered business-rule catalogue |
| Missing traceability | Map each requirement to stories and UAT scenarios |
| Exposure of personal information | Use fictional records only; prohibit real applicant data |

## Deliverables

Working web prototype, GitHub repository, GitHub Pages deployment and complete BA documentation package.
