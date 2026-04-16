---
title: Product Requirements Document (PRD)
description: Template for prd-template
---

# Product Requirements Document (PRD)

**Feature Name:** [Feature name]

**Author:** [Your name, role]

**Date:** [Creation date]

**Last Updated:** [Last update date]

**Status:** [Draft | In Review | Approved | In Development | Launched]

---

## Executive Summary

[2-3 sentence overview of what we're building, why it matters, and expected impact]

---

## 1. Problem Statement

### The Problem
[Describe the customer problem or opportunity. What pain point are we solving?]

### Target Users
[Who experiences this problem? Be specific about user segments]

- **Primary Users:** [e.g., Wealth managers with 50+ clients]
- **Secondary Users:** [e.g., Portfolio administrators]

### Current State
[What are users doing today? What are the workarounds or alternatives?]

### Jobs-to-be-Done
```
When [situation],
I want to [motivation],
So I can [expected outcome]
```

### Impact of Not Solving
[What happens if we don't build this? What is the cost of inaction?]

---

## 2. Goals & Success Criteria

### Business Goals
[What business outcomes are we targeting?]

- [Goal 1: e.g., Increase AUM per advisor by 20%]
- [Goal 2: e.g., Reduce operational costs by $100K/year]
- [Goal 3: e.g., Improve advisor retention by 15%]

### Success Metrics

**Adoption Metrics:**
- [Metric 1: e.g., 60% of wealth managers using feature within 90 days]

**Outcome Metrics:**
- [Metric 2: e.g., Reduce portfolio review time by 66%]

**Satisfaction Metrics:**
- [Metric 3: e.g., Feature satisfaction score >4.5/5]

**Business Metrics:**
- [Metric 4: e.g., Increase AUM per advisor by 20%]

**Measurement Plan:**
- How: [Analytics tools, dashboards]
- When: [Review cadence]
- Owner: [Person responsible]

---

## 3. User Research & Validation

### Research Conducted
[Summary of customer interviews, surveys, usability tests]

- **Method:** [e.g., 10 customer interviews]
- **Date:** [When conducted]
- **Key Findings:** [Main insights]

### Customer Quotes
> "[Actual customer quote that validates the problem]"
> — [Customer name/role]

### Validation Status
- [ ] Problem validated with customers
- [ ] Solution concept tested
- [ ] Prototype validated
- [ ] Pricing/value validated

### Supporting Research
- [Link to research report]
- [Link to competitive analysis]
- [Link to market sizing]

---

## 4. Solution Overview

### High-Level Description
[Describe the solution in plain language. What are we building?]

### User Experience
[Describe the end-to-end user experience. How will users interact with this?]

### Key Features
1. **[Feature 1]** - [Brief description]
2. **[Feature 2]** - [Brief description]
3. **[Feature 3]** - [Brief description]

### User Flows
[Link to user flow diagrams or describe key flows]

### Design Artifacts
- [Link to wireframes]
- [Link to prototypes]
- [Link to design specs]

---

## 5. User Stories & Requirements

### Epic
As a [user type],
I want to [action],
So that [benefit]

### User Stories

#### Story 1: [Story title]
**As a** [user type]
**I want to** [action]
**So that** [benefit]

**Acceptance Criteria:**
- [ ] [Criterion 1]
- [ ] [Criterion 2]
- [ ] [Criterion 3]

**Priority:** [Must Have | Should Have | Could Have | Won't Have]

#### Story 2: [Story title]
[Repeat structure above]

### Functional Requirements
- [Requirement 1: System shall...]
- [Requirement 2: System shall...]

### Non-Functional Requirements
- **Performance:** [e.g., Page load time less than 2 seconds]
- **Security:** [e.g., Data encrypted at rest and in transit]
- **Compliance:** [e.g., Audit trail for all transactions]
- **Accessibility:** [e.g., WCAG 2.1 AA compliance]
- **Scalability:** [e.g., Support 10K concurrent users]

---

## 6. Financial Services Considerations

### Regulatory & Compliance
- **Regulations:** [SEC, FINRA, state regulations]
- **Requirements:** [Specific compliance needs]
- **Audit Trail:** [What needs to be logged]
- **Reporting:** [Regulatory reporting requirements]

### Security & Privacy
- **Data Classification:** [PII, financial data, etc.]
- **Access Controls:** [Role-based permissions]
- **Encryption:** [Standards and requirements]
- **Authentication:** [MFA, SSO requirements]

### Risk Management
- **Financial Risk:** [Transaction accuracy, money movement]
- **Operational Risk:** [System stability, disaster recovery]
- **Reputational Risk:** [Customer trust implications]
- **Mitigation:** [How we're addressing each risk]

---

## 7. Technical Considerations

### Architecture Approach
[High-level technical approach. Link to detailed tech design doc]

### Dependencies
- **Internal:** [Other systems/services this depends on]
- **External:** [Third-party APIs, vendors]
- **Team Dependencies:** [Other teams required]

### Technical Risks
- [Risk 1: e.g., Integration complexity with legacy system]
- [Risk 2: e.g., Performance at scale unknown]
- **Mitigation:** [How we'll address each risk]

### API Changes
- [ ] New APIs
- [ ] Modified existing APIs
- [ ] Deprecated APIs

### Data Requirements
- **New Data:** [What new data we're collecting/storing]
- **Data Migration:** [Any existing data that needs migration]
- **Data Retention:** [Retention policies]

---

## 8. Go-to-Market Plan

### Launch Strategy
- **Rollout Plan:** [Phased vs. big bang]
  - Phase 1: [Internal users, timing]
  - Phase 2: [Beta customers, timing]
  - Phase 3: [General availability, timing]

### Marketing & Communication
- **Internal:** [How we'll train and communicate internally]
- **External:** [Customer announcements, marketing campaigns]
- **Positioning:** [Key messages, value props]

### Sales Enablement
- **Materials Needed:** [Pitch deck, demo scripts, FAQs]
- **Training Plan:** [Sales team training schedule]

### Customer Support
- **Documentation:** [User guides, help articles, FAQs]
- **Training:** [Support team training plan]
- **Escalation:** [How to handle issues]

---

## 9. Scope & Prioritization

### In Scope
- [Feature 1]
- [Feature 2]
- [Feature 3]

### Out of Scope
- [Feature X: e.g., Mobile app version - deferred to Q3]
- [Feature Y: e.g., Advanced analytics - future consideration]

### MVP Definition
**Minimum Viable Product includes:**
- [Must-have feature 1]
- [Must-have feature 2]
- [Must-have feature 3]

**Post-MVP Enhancements:**
- V1.1: [Enhancement 1]
- V1.2: [Enhancement 2]

### RICE Score
- **Reach:** [Number of users per quarter]
- **Impact:** [0.25 - 3 score]
- **Confidence:** [Percentage]
- **Effort:** [Person-months]
- **Score:** [Calculated RICE score]

---

## 10. Timeline & Resources

### Target Milestones
- **PRD Approval:** [Date]
- **Design Complete:** [Date]
- **Development Start:** [Date]
- **Code Complete:** [Date]
- **Testing Complete:** [Date]
- **Beta Launch:** [Date]
- **General Availability:** [Date]

### Resource Requirements
- **Product:** [X person-months, names]
- **Design:** [X person-months, names]
- **Engineering:** [X person-months, names]
- **QA:** [X person-months, names]
- **Other:** [Documentation, compliance, etc.]

### Budget
- **Development:** [$X]
- **Infrastructure:** [$X/month]
- **Third-party Services:** [$X]
- **Total:** [$X]

---

## 11. Risks & Mitigation

| Risk | Probability | Impact | Mitigation | Owner |
|------|-------------|--------|------------|-------|
| [Risk 1] | High/Med/Low | High/Med/Low | [How we'll mitigate] | [Name] |
| [Risk 2] | High/Med/Low | High/Med/Low | [How we'll mitigate] | [Name] |

---

## 12. Open Questions

- [ ] [Question 1 that needs resolution]
- [ ] [Question 2 that needs resolution]

---

## 13. Approval & Sign-off

| Role | Name | Status | Date |
|------|------|--------|------|
| CPO | [Name] | [Approved/Pending] | [Date] |
| CTO | [Name] | [Approved/Pending] | [Date] |
| UX Designer | [Name] | [Approved/Pending] | [Date] |
| Compliance | [Name] | [Approved/Pending] | [Date] |
| CEO | [Name] | [Approved/Pending] | [Date] |

---

## Appendix

### A. Research Reports
- [Link to customer research]
- [Link to competitive analysis]
- [Link to market sizing]

### B. Design Assets
- [Link to user flows]
- [Link to wireframes]
- [Link to prototypes]

### C. Technical Design
- [Link to technical design document]
- [Link to API specs]

### D. Related Documents
- [Link to related PRDs]
- [Link to roadmap]
- [Link to OKRs]
