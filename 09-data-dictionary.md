# 09 — Data Dictionary

| Field | Type / format | Required | Definition / validation | Classification |
|---|---|---:|---|---|
| application_reference | Text, `LN-YYYY-NNNN` | Yes | Unique demonstration application identifier | Internal |
| first_name | Text, 1–50 chars | Yes | Fictional applicant given name | Demo PII |
| last_name | Text, 1–50 chars | Yes | Fictional applicant family name | Demo PII |
| email | Valid email format | Yes | Fictional contact address | Demo PII |
| province | Enumeration | Yes | Canadian province of residence | Demo PII |
| loan_product | Enumeration | Yes | Personal Loan, Auto Loan or Line of Credit | Internal |
| requested_amount | Currency CAD | Yes | Minimum 1,000; positive number | Confidential demo |
| monthly_gross_income | Currency CAD | Yes | Non-negative monthly income | Confidential demo |
| monthly_debt_payments | Currency CAD | Yes | Non-negative recurring debt payments | Confidential demo |
| employment_status | Enumeration | Yes | Full-time, part-time, self-employed or contract | Confidential demo |
| simulated_credit_score | Integer, 300–900 | Yes | Fictional score used only for routing simulation | Confidential demo |
| dti_percentage | Decimal, 1 place | Derived | Debt ÷ gross income × 100 | Internal |
| risk_category | Enumeration | Derived | Low, Medium, High or Exception | Internal |
| workflow_route | Enumeration | Derived | Loan Officer, Underwriter or Manual Review | Internal |
| application_status | Enumeration | Yes | Current value from approved status model | Internal |
| consent_confirmed | Boolean | Yes | Confirms demonstration uses fictional information | Internal |
| submitted_at | ISO 8601 date/time | Derived | Date and time of successful submission | Internal |
| assigned_reviewer | Text / user ID | No | Demonstration reviewer responsible for case | Internal |
| decision | Enumeration | No | Approved, Declined or Pending | Confidential demo |
| decision_reason | Text | No | Demonstration rationale; must not include real data | Confidential demo |

## Data-quality rules

- Required fields cannot be null at submission.
- Numeric values must be within documented ranges.
- Derived values must be recalculated when source fields change.
- Status must use the approved transition model.
- Reference numbers must be unique within the demonstration dataset.
- Real customer, employee or client data must never be entered.

## Retention and privacy note

The static prototype does not intentionally persist submitted form information. A production solution would require approved retention, consent, access-control, encryption, audit and deletion requirements before handling personal information.
