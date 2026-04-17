---
title: Prioritization Framework
description: Strategic decision-making framework using RICE scoring and other methods
---

# Prioritization Framework

## Overview

This framework helps us make strategic decisions about what to build, when to build it, and what to defer. We use multiple prioritisation methods depending on the context.

## Primary Method: RICE Scoring

**RICE** = (Reach × Impact × Confidence) / Effort

### Reach
**How many users/customers will this impact in a given time period?**

Scale: Absolute numbers (users per quarter)
- 1,000+ users/quarter = High reach
- 100-1,000 users/quarter = Medium reach
- Less than 100 users/quarter = Low reach

Examples:
- Feature for all wealth managers: 500 users/quarter
- Broker-specific improvement: 200 users/quarter
- Admin tool: 20 users/quarter

### Impact
**How much will this impact each user?**

Scale: 0-3 points
- **3 = Massive** - Core workflow transformation, major pain point solved
- **2 = High** - Significant improvement, notable time savings
- **1 = Medium** - Moderate improvement, nice-to-have
- **0.5 = Low** - Minor improvement, small quality of life gain
- **0.25 = Minimal** - Barely noticeable improvement

Examples (Wealth Management):
- Automated portfolio rebalancing: 3 (massive time savings)
- Enhanced reporting dashboard: 2 (significant improvement)
- Customizable email templates: 1 (moderate improvement)
- UI colour scheme update: 0.5 (low impact)

### Confidence
**How confident are we in our Reach and Impact estimates?**

Scale: Percentage
- **100% = High** - Strong data, validated with customers, clear evidence
- **80% = Medium** - Some data, reasonable assumptions, limited validation
- **50% = Low** - Mostly assumptions, little validation, high uncertainty

Examples:
- Customer-requested feature with usage data: 100%
- Competitive feature with market research: 80%
- Internal hypothesis without validation: 50%

### Effort
**How much total work is required (product, design, engineering)?**

Scale: Person-months
- 0.5 months = Quick win (days to 2 weeks)
- 1 month = Small project (2-4 weeks)
- 2-3 months = Medium project (1-2 sprints)
- 6+ months = Large project (multi-sprint)

**Include:**
- Engineering implementation time
- Design and UX work
- Testing and QA
- Documentation
- Deployment and rollout

### RICE Score Calculation

```
RICE Score = (Reach × Impact × Confidence) / Effort
```

**Example:**
```
Feature: Automated portfolio rebalancing
Reach: 500 users/quarter
Impact: 3 (massive)
Confidence: 80%
Effort: 2 months

RICE = (500 × 3 × 0.8) / 2 = 600
```

### Prioritization Thresholds

- **RICE > 500** - High priority, schedule ASAP
- **RICE 100-500** - Medium priority, plan for next quarter
- **RICE < 100** - Low priority, backlog or defer

## Alternative Methods

### Value vs. Effort Matrix

Simple 2×2 matrix for quick prioritisation:

```
High Value, Low Effort  → Quick Wins (do first)
High Value, High Effort → Strategic Investments (plan carefully)
Low Value, Low Effort   → Fill-ins (if capacity available)
Low Value, High Effort  → Time Sinks (avoid or defer)
```

Use when:
- Need quick triage
- Limited data available
- Stakeholder alignment workshop

### MoSCoW Method

Categorize features into:
- **Must Have** - Critical for launch, non-negotiable
- **Should Have** - Important but not critical
- **Could Have** - Nice to have if resources permit
- **Won't Have** - Explicitly out of scope

Use when:
- Planning MVP or release scope
- Managing stakeholder expectations
- Deadline-driven projects

### Strategic Alignment

Score each opportunity on:
1. **Business Impact** - Revenue, cost savings, market share
2. **Customer Value** - Solves pain point, improves experience
3. **Strategic Fit** - Aligns with company vision and OKRs
4. **Competitive Advantage** - Differentiates us in market

Scale: 1-5 for each dimension
Total score: Sum of all dimensions (max 20)

Use when:
- Annual roadmap planning
- Executive decision-making
- Multi-year strategic investments

## Financial Services Considerations

### Regulatory Priority Boost
Features required for compliance get automatic priority elevation:
- **SEC/FINRA mandates** - Immediate priority
- **Regulatory best practices** - High priority
- **Audit requirements** - High priority

### Risk-Adjusted Prioritization
Consider:
- **Financial risk** - Transaction accuracy, money movement
- **Operational risk** - System stability, data integrity
- **Reputational risk** - Customer trust, brand impact

High-risk features require:
- Extra validation and testing
- Phased rollout plans
- Rollback procedures
- Compliance review

### Client Segment Weighting
Weight reach by client value:
- **Enterprise clients** - 3x multiplier
- **Mid-market clients** - 2x multiplier
- **Retail clients** - 1x multiplier

Example:
- Feature reaching 100 enterprise clients = 300 effective reach

## Prioritization Process

### 1. Intake
All opportunities go through discovery first (see `/frameworks/discovery.md`)

### 2. Scoring
Product team scores each opportunity using RICE

### 3. Review
Weekly product prioritisation session:
- Review new opportunities
- Re-score existing backlog items
- Adjust for strategic shifts

### 4. Planning
Quarterly roadmap planning:
- Select top RICE-scored items
- Balance quick wins and strategic investments
- Ensure cross-functional alignment

### 5. Communication
Share prioritisation decisions:
- Publish roadmap to stakeholders
- Explain rationale for decisions
- Manage expectations on deferred items

## OKR Alignment

Ensure prioritisation supports company OKRs:

**Example OKR Framework:**
```
Objective: Improve wealth manager productivity
KR1: Reduce portfolio review time by 40%
KR2: Increase client meetings per week by 25%
KR3: Achieve 4.5+ satisfaction score from wealth managers

→ Prioritize features that directly impact these KRs
```

## Tools & Templates

- RICE scoring spreadsheet: `/templates/rice-scoring-template.csv`
- Value vs Effort matrix: `/templates/value-effort-matrix.md`
- Prioritization workshop guide: `/templates/prioritisation-workshop.md`
- Roadmap template: `/templates/roadmap-template.md`

## Review Cadence

- **Weekly:** Product team reviews and scores new opportunities
- **Monthly:** Review prioritisation decisions with stakeholders
- **Quarterly:** Major roadmap planning and reprioritisation
- **Ad-hoc:** Urgent requests or strategic pivots
