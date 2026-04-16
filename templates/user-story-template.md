---
title: User Story Template
description: Template for user-story-template
---

# User Story Template

## Story Format

```
As a [user type],
I want to [action],
So that [benefit/value]
```

## Example

```
As a wealth manager,
I want to automatically rebalance client portfolios based on target allocations,
So that I can maintain optimal asset allocation without manual calculations
```

---

## Complete User Story Template

### Story ID: [STORY-###]

### Title
[Brief, descriptive title]

### Story
**As a** [user type/persona]
**I want to** [action/capability]
**So that** [benefit/business value]

### Priority
- [ ] Must Have (critical for MVP)
- [ ] Should Have (important but not critical)
- [ ] Could Have (nice to have)
- [ ] Won't Have (explicitly out of scope)

### Story Points / Effort
[Estimate: 1, 2, 3, 5, 8, 13, 21]

### Acceptance Criteria

**Given** [context/precondition]
**When** [action/event]
**Then** [expected outcome]

**Examples:**

1. **Given** I am logged in as a wealth manager
   **When** I select a client portfolio with drift >5%
   **Then** The system calculates and displays rebalancing trades needed

2. **Given** I have reviewed rebalancing recommendations
   **When** I click "Execute Rebalance"
   **Then** The system generates trade orders and updates portfolio allocation

3. **Given** Rebalancing is in progress
   **When** Any trade fails
   **Then** The system rolls back all changes and notifies me of the failure

### Definition of Done

- [ ] Code implemented and peer reviewed
- [ ] Unit tests written and passing (>80% coverage)
- [ ] Integration tests passing
- [ ] Security review completed
- [ ] Compliance requirements validated
- [ ] Documentation updated
- [ ] UX reviewed and approved
- [ ] Acceptance criteria met
- [ ] QA testing completed
- [ ] Ready for deployment

### Dependencies

**Blocked By:**
- [STORY-### - Description]

**Blocks:**
- [STORY-### - Description]

**Requires:**
- [Technical dependency, service, API]
- [Design dependency, mockups, specs]

### Technical Notes

**Architecture:**
[High-level technical approach]

**APIs:**
- [API endpoints needed]
- [External services required]

**Data:**
- [Data models affected]
- [Database changes needed]

**Security:**
- [Authentication/authorization requirements]
- [Data encryption needs]
- [Audit logging requirements]

**Performance:**
- [Response time requirements]
- [Scalability considerations]

### Financial Services Considerations

**Compliance:**
- [ ] Audit trail for all actions
- [ ] Role-based access controls
- [ ] Regulatory reporting requirements

**Risk:**
- [ ] Transaction accuracy validated
- [ ] Error handling and rollback
- [ ] Business continuity addressed

**Security:**
- [ ] Data encryption (at rest and in transit)
- [ ] Input validation
- [ ] Penetration testing required

### Design Assets
- [Link to wireframes]
- [Link to user flows]
- [Link to prototypes]

### Test Scenarios

1. **Happy Path:**
   - [Describe expected normal flow]

2. **Edge Cases:**
   - [Edge case 1]
   - [Edge case 2]

3. **Error Cases:**
   - [Error scenario 1]
   - [Error scenario 2]

### Questions / Unknowns
- [ ] [Question that needs resolution]
- [ ] [Unknown that affects implementation]

---

## Story Sizing Guide

### 1 Point (XS)
- Simple UI changes
- Text/copy updates
- Minor bug fixes
- 1-2 hours of work

### 2 Points (S)
- Small feature additions
- Simple API changes
- Basic CRUD operations
- 2-4 hours of work

### 3 Points (M)
- Moderate features
- Multiple component changes
- Some backend logic
- 1 day of work

### 5 Points (L)
- Significant features
- Multiple systems involved
- Complex business logic
- 2-3 days of work

### 8 Points (XL)
- Large features
- Cross-team dependencies
- Significant complexity
- 1 week of work

### 13+ Points
- Epic-sized work
- Should be broken down into smaller stories

---

## Acceptance Criteria Checklist

### Functional
- [ ] Core functionality works as specified
- [ ] All user flows complete successfully
- [ ] Data validation works correctly
- [ ] Error messages are clear and actionable

### Non-Functional
- [ ] Performance meets requirements
- [ ] Works across supported browsers/devices
- [ ] Accessible (WCAG 2.1 AA)
- [ ] Secure (no vulnerabilities)

### Financial Services Specific
- [ ] Audit trail captured
- [ ] Compliance requirements met
- [ ] Transaction integrity maintained
- [ ] Error handling prevents data corruption

### Quality
- [ ] Unit tests passing
- [ ] Integration tests passing
- [ ] Code reviewed
- [ ] Documentation updated

---

## Related Templates

- Full PRD Template: `/templates/prd-template.md`
- Test Plan Template: `/templates/test-plan-template.md`
- Definition of Done Checklist: `/processes/definition-of-done.md`
