# 02 — Business Requirements

## Business requirements

| ID | Requirement | Priority |
|---|---|---|
| BR-01 | Provide a consistent digital personal-loan intake process. | Must |
| BR-02 | Reduce incomplete submissions through mandatory-field validation. | Must |
| BR-03 | Present affordability and simulated risk information consistently. | Must |
| BR-04 | Route applications to the appropriate review path. | Must |
| BR-05 | Give applicants visibility into application progress. | Should |
| BR-06 | Give operations staff visibility into volumes, decisions and risk distribution. | Should |
| BR-07 | Maintain clear traceability between requirements, rules and tests. | Must |

## Functional requirements

| ID | Functional requirement | Acceptance summary |
|---|---|---|
| FR-01 | Capture applicant name, email and province. | Required fields cannot be blank. |
| FR-02 | Capture loan product and requested amount. | Amount must be numeric and at least $1,000. |
| FR-03 | Capture monthly gross income and debt payments. | Values must be non-negative numbers. |
| FR-04 | Capture employment status and simulated credit score. | Score must be between 300 and 900. |
| FR-05 | Calculate debt-to-income ratio (DTI). | DTI = monthly debt / monthly gross income × 100. |
| FR-06 | Classify simulated application risk. | Result follows the documented rule thresholds. |
| FR-07 | Require fictional-data confirmation before submission. | Submission is blocked until selected. |
| FR-08 | Generate an application reference number. | Successful submissions show a unique reference. |
| FR-09 | Place submitted applications in a review workflow. | Status and assigned route are displayed. |
| FR-10 | Display a loan-officer queue. | Queue shows reference, applicant, amount, risk and status. |
| FR-11 | Display an application timeline. | Major workflow stages and current state are visible. |
| FR-12 | Display management KPIs. | Dashboard includes volume, approval, turnaround and risk views. |

## Non-functional requirements

| ID | Requirement |
|---|---|
| NFR-01 | Pages should respond to user actions within two seconds under demonstration conditions. |
| NFR-02 | Layout must remain usable at widths of 375 px and above. |
| NFR-03 | Form fields must have visible labels and keyboard-accessible controls. |
| NFR-04 | The application must run in current Chrome, Edge, Firefox and Safari versions. |
| NFR-05 | The prototype must not request or retain real personal or financial information. |
| NFR-06 | Rules and results must be labelled as simulated. |

## Reporting requirements

- Total applications received
- Approval rate
- Average turnaround time
- Applications by workflow stage
- Applications by simulated risk category
- High-risk review volume
- Requested amount by product

## Dependencies

GitHub Pages availability, supported browser and approved simulated rule catalogue.
