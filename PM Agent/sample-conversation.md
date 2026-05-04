# Sample Conversation Script

## Scenario
You want to explore a new feature for helping small business owners track vendor payments and validate whether it fits your product.

## Conversation flow

### User
I want to explore a new feature for helping small business owners track vendor payments.

### EJ
That sounds promising. To help structure discovery, I need more detail first.
- Who is the primary user or persona for this feature?
- What is their current vendor payment process today?
- What outcome would make this feature successful for them?

### User
The primary user is a small business owner who currently uses spreadsheets and email to track payments. They struggle to know which invoices are due, which vendors have been paid, and how much cash they need to reserve.

### EJ
Great, that gives us a strong starting point. I recommend using either:
- **Jobs to be Done** to understand the job they are hiring this feature for, or
- **Opportunity Solution Tree** to map the problem, needs, and possible solutions.

Would you like me to generate a problem statement, user story, or opportunity map next?

### User
Please create all three artifacts.

### EJ
#### Problem Statement
- **Context:** Small business owners use spreadsheets and email to track vendor payments.
- **User / Persona:** Small business owner managing vendor invoices.
- **Need / Pain:** They need a reliable way to see due invoices, payment status, and cash impact.
- **Outcome / Benefit:** They can make timely payments, reduce late fees, and preserve working capital.
- **Product / Service Fit:** This aligns with the product's financial operations and cash management capabilities.

```json
{
  "artifactType": "problem_statement",
  "context": "Small business owners use spreadsheets and email to track vendor payments.",
  "user": "Small business owner managing vendor invoices",
  "need": "Reliable visibility into due invoices, payment status, and cash impact",
  "outcome": "Timely payments, reduced late fees, and preserved working capital",
  "productFit": "Aligns with financial operations and cash management capabilities",
  "nextSteps": [
    "Interview representative small business owners about current payment workflows",
    "Define the minimum viable workflow for invoice visibility and payment tracking"
  ]
}
```

#### User Story
- **Persona:** Small business owner
- **As a:** small business owner
- **I want:** a single view of vendor invoice due dates, payment status, and cash requirements
- **So that:** I can avoid late payments and plan cash flow with confidence
- **Acceptance Criteria:**
  - The dashboard shows upcoming due invoices by date
  - The feature indicates paid vs unpaid vendor invoices
  - The solution estimates cash required for upcoming payments
- **Implementation Notes:**
  - Integrate with existing invoice and vendor data sources
  - Provide a simple dashboard and notification summary

**Gherkin Feature:**
```
Feature: Vendor Payment Tracking Dashboard
  As a small business owner
  I want a single view of vendor invoice due dates, payment status, and cash requirements
  So that I can avoid late payments and plan cash flow with confidence

  Scenario: View upcoming due invoices
    Given I have unpaid vendor invoices
    When I access the payment dashboard
    Then I see a list of upcoming due dates sorted by date

  Scenario: Check payment status
    Given I have vendor invoices with different payment statuses
    When I view the invoice list
    Then I can see which invoices are paid and which are unpaid

  Scenario: Estimate cash requirements
    Given I have upcoming due invoices
    When I check the dashboard
    Then I see an estimate of cash needed for upcoming payments
```

```json
{
  "artifactType": "user_story",
  "persona": "Small business owner",
  "role": "small business owner",
  "goal": "a single view of vendor invoice due dates, payment status, and cash requirements",
  "benefit": "avoid late payments and plan cash flow with confidence",
  "acceptanceCriteria": [
    "The dashboard shows upcoming due invoices by date",
    "The feature indicates paid vs unpaid vendor invoices",
    "The solution estimates cash required for upcoming payments"
  ],
  "implementationNotes": "Integrate with existing invoice and vendor data sources. Provide a simple dashboard and notification summary.",
  "gherkinFeature": {
    "name": "Vendor Payment Tracking Dashboard",
    "scenarios": [
      {
        "name": "View upcoming due invoices",
        "given": "I have unpaid vendor invoices",
        "when": "I access the payment dashboard",
        "then": "I see a list of upcoming due dates sorted by date"
      },
      {
        "name": "Check payment status",
        "given": "I have vendor invoices with different payment statuses",
        "when": "I view the invoice list",
        "then": "I can see which invoices are paid and which are unpaid"
      },
      {
        "name": "Estimate cash requirements",
        "given": "I have upcoming due invoices",
        "when": "I check the dashboard",
        "then": "I see an estimate of cash needed for upcoming payments"
      }
    ]
  }
}
```

#### Opportunity Map
- **Problem:** Small business owners lack a consolidated view of vendor payment status and cash needs.
- **User Needs:**
  - See which invoices are due soon
  - Confirm which vendors have been paid
  - Understand cash required for upcoming payments
- **Solution Ideas:**
  - A vendor payment dashboard with invoice status
  - Automated reminders for due payments
  - Cash flow forecasting for upcoming vendor obligations
- **Impact:** Reduces late payments, improves cash planning, and lowers vendor relationship risk.

```json
{
  "artifactType": "opportunity_map",
  "problem": "Small business owners lack a consolidated view of vendor payment status and cash needs.",
  "userNeeds": [
    "See which invoices are due soon",
    "Confirm which vendors have been paid",
    "Understand cash required for upcoming payments"
  ],
  "solutionIdeas": [
    "A vendor payment dashboard with invoice status",
    "Automated reminders for due payments",
    "Cash flow forecasting for upcoming vendor obligations"
  ],
  "impact": "Reduces late payments, improves cash planning, and lowers vendor relationship risk.",
  "nextSteps": [
    "Validate the concept with small business owners",
    "Estimate effort to build the dashboard and reminders"
  ]
}
```

### User
Thanks. Can you also summarize the product fit?

### EJ
#### Benefit Alignment Summary
- **User Benefit:** Clear, consolidated visibility into vendor payments and cash needs.
- **Product/Service Element:** Financial operations dashboard and payment tracking workflow.
- **Why it matters:** It reduces risk, improves cash planning, and supports small business financial health.
- **Gap / Risk:** If invoice data is incomplete or delayed, the dashboard may be inaccurate.

```json
{
  "artifactType": "benefit_alignment",
  "userBenefit": "Clear, consolidated visibility into vendor payments and cash needs.",
  "productServiceElement": "Financial operations dashboard and payment tracking workflow.",
  "whyItMatters": "It reduces risk, improves cash planning, and supports small business financial health.",
  "gapOrRisk": "If invoice data is incomplete or delayed, the dashboard may be inaccurate."
}
```

### User
That is helpful. What should I do next?

### Terese
I recommend:
1. Interview a few representative small business owners to validate the pain and current workflow.
2. Define the MVP scope for the payment tracking dashboard.
3. Sketch the data flow and integration points for invoice, vendor, and cash availability data.
4. Choose a prioritization framework such as RICE or Kano to evaluate the feature against other initiatives.
