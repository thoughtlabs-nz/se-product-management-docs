---
title: Framework Summary
description: Comprehensive overview of product management frameworks for financial services
---

# Product Management Framework - Summary

**Version:** 1.0  
**Created:** April 2026  
**Owner:** Chief Product Officer  
**Status:** Active

---

## Overview

This document provides a comprehensive summary of our Product Management Framework, designed specifically for financial services (broker services and wealth management). The framework ensures we build exceptional products through systematic discovery, prioritization, delivery, and measurement.

---

## Framework Components

### 1. Core Frameworks

#### Product Discovery (`/frameworks/discovery.md`)
**Purpose:** Identify and validate product opportunities

**Key Methods:**
- Jobs-to-be-Done (JTBD) framework
- Customer interviews and research
- Opportunity solution trees
- User story mapping
- Prototype testing and validation

**Outputs:** Product Requirements Documents (PRDs)

**Cadence:** Ongoing discovery with monthly customer research

---

#### Prioritization (`/frameworks/prioritization.md`)
**Purpose:** Make strategic decisions about what to build

**Primary Method:** RICE Scoring
```
RICE = (Reach × Impact × Confidence) / Effort
```

**Alternative Methods:**
- Value vs. Effort matrix
- MoSCoW (Must/Should/Could/Won't)
- Strategic alignment scoring

**Financial Services Adjustments:**
- Regulatory priority boost
- Risk-adjusted prioritization
- Client segment weighting (Enterprise 3x, Mid-market 2x, Retail 1x)

---

#### Product Development Lifecycle (`/frameworks/product-lifecycle.md`)
**Purpose:** End-to-end process from idea to iteration

**Stages:**
1. **Discovery** - Validate the problem
2. **Planning** - Define what to build
3. **Design** - Create user experience
4. **Development** - Build with quality
5. **Testing** - Ensure reliability
6. **Launch** - Deploy with control
7. **Iterate** - Learn and improve

**Financial Services Requirements:**
- Audit trails for all actions
- Role-based access controls
- Data encryption (at rest and in transit)
- Transaction integrity (ACID compliance)
- Compliance review at multiple stages

---

#### Metrics & Success (`/frameworks/metrics.md`)
**Purpose:** Measure product success and inform decisions

**Metrics Hierarchy:**
- North Star Metric (top-level value indicator)
- Product Metrics (AARRR: Acquisition, Activation, Retention, Revenue, Referral)
- Feature Success Criteria (usage, outcome, satisfaction, business impact)

**Key Frameworks:**
- OKRs (Objectives and Key Results)
- Product-Market Fit assessment
- A/B testing methodology
- Cohort retention analysis

**Financial Services Metrics:**
- Regulatory compliance metrics (99.99% transaction accuracy)
- Risk metrics (security incidents, system uptime)
- Client trust metrics (NPS, AUM growth, retention)

---

### 2. Templates

All templates support the frameworks above and ensure consistency:

| Template | Purpose | Location |
|----------|---------|----------|
| PRD Template | Document product requirements | `/templates/prd-template.md` |
| User Story Template | Define features as user stories | `/templates/user-story-template.md` |
| Customer Interview Guide | Conduct effective research | `/templates/customer-interview-guide.md` |
| Roadmap Template | Plan quarterly/annual roadmaps | `/templates/roadmap-template.md` |

---

### 3. Processes & Rituals

#### Weekly Product Review (`/processes/weekly-product-review.md`)
**Purpose:** Tactical alignment on product progress and decisions

**Frequency:** Every Monday at 9am (automated routine)

**Agenda:**
1. Metrics review (10 min)
2. In-flight features status (15 min)
3. Customer feedback & insights (10 min)
4. Prioritization & roadmap updates (15 min)
5. Decisions & action items (5 min)
6. Q&A (5 min)

**Automated Routine:** Active (trigger ID: 0e67f12a-1894-4774-acab-e07711b1ccd6)

---

#### Monthly Customer Research (`/processes/monthly-customer-research.md`)
**Purpose:** Stay connected to user needs through regular research

**Frequency:** First of each month (automated routine)

**Commitment:** 3-5 customer interviews per month

**Process:**
- Week 1: Planning & recruitment
- Weeks 2-3: Conduct interviews
- Week 4: Synthesis & action

**Outputs:** Monthly research reports in `/research/`

**Automated Routine:** Active (trigger ID: 381d3ce5-b772-4dc8-afbe-f8d43f5e7604)

---

#### Quarterly Roadmap Planning (`/processes/quarterly-roadmap-planning.md`)
**Purpose:** Strategic planning for upcoming quarter

**Timing:** 4 weeks before quarter start

**Timeline:**
- Week 1: Data gathering & analysis
- Week 2: Opportunity prioritization
- Week 3: Roadmap drafting & alignment
- Week 4: Finalization & communication

**Outputs:** Committed quarterly roadmap with PRDs

---

### 4. Domain Expertise: Financial Services

Our framework is tailored for **broker services** and **wealth management** with specific considerations:

#### Regulatory & Compliance
- SEC, FINRA, state regulations
- Audit trail requirements
- Regulatory reporting obligations
- Compliance review gates in lifecycle

#### Security & Privacy
- Data protection (PII, financial data)
- Encryption standards
- Authentication (MFA, SSO)
- Access controls (role-based permissions)

#### Risk Management
- Financial risk (transaction accuracy, money movement)
- Operational risk (system stability, disaster recovery)
- Reputational risk (customer trust, brand impact)
- Risk-adjusted prioritization

#### Client Expectations
- High reliability (99.9%+ uptime SLAs)
- Transaction accuracy (99.99%+ target)
- Data security and privacy
- Responsive support

---

## How to Use This Framework

### For New Features

1. **Start with Discovery** (`/frameworks/discovery.md`)
   - Identify the problem through customer research
   - Define JTBD and validate with users
   - Document in PRD using `/templates/prd-template.md`

2. **Prioritize** (`/frameworks/prioritization.md`)
   - Score using RICE framework
   - Adjust for financial services considerations
   - Review in weekly product review meeting

3. **Follow the Lifecycle** (`/frameworks/product-lifecycle.md`)
   - Plan → Design → Develop → Test → Launch → Iterate
   - Complete stage gates and approvals
   - Ensure compliance at each stage

4. **Measure Success** (`/frameworks/metrics.md`)
   - Define success criteria in PRD
   - Track metrics from launch
   - Review at 30, 60, 90 days

### For Product Managers

**Daily:**
- Check product metrics dashboard
- Review customer feedback
- Support in-flight features

**Weekly:**
- Participate in weekly product review (Monday 9am)
- Update feature status and roadmap
- Prioritize new opportunities

**Monthly:**
- Conduct 3-5 customer interviews
- Synthesize research findings
- Review and update roadmap

**Quarterly:**
- Lead roadmap planning process
- Set OKRs for next quarter
- Conduct retrospective

---

## Success Metrics

We measure framework effectiveness through:

### Process Health
- **Cycle time:** Discovery to launch (target: < 90 days for medium features)
- **On-time delivery:** % of committed features shipped on schedule (target: >80%)
- **Customer validation:** % of features validated with research (target: >80%)

### Product Outcomes
- **Feature adoption:** % of target users adopting within 90 days (target: >60%)
- **Success criteria met:** % of features meeting defined success metrics (target: >75%)
- **Customer satisfaction:** NPS for new features (target: >50)

### Business Impact
- **North Star Metric growth:** Aligned with company OKRs
- **Revenue impact:** Measurable contribution to MRR/ARR
- **Cost savings:** Quantified operational efficiency gains

---

## Active Routines

| Routine | Schedule | Purpose | Status |
|---------|----------|---------|--------|
| Weekly Product Review | Every Monday 9am ET | Review metrics, status, prioritization | ✅ Active |
| Monthly Customer Research | 1st of each month 9am ET | Conduct customer interviews and synthesis | ✅ Active |

**Next Scheduled:**
- Weekly Product Review: April 20, 2026 at 9:00am ET
- Monthly Customer Research: May 1, 2026 at 9:00am ET

---

## Team Roles & Responsibilities

### Chief Product Officer (CPO)
- **Strategy:** Define product vision and roadmap
- **Discovery:** Lead customer research and opportunity validation
- **Delivery:** Own product lifecycle from idea to launch
- **Leadership:** Collaborate with CEO, CTO, UX Designer, CMO
- **Excellence:** Establish and evolve PM frameworks

### Product Team (Future Hires)
As the organization scales, consider hiring:

**Product Manager (IC)**
- Focus: Execute on specific product areas
- Responsibilities: PRDs, user stories, feature delivery
- Skills: Customer empathy, analytical, execution-focused

**Product Operations Specialist**
- Focus: Process optimization, tools, analytics
- Responsibilities: Dashboards, reporting, process improvement
- Skills: Data analysis, operational excellence, tool expertise

**Technical Product Manager**
- Focus: API products, platform, integrations
- Responsibilities: API design, developer experience, technical docs
- Skills: Technical background, API design, developer empathy

**Product Marketing Manager** (if not in CMO org)
- Focus: Go-to-market, positioning, launches
- Responsibilities: Launch plans, messaging, sales enablement
- Skills: Marketing, communication, storytelling

---

## Next Steps

### Immediate (Q2 2026)
- [ ] Begin weekly product review routine (starting April 20)
- [ ] Conduct first monthly customer research cycle (May 1)
- [ ] Create initial product roadmap for Q2/Q3 2026
- [ ] Identify and prioritize first features to build

### Near-term (Q3 2026)
- [ ] Establish metrics dashboards
- [ ] Complete 3+ customer research cycles
- [ ] Deliver first features using this framework
- [ ] Measure and iterate on framework effectiveness

### Future (Q4 2026+)
- [ ] Scale product team based on needs
- [ ] Evolve framework based on learnings
- [ ] Expand to additional product areas
- [ ] Build product management community of practice

---

## Resources & References

### Internal Documentation
- Framework files: `/product-management/frameworks/`
- Templates: `/product-management/templates/`
- Processes: `/product-management/processes/`
- Research: `/product-management/research/`
- Roadmaps: `/product-management/roadmaps/`
- Metrics: `/product-management/metrics/`

### External Resources
- Product Management best practices
- Financial services regulatory guidance
- Industry benchmarks and standards
- Product management community resources

---

## Version History

| Version | Date | Changes | Author |
|---------|------|---------|--------|
| 1.0 | 2026-04-13 | Initial framework creation | Chief Product Officer |

---

## Feedback & Iteration

This framework is a living document. We welcome feedback and will iterate based on:
- Team experience and learnings
- Product outcomes and success
- Organizational growth and changes
- Industry evolution and best practices

**How to suggest improvements:**
- Propose changes in weekly product review
- Submit formal feedback to CPO
- Share learnings from retrospectives
- Contribute templates or process improvements

---

*This framework supports our goal: To build exceptional product management capabilities in the financial services sector for broker services and wealth management.*
