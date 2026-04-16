---
title: Metrics & Success Framework
description: Measuring product success across discovery, delivery, and outcomes
---

# Metrics & Success Framework

## Overview

This framework defines how we measure product success across discovery, delivery, and outcomes. We use metrics to inform decisions, validate hypotheses, and demonstrate impact.

## Metrics Hierarchy

```
North Star Metric
      ↓
Product Metrics (leading indicators)
      ↓
Feature Metrics (specific success criteria)
```

## North Star Metric

**Definition:** The single metric that best captures the core value we deliver to customers.

### Example North Star Metrics (Financial Services)

**For Wealth Management Platform:**
```
Assets Under Management (AUM) actively managed per advisor
```
Why: Captures both platform adoption and advisor productivity

**For Broker Services Platform:**
```
Monthly Active Trading Value
```
Why: Reflects platform usage, liquidity, and customer engagement

**Characteristics of a good North Star:**
- Reflects customer value (not just vanity metrics)
- Measurable and trackable
- Drives business outcomes
- Aligns entire organization
- Actionable (we can influence it)

## Product Metrics Framework

### AARRR (Pirate Metrics)

**Acquisition** - How do users find us?
- New user sign-ups
- Marketing qualified leads (MQLs)
- Trial starts
- Cost per acquisition (CPA)

**Activation** - Do users have a great first experience?
- Onboarding completion rate
- Time to first value
- First transaction/action completed
- Percentage completing key setup steps

**Retention** - Do users come back?
- Daily Active Users (DAU)
- Monthly Active Users (MAU)
- DAU/MAU ratio (stickiness)
- Cohort retention curves
- Churn rate

**Revenue** - How do we make money?
- Monthly Recurring Revenue (MRR)
- Average Revenue Per User (ARPU)
- Customer Lifetime Value (LTV)
- LTV:CAC ratio
- Revenue churn vs logo churn

**Referral** - Do users tell others?
- Net Promoter Score (NPS)
- Referral rate
- Viral coefficient
- Word-of-mouth attribution

### Financial Services Specific Metrics

**Engagement Metrics:**
- Active accounts per advisor
- Transactions per day/week/month
- AUM growth rate
- Portfolio reviews completed
- Reports generated

**Efficiency Metrics:**
- Time to complete key workflows
- Manual process automation rate
- Error rate reduction
- Support ticket volume

**Business Impact:**
- Revenue per user
- Account retention rate
- Cross-sell/upsell rate
- Operational cost savings

**Quality & Compliance:**
- Transaction accuracy rate
- SLA adherence (uptime, performance)
- Compliance incidents
- Audit findings
- Security incidents

## Feature Success Criteria

For every feature, define success before building:

### 1. Usage Metrics
How many users will adopt this feature?

**Examples:**
- 60% of wealth managers use automated rebalancing within 90 days
- 80% of brokers enable real-time alerts
- 40% of clients access mobile app weekly

### 2. Outcome Metrics
What impact will it have on user behavior or business?

**Examples:**
- Reduce portfolio review time from 45 min to 15 min (66% reduction)
- Increase client meetings per advisor from 8 to 12 per week (+50%)
- Decrease trade execution errors by 80%

### 3. Satisfaction Metrics
Do users like it?

**Examples:**
- Feature satisfaction score >4/5
- NPS increase of 10+ points
- feature opt-out rate

### 4. Business Metrics
Does it drive business value?

**Examples:**
- Increase AUM per advisor by 25%
- Reduce operational costs by $100K/year
- Increase user retention by 15%

## Setting Feature Success Criteria

### Template

For feature: [Feature Name]

**Target Users:** [Who will use this?]

**Success Metrics:**
1. **Adoption:** [X%] of [user segment] will use this feature within [timeframe]
2. **Outcome:** [Metric] will improve from [baseline] to [target] ([% change])
3. **Satisfaction:** Feature will achieve [score] satisfaction rating
4. **Business Impact:** [Business metric] will improve by [% or $]

**Measurement Plan:**
- Track via [analytics tool/dashboard]
- Review frequency: [daily/weekly/monthly]
- Owner: [person responsible]

**Timeline:**
- Launch: [date]
- 30-day review: [date]
- 90-day assessment: [date]

### Example

For feature: Automated Portfolio Rebalancing

**Target Users:** Wealth managers managing 50+ client portfolios

**Success Metrics:**
1. **Adoption:** 60% of wealth managers will use automated rebalancing within 90 days
2. **Outcome:** Portfolio rebalancing time will decrease from 2 hours to 15 minutes (87% reduction)
3. **Satisfaction:** Feature will achieve 4.5/5 satisfaction score
4. **Business Impact:** AUM per advisor will increase by 20% due to capacity gains

**Measurement Plan:**
- Track via Amplitude + internal admin dashboard
- Review frequency: Weekly for first 30 days, then monthly
- Owner: CPO

**Timeline:**
- Launch: Q2 2026
- 30-day review: Check adoption trending toward 20%
- 90-day assessment: Validate all success criteria met

## Measurement Stack

### Analytics Tools
- **Product Analytics:** Amplitude, Mixpanel, or similar
- **User Behavior:** Session recordings, heatmaps
- **Business Intelligence:** Internal data warehouse
- **Customer Feedback:** NPS surveys, in-app feedback
- **Support Metrics:** Support ticket system

### Dashboards

**Executive Dashboard (CEO, Board):**
- North Star Metric
- MRR/ARR growth
- Customer acquisition and churn
- NPS score

**Product Dashboard (CPO, Product Team):**
- Feature adoption rates
- Key user flows and funnels
- A/B test results
- Success metrics for in-flight features

**Operational Dashboard (CTO, Ops Team):**
- System uptime and performance
- Error rates and incidents
- Support ticket volume
- Technical debt metrics

## Metrics Review Cadence

### Daily
- Critical system metrics (uptime, errors)
- Revenue and transaction volume
- Major incident alerts

### Weekly
- Feature adoption trends
- User engagement metrics
- A/B test progress
- Support ticket themes

### Monthly
- Product metrics deep dive
- Feature success criteria review
- Cohort retention analysis
- NPS trends

### Quarterly
- North Star Metric review
- Product-market fit assessment
- OKR progress review
- Strategic metrics alignment

## Product-Market Fit Metrics

**Signals of Product-Market Fit:**
- **40% rule:** >40% of users would be "very disappointed" if product went away
- **Retention curve flattens:** Cohorts stabilize after initial drop-off
- **Organic growth:** >40% of new users come from word-of-mouth
- **High engagement:** Users exceed expected usage patterns
- **NPS >50:** Strong customer advocacy

**Measurement:**
- Sean Ellis PMF survey (quarterly)
- Cohort retention analysis (monthly)
- Customer acquisition source tracking (ongoing)
- Usage benchmarking (quarterly)

## A/B Testing Framework

### When to A/B Test
- Uncertain which approach is better
- Controversial change
- Significant risk if wrong
- Want to measure incremental impact

### Test Design
1. **Hypothesis:** "We believe [change] will result in [outcome]"
2. **Success Metric:** Primary metric to measure
3. **Sample Size:** Calculate for statistical significance
4. **Duration:** Typically 1-2 weeks minimum
5. **Traffic Split:** Usually 50/50, sometimes 90/10 for risky changes

### Example
```
Hypothesis: We believe adding a portfolio health score
will increase engagement with rebalancing tools

Variant A (Control): Current experience
Variant B (Test): Add health score widget

Success Metric: % of users who initiate a rebalancing action
Secondary Metrics: Time on page, feature discovery rate

Sample Size: 1,000 users per variant
Duration: 2 weeks
Traffic Split: 50/50
```

## Avoiding Metrics Pitfalls

### Don't
- **Vanity metrics** - Metrics that look good but don't drive decisions
- **Too many metrics** - Focus on what matters most
- **Lack of context** - Always compare (vs. target, vs. last period, vs. cohort)
- **Ignoring segments** - Average can mask important variations
- **Short-term thinking** - Balance short-term wins with long-term health

### Do
- **Lead with outcomes** - Focus on customer and business impact
- **Segment your data** - Analyze by user type, cohort, feature usage
- **Track leading indicators** - Predict problems before they become critical
- **Set targets** - Every metric needs a goal
- **Tell stories** - Use metrics to inform narratives, not replace them

## Financial Services Metric Considerations

### Regulatory Metrics
Track for compliance and audit:
- Transaction accuracy rate (target: 99.99%)
- System uptime (SLA: 99.9%+)
- Data retention compliance
- Audit trail completeness
- Security incident response time

### Risk Metrics
Monitor for operational risk:
- Failed transaction rate
- Data discrepancy rate
- Unauthorized access attempts
- System capacity utilization
- Disaster recovery test results

### Client Trust Metrics
Critical for financial services:
- Net Promoter Score (NPS)
- Customer satisfaction (CSAT)
- Assets under management (AUM) growth
- Client retention rate
- Referral rate

## OKR Framework

Align metrics with quarterly Objectives and Key Results:

### Example OKR

**Objective:** Improve wealth manager productivity

**Key Results:**
1. Reduce average portfolio review time from 45 min to 20 min
2. Increase client meetings per advisor from 8 to 12 per week
3. Achieve 4.5+ satisfaction score from wealth managers

**Metrics Tracking:**
- Weekly: Check progress on time savings
- Monthly: Survey advisor satisfaction
- Quarterly: Assess overall objective achievement

## Templates

- Feature success criteria template: `/templates/success-criteria-template.md`
- A/B test plan template: `/templates/ab-test-template.md`
- OKR template: `/templates/okr-template.md`
- Metrics dashboard spec: `/templates/dashboard-spec-template.md`
