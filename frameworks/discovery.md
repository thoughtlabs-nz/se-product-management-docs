---
title: Product Discovery Framework
description: Identify, validate, and prioritise product opportunities using JTBD and user research
---

# Product Discovery Framework

## Overview

Product discovery is how we identify, validate, and prioritise product opportunities. This framework ensures we build the right things for our customers in broker services and wealth management.

## Discovery Process

### 1. Opportunity Identification

**Sources of opportunities:**
- Customer feedback and support tickets
- Market trends and competitive analysis
- Regulatory changes and compliance requirements
- Business goals and strategic initiatives
- Technical debt and system improvements
- Data analytics and usage patterns

**Activities:**
- Customer interviews (quarterly cadence)
- User research sessions
- Market analysis reports
- Stakeholder input sessions
- Analytics review

### 2. Problem Definition

Use **Jobs-to-be-Done (JTBD)** framework:

```
When [situation],
I want to [motivation],
So I can [expected outcome]
```

**Example (Wealth Management):**
```
When reviewing client portfolios at month-end,
I want to generate comprehensive performance reports quickly,
So I can spend more time on client advisory instead of manual report creation
```

**Key Questions:**
- What problem are we solving?
- Who experiences this problem?
- How often does it occur?
- What is the impact if we don't solve it?
- What are customers doing today as a workaround?

### 3. Solution Exploration

**Approaches:**
- **User Story Mapping** - Map the customer journey
- **Opportunity Solution Trees** - Explore multiple solution paths
- **Competitive Analysis** - Learn from market solutions
- **Technical Spikes** - Validate feasibility
- **Prototyping** - Build quick mockups for feedback

**Collaboration:**
- Work with UX Designer for user flows and prototypes
- Consult CTO on technical feasibility and architecture
- Review with CMO for market positioning

### 4. Validation

**Methods:**
- **Customer Interviews** - Validate problem and solution fit
- **Surveys** - Quantify demand and willingness to pay
- **Prototype Testing** - Test usability and value
- **A/B Tests** - Validate hypotheses with real data
- **Beta Programs** - Launch to subset of users

**Success Criteria:**
- Clear customer pain point articulated
- Solution addresses core JTBD
- Measurable success metrics defined
- Technical feasibility confirmed
- Business value quantified

### 5. Documentation

Output: **Product Requirements Document (PRD)**

Required sections:
- Problem statement
- Target users and personas
- User stories and acceptance criteria
- Success metrics
- Technical considerations
- Go-to-market plan
- Timeline and resources

Template: `/templates/prd-template.md`

## Financial Services Considerations

### Regulatory & Compliance
- Identify regulatory requirements (FINRA, SEC, etc.)
- Document compliance needs upfront
- Involve legal/compliance team early

### Security & Privacy
- Data protection requirements
- Authentication and authorization needs
- Audit trail and reporting
- Encryption and security standards

### Risk Management
- Financial transaction accuracy
- System reliability and uptime
- Business continuity planning
- Vendor due diligence

## Discovery Cadence

- **Weekly:** Review customer feedback and support trends
- **Monthly:** Customer interview sessions (3-5 interviews)
- **Quarterly:** Market analysis and competitive review
- **Ad-hoc:** Respond to urgent business needs or regulatory changes

## Tools & Resources

- Customer interview guide: `/templates/customer-interview-guide.md`
- User story template: `/templates/user-story-template.md`
- Research report template: `/templates/research-report-template.md`
- Opportunity solution tree template: `/templates/opportunity-solution-tree.md`

## Success Metrics

- % of features validated with customer research
- Time from opportunity identification to PRD completion
- % of shipped features that meet success criteria
- Customer satisfaction with new features (NPS, CSAT)
