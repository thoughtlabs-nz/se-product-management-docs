---
title: Monthly Customer Research Process
description: Process guide for monthly-customer-research
---

# Monthly Customer Research Process

## Overview

Regular customer research ensures we stay connected to user needs and validate product decisions with real customer input.

**Frequency:** Monthly

**Owner:** Chief Product Officer

**Commitment:** 3-5 customer interviews per month minimum

---

## Monthly Research Cycle

### Week 1: Planning & Recruitment

**Activities:**
- [ ] Define research goals for the month
- [ ] Identify target user segments
- [ ] Select customers to interview
- [ ] Send recruitment emails
- [ ] Schedule interview sessions

**Research Goals Examples:**
- Validate problem around [topic]
- Test new feature concept for [feature]
- Understand workflow challenges in [area]
- Gather feedback on recent launch

**Target Segments:**
- Wealth managers (high AUM)
- Broker traders (high volume)
- Portfolio administrators
- New users (< 3 months)
- Power users (daily active)

### Week 2-3: Conduct Interviews

**Schedule:**
- 3-5 interviews scheduled throughout weeks 2-3
- 45 minutes per interview
- Record with permission
- Take detailed notes

**Interview Guide:**
Use template: `/templates/customer-interview-guide.md`

**Focus Areas:**
- Current workflow and pain points
- Feature usage and satisfaction
- Unmet needs and opportunities
- Competitive alternatives
- Future needs

### Week 4: Synthesis & Action

**Activities:**
- [ ] Synthesize findings from all interviews
- [ ] Identify patterns and themes
- [ ] Document insights and quotes
- [ ] Update product hypotheses
- [ ] Share findings with team
- [ ] Plan follow-up actions

**Deliverables:**
- Research report: `/research/[month]-[topic]-research.md`
- Insights shared in weekly product review
- Recommendations for roadmap

---

## Interview Best Practices

### Before the Interview

**Preparation:**
- [ ] Research the customer (company, role, usage patterns)
- [ ] Review their support ticket history
- [ ] Check product usage data
- [ ] Prepare targeted questions
- [ ] Test recording equipment

**Scheduling:**
- Send calendar invite 1 week in advance
- Confirm 1 day before
- Provide video link (Zoom, Google Meet, etc.)
- Allocate 45-60 minutes

### During the Interview

**Structure:**
1. Introduction (5 min)
2. Context setting (5 min)
3. Current state exploration (15 min)
4. Pain points & impact (10 min)
5. Solution exploration (8 min)
6. Wrap-up (2 min)

**Remember:**
- Listen 80%, talk 20%
- Ask open-ended questions
- Dig deeper with "Why?" 5 times
- Focus on behavior, not opinions
- Capture exact quotes
- Stay curious, don't pitch

See full guide: `/templates/customer-interview-guide.md`

### After the Interview

**Same Day:**
- [ ] Review and clean up notes
- [ ] Highlight key quotes
- [ ] Note surprising insights
- [ ] Identify patterns
- [ ] Send thank-you email

**Within 1 Week:**
- [ ] Add to research synthesis
- [ ] Share highlights with team
- [ ] Update product hypotheses

---

## Research Report Template

### File Location
`/research/[YYYY-MM]-[topic]-research.md`

Example: `/research/2026-04-portfolio-rebalancing-research.md`

### Report Structure

```markdown
# [Month] [Topic] Customer Research

**Date:** [Month Year]
**Researcher:** Chief Product Officer
**Participants:** [Number] customers interviewed
**Goal:** [Research objective]

## Summary

[2-3 paragraphs summarizing key findings]

## Participants

| Name | Role | Company Type | Interview Date |
|------|------|--------------|----------------|
| [Name] | Wealth Manager | Mid-market RIA | 2026-04-05 |
| [Name] | Broker | Institutional | 2026-04-08 |

## Key Findings

### Finding 1: [Theme]

**Insight:** [What we learned]

**Evidence:**
> "[Customer quote supporting this]"
> — [Name, Role]

**Implications:**
- [What this means for product]
- [Recommended action]

### Finding 2: [Theme]
[Same structure]

## Pain Points Ranked

1. **[Pain Point 1]** - [Impact: High/Med/Low]
   - Affects [X%] of interviewees
   - Time cost: [Hours per week/month]

2. **[Pain Point 2]** - [Impact]
   - [Details]

## Feature Requests

| Feature | Frequency | Priority | Notes |
|---------|-----------|----------|-------|
| [Feature 1] | 4/5 interviews | High | [Context] |
| [Feature 2] | 3/5 interviews | Medium | [Context] |

## Jobs-to-be-Done Identified

```
When [situation],
I want to [motivation],
So I can [outcome]
```

## Recommendations

### Immediate Actions
1. [Recommendation 1]
2. [Recommendation 2]

### Roadmap Implications
- [Feature X] should be prioritized higher
- [Feature Y] validated, proceed to design
- [Feature Z] not resonating, deprioritize

### Follow-up Research Needed
- [Topic to explore further]
- [Segment to interview next]

## Appendix

### Interview Questions Used
[Link to interview guide used]

### Raw Notes
[Link to detailed notes if applicable]
```

---

## Research Cadence by Topic

### Rotating Focus Areas

**Q1:** Onboarding & activation
**Q2:** Core workflow efficiency
**Q3:** Advanced features & power users
**Q4:** Competitive analysis & market trends

**Quarterly Deep Dive:**
Pick one major area for 10+ interviews and comprehensive study

---

## Recruitment Strategies

### Internal Sources
- Customer Success Manager (CSM) referrals
- Support ticket respondents
- Recent feature adopters
- NPS survey respondents (promoters and detractors)
- Beta program participants

### Outreach Methods

**Email Template:**
```
Subject: Quick feedback on [product]?

Hi [Name],

I'm [Your Name], Chief Product Officer at [Company]. We're working to 
improve [product/feature area] and I'd love to learn from your experience.

Would you be open to a 30-minute conversation about how you use [product]? 
As a thank-you, I'll [incentive if applicable].

Your insights would be invaluable in helping us build better solutions.

Available times: [Calendly link]

Thanks,
[Your Name]
```

**Incentives (Optional):**
- Early access to new features
- Feature request priority
- Gift card ($50-100)
- Extended trial or subscription credit

### Target Mix Each Month
- 2 existing happy customers (retention, expansion)
- 1-2 customers with issues (improvement, churn prevention)
- 1 prospective customer (acquisition, market fit)
- 1 power user (advanced needs, advocacy)

---

## Analysis & Synthesis

### Pattern Recognition

**Look for:**
- Repeated phrases or words (signals importance)
- Similar stories across interviews
- Consistent pain points
- Surprising insights that challenge assumptions
- Edge cases that reveal system limitations

### Affinity Mapping

**Process:**
1. Write each insight on a virtual sticky note
2. Group related insights together
3. Name each group (theme)
4. Prioritize themes by frequency and impact

**Tools:**
- Miro or Mural
- Spreadsheet with tagging
- Simple markdown doc with categories

### Impact Assessment

For each finding, assess:
- **Frequency:** How many customers mentioned this?
- **Severity:** How big is the impact?
- **Segment:** Which user types does this affect?
- **Quantifiable:** Can we measure the time/money cost?

---

## Sharing Insights

### Weekly Product Review
- Share 1-2 key insights
- Play a compelling customer quote
- Tie to roadmap decisions

### Monthly All-Hands
- Customer story or case study
- Highlight themes from research
- Show how research informed decisions

### Research Repository
Maintain index: `/research/research-index.md`

Lists all research with:
- Date
- Topic
- Key findings
- Links to full reports

---

## Success Metrics

**Research Activity:**
- Interviews conducted per month (target: 3-5)
- Response rate to recruitment (target: >30%)
- Diversity of segments covered

**Research Impact:**
- % of features validated with customer input (target: >80%)
- Roadmap changes driven by research
- Customer satisfaction with new features

**Team Engagement:**
- % of product team observing interviews (target: >50%)
- Research insights shared per month
- Product decisions citing customer evidence

---

## Tools & Resources

**Interview Management:**
- Calendly or similar for scheduling
- Zoom or Google Meet for video calls
- Otter.ai or similar for transcription
- Note-taking template

**Analysis:**
- Miro/Mural for affinity mapping
- Spreadsheet for tracking themes
- Research repository folder

**Templates:**
- Customer interview guide: `/templates/customer-interview-guide.md`
- Research report: `/templates/research-report-template.md`
- Recruitment email: `/templates/recruitment-email-template.md`

---

## Related Processes

- Discovery framework: `/frameworks/discovery.md`
- Weekly product review: `/processes/weekly-product-review.md`
- Feature validation: `/frameworks/product-lifecycle.md`
