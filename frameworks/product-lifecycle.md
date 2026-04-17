---
title: Product Development Lifecycle
description: End-to-end product delivery process from discovery through iteration
---

# Product Development Lifecycle

## Overview

This framework defines our end-to-end process for taking a product idea from discovery through delivery and iteration. We follow an iterative, agile approach while ensuring proper governance for financial services.

## Lifecycle Stages

```
Discovery → Planning → Design → Development → Testing → Launch → Iterate
     ↑                                                              ↓
     └──────────────── Feedback & Learning ────────────────────────┘
```

## Stage 1: Discovery

**Goal:** Validate that we're solving the right problem

**Activities:**
- Customer research and interviews
- Problem definition (JTBD framework)
- Market and competitive analysis
- Opportunity sizing
- Technical feasibility assessment

**Key Artifacts:**
- Research report
- Problem statement
- Opportunity brief

**Exit Criteria:**
- Clear problem definition
- Target users identified
- Business value quantified
- Technical feasibility confirmed

**Responsible:** CPO with input from CTO, UX Designer, CMO

**Framework:** See `/frameworks/discovery.md`

## Stage 2: Planning

**Goal:** Define what we're building and how we'll measure success

**Activities:**
- Write Product Requirements Document (PRD)
- Define user stories and acceptance criteria
- Identify technical architecture approach
- Set success metrics and goals
- Estimate effort and resources
- Prioritize using RICE framework
- Plan phased rollout if needed

**Key Artifacts:**
- PRD (product requirements document)
- User stories with acceptance criteria
- Technical design document
- Success metrics dashboard spec
- Project plan and timeline

**Exit Criteria:**
- PRD reviewed and approved
- Success metrics defined
- Technical approach agreed
- Resource capacity confirmed
- Roadmap slot allocated

**Responsible:** CPO (PRD), CTO (tech design), UX Designer (user flows)

**Templates:** `/templates/prd-template.md`, `/templates/user-story-template.md`

## Stage 3: Design

**Goal:** Create user experience that solves the problem elegantly

**Activities:**
- User flow mapping
- Wireframing and prototyping
- Visual design
- User testing with prototypes
- Design review and iteration
- Accessibility review
- Compliance review (financial services specific)

**Key Artifacts:**
- User flows and journey maps
- Wireframes
- High-fidelity designs
- Interactive prototypes
- Design system components
- Accessibility checklist

**Exit Criteria:**
- User flows validated with customers
- Designs meet accessibility standards
- Compliance requirements addressed
- Development-ready design specs
- Design review approved by CPO

**Responsible:** UX Designer with input from CPO and compliance

**Collaboration:** Weekly design reviews with product and engineering

## Stage 4: Development

**Goal:** Build the product with quality and security

**Activities:**
- Sprint planning
- Feature implementation
- Code reviews
- Unit and integration testing
- Security review
- Compliance controls implementation
- Documentation

**Key Artifacts:**
- Working code in version control
- Automated tests
- API documentation
- Security audit report
- Compliance checklist
- User documentation

**Exit Criteria:**
- All user stories completed
- Code review passed
- Automated tests passing (>80% coverage)
- Security review completed
- Compliance requirements met
- Documentation complete

**Responsible:** CTO and engineering team

**Methodology:** Agile/Scrum with 2-week sprints

### Financial Services Requirements

**Must-haves for every feature:**
- **Audit trail** - All actions logged for compliance
- **Access controls** - Role-based permissions
- **Data encryption** - At rest and in transit
- **Input validation** - Prevent injection attacks
- **Error handling** - Graceful failures, no data corruption
- **Transaction integrity** - ACID compliance for financial operations

## Stage 5: Testing

**Goal:** Ensure quality, reliability, and compliance before launch

**Activities:**
- **Functional Testing** - Feature works as specified
- **Integration Testing** - Works with existing systems
- **Performance Testing** - Meets SLA requirements
- **Security Testing** - Penetration testing, vulnerability scan
- **Compliance Testing** - Regulatory requirements verified
- **User Acceptance Testing (UAT)** - Real users validate the feature
- **Regression Testing** - Existing features still work

**Key Artifacts:**
- Test plans and test cases
- UAT results
- Performance benchmarks
- Security scan reports
- Compliance sign-off
- Bug reports and resolutions

**Exit Criteria:**
- All critical bugs resolved
- UAT approved by business stakeholders
- Performance meets SLA targets
- Security review passed
- Compliance approved
- Rollback plan documented

**Responsible:** QA team, compliance team, CPO (UAT coordination)

### Financial Services Testing Standards

**Critical path testing:**
- Money movement and transactions
- Calculation accuracy (returns, fees, taxes)
- Reporting accuracy
- Data integrity

**Compliance testing:**
- Regulatory reporting requirements
- Audit trail completeness
- Access controls functioning
- Data retention policies enforced

## Stage 6: Launch

**Goal:** Deploy to production with controlled rollout

**Activities:**
- **Deployment Planning** - Timing, rollback plan, monitoring
- **Phased Rollout** - Start with internal users or beta customers
- **Feature Flags** - Control who sees the new feature
- **Monitoring Setup** - Dashboards, alerts, error tracking
- **Communication** - Announce to users, train support team
- **Documentation** - Release notes, user guides, API docs

**Key Artifacts:**
- Deployment checklist
- Rollout plan
- Monitoring dashboard
- Release notes
- User communication
- Support team training materials

**Rollout Strategy:**
```
Phase 1: Internal users (10%)
Phase 2: Beta customers (25%)
Phase 3: General availability (100%)
```

**Monitoring Windows:**
- 24 hours post-deployment (intensive monitoring)
- 1 week post-deployment (daily review)
- 30 days post-deployment (success metrics review)

**Exit Criteria:**
- Successfully deployed to production
- No critical issues in monitoring
- Support team trained
- Users communicated
- Rollback plan ready

**Responsible:** CTO (deployment), CPO (communication), CMO (marketing)

## Stage 7: Iterate

**Goal:** Learn, measure, and improve continuously

**Activities:**
- **Monitor Metrics** - Track success criteria from PRD
- **Gather Feedback** - User interviews, surveys, support tickets
- **Analyze Usage** - Feature adoption, engagement, retention
- **Identify Improvements** - Bug fixes, UX refinements, enhancements
- **Plan Next Iteration** - Prioritize improvements using RICE

**Key Artifacts:**
- Success metrics dashboard
- User feedback summary
- Usage analytics report
- Iteration backlog
- Retrospective notes

**Review Cadence:**
- **Daily:** Monitor critical metrics and errors
- **Weekly:** Review user feedback and support tickets
- **30 days:** Success metrics review meeting
- **90 days:** Feature retrospective and iteration planning

**Success Criteria Review:**
- Are we meeting the success metrics defined in the PRD?
- Is the feature being adopted by target users?
- What unexpected issues or opportunities emerged?
- What improvements should we prioritise?

**Responsible:** CPO with input from entire product team

**Framework:** See `/frameworks/metrics.md`

## Cross-Stage Activities

### Compliance & Security (Continuous)
- Security review at planning, development, and testing
- Compliance check at planning, testing, and launch
- Regular security audits post-launch

### Documentation (Continuous)
- PRD during planning
- Technical docs during development
- User docs before launch
- Update docs during iteration

### Stakeholder Communication (Continuous)
- Weekly updates during development
- Demo sessions after key milestones
- Launch communications
- Post-launch metrics sharing

## Process Governance

### Stage Gates
Each stage requires explicit approval before moving forward:
- **Discovery → Planning:** CPO approves opportunity
- **Planning → Design:** CPO approves PRD
- **Design → Development:** CPO + CTO approve designs
- **Development → Testing:** CTO approves code complete
- **Testing → Launch:** CPO + Compliance approve UAT
- **Launch → Iterate:** CPO confirms successful rollout

### Decision Authority
- **CPO:** Product scope, priorities, launch timing
- **CTO:** Technical approach, architecture, deployment
- **Compliance:** Regulatory requirements, launch approval
- **CEO:** Strategic direction, major investments

## Templates & Tools

- PRD template: `/templates/prd-template.md`
- User story template: `/templates/user-story-template.md`
- Test plan template: `/templates/test-plan-template.md`
- Launch checklist: `/templates/launch-checklist.md`
- Retrospective template: `/templates/retrospective-template.md`

## Metrics

**Process Health:**
- Cycle time (discovery to launch)
- On-time delivery rate
- Defect escape rate
- Time to recovery from incidents

**Product Health:**
- Feature adoption rate
- User satisfaction (NPS, CSAT)
- Success metrics achievement rate
- Customer retention impact
