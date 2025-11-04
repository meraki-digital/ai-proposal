# Task 01: Discover Opportunity

## Purpose
Conduct a structured discovery interview to understand the business opportunity, client needs, and project requirements. Generate two foundational documents that will guide the entire proposal development process.

## Context
This is the first step in proposal development. You may start with a seed file containing initial opportunity details, or begin from scratch. Either way, your goal is to gather comprehensive information through conversation.

## Prerequisites
- Proposal folder exists under `./agentic/proposals/<proposal-id>/`
- Optional: `<proposal-id>-seed.md` file with initial opportunity description

## Outputs
1. `<proposal-id>-opportunity-brief.md` - Executive summary of the opportunity
2. `<proposal-id>-requirements-analysis.md` - Detailed technical and business requirements

---

## Discovery Interview Structure

### Phase 1: Opportunity Context (5-8 questions)

**Client & Project Background:**
- Who is the client? (Company name, industry, size, location)
- What is the project name and general description?
- What triggered this opportunity? (RFP, relationship, competitive bid, negotiated)
- What is the client's primary business objective for this project?
- Who are the key decision-makers and stakeholders?

**Competitive Landscape:**
- Is this a competitive bid or sole-source?
- Who are the likely competitors?
- What is our relationship history with this client?
- What differentiates us from competitors for this opportunity?

**Timeline & Budget Context:**
- What is the proposal submission deadline?
- What is the desired project start and completion timeframe?
- What is the client's budget range or expectation?
- Are there any critical milestones or deadlines?

### Phase 2: Technical Requirements (8-12 questions)

**Project Scope:**
- What are the primary deliverables?
- What is the physical location and site characteristics? (if applicable)
- What are the technical specifications or performance requirements?
- Are there any existing systems, structures, or conditions to work with?
- What are the quality standards and acceptance criteria?

**Constraints & Challenges:**
- What are the known constraints? (site access, weather, permits, existing operations)
- Are there environmental, safety, or regulatory considerations?
- What are the biggest technical risks or unknowns?
- Are there any known issues from similar past projects?

**Resources & Dependencies:**
- What client resources or support will be available?
- What third-party vendors or subcontractors might be required?
- Are there any dependencies on client deliverables or approvals?
- What equipment, materials, or specialized resources are needed?

### Phase 3: Business Requirements (6-10 questions)

**Financial Considerations:**
- What is the contract type? (fixed price, cost-plus, time and materials)
- Are there payment milestones or terms specified?
- What contingency or risk buffer is appropriate?
- Are there bonding, insurance, or financial guarantee requirements?

**Compliance & Governance:**
- What certifications, licenses, or permits are required?
- Are there specific compliance standards? (OSHA, EPA, industry-specific)
- What reporting or documentation is required?
- Are there labor, diversity, or local hiring requirements?

**Success Criteria:**
- How will the client evaluate proposals?
- What are the weighted evaluation factors? (price, experience, approach, timeline)
- What does success look like for the client?
- What are the deal-breakers or must-haves?

### Phase 4: Strategic Considerations (3-5 questions)

- Why should we pursue this opportunity?
- What is our win strategy?
- What risks should we flag for leadership approval?
- Are there any team members or past projects we should reference?
- What questions remain unanswered that we need to clarify with the client?

---

## Interview Guidelines

1. **If seed file exists:**
   - Read it first
   - Acknowledge the information provided
   - Focus questions on gaps, clarifications, and deeper details
   - Skip questions already answered in the seed file

2. **If starting from scratch:**
   - Work through all phases systematically
   - Ask 3-5 questions at a time, then pause for answers
   - Build on previous answers to ask relevant follow-ups
   - Note any assumptions you're making

3. **General approach:**
   - Use clear, professional language
   - Ask open-ended questions when possible
   - Probe for specifics when answers are vague
   - Acknowledge uncertainty - it's okay to document unknowns
   - Suggest reasonable assumptions when information is unavailable

---

## Document 1: Opportunity Brief

Create `<proposal-id>-opportunity-brief.md` with this structure:

```markdown
# Opportunity Brief: [Project Name]

**Proposal ID:** [ID]
**Client:** [Client Name]
**Prepared:** [ISO Date and Time]
**Prepared By:** [Your company name or team]

---

## Executive Summary
[2-3 paragraph overview of the opportunity, client objectives, and why we're pursuing it]

## Opportunity Overview

### Client Profile
- **Organization:** [Name, industry, size]
- **Location:** [Primary location]
- **Key Contacts:** [Decision-makers and their roles]
- **Relationship History:** [New client, repeat business, etc.]

### Project Context
- **Project Name:** [Official name]
- **Type:** [Construction, consulting, infrastructure, etc.]
- **Trigger:** [RFP, invitation, relationship]
- **Business Objective:** [Client's primary goal]

### Competitive Landscape
- **Competition Type:** [Competitive bid, sole source, negotiated]
- **Known Competitors:** [List or "Unknown"]
- **Our Differentiators:** [What sets us apart]

## Timeline & Milestones

| Milestone | Date | Notes |
|-----------|------|-------|
| Proposal Due | [Date] | [Details] |
| Project Start | [Date] | [Details] |
| Key Milestone 1 | [Date] | [Details] |
| Project Completion | [Date] | [Details] |

## Financial Overview
- **Budget Range:** [Client's expected range]
- **Contract Type:** [Fixed price, cost-plus, T&M]
- **Payment Terms:** [Milestone-based, monthly, etc.]
- **Bonding/Insurance:** [Requirements]

## Strategic Assessment

### Why We Should Pursue
[Bulleted list of strategic reasons]

### Win Strategy
[Our approach to winning this opportunity]

### Key Risks
[Major risks or concerns requiring leadership attention]

## Open Questions
[List of unanswered questions that need client clarification]

---

## Appendices
- Related Document: [Link to requirements-analysis.md]
```

---

## Document 2: Requirements Analysis

Create `<proposal-id>-requirements-analysis.md` with this structure:

```markdown
# Requirements Analysis: [Project Name]

**Proposal ID:** [ID]
**Client:** [Client Name]
**Prepared:** [ISO Date and Time]
**Prepared By:** [Your company name or team]

---

## Overview
[1-2 paragraph description of the project scope and requirements]

## Functional Requirements

### Primary Deliverables
| Deliverable | Description | Quantity/Size | Acceptance Criteria |
|-------------|-------------|---------------|---------------------|
| [Item 1] | [Details] | [Spec] | [How client measures success] |
| [Item 2] | [Details] | [Spec] | [How client measures success] |

### Performance Requirements
- **[Category 1]:** [Specific performance metrics or standards]
- **[Category 2]:** [Specific performance metrics or standards]

### Quality Standards
[Industry standards, client-specific requirements, inspection criteria]

## Technical Requirements

### Site Characteristics
[For construction/infrastructure projects - location, access, existing conditions, utilities, etc.]

### Technical Specifications
[Detailed technical specs, materials, equipment, systems, technologies required]

### Integration Requirements
[Existing systems or structures to integrate with, interfaces, compatibility needs]

## Operational Requirements

### Resource Requirements
- **Labor:** [Skill types, quantities, duration]
- **Equipment:** [Types, capacities, duration]
- **Materials:** [Key materials, quantities, specifications]
- **Subcontractors:** [Specialty trades or services needed]

### Client Support
- **Provided by Client:** [Resources, access, information client will provide]
- **Dependencies:** [What we need from client to succeed]

## Compliance Requirements

### Regulatory & Legal
- **Permits:** [List required permits]
- **Certifications:** [Required certifications or licenses]
- **Standards:** [OSHA, EPA, industry-specific regulations]
- **Labor Requirements:** [Prevailing wage, local hiring, diversity]

### Reporting & Documentation
- **Progress Reporting:** [Frequency, format, recipients]
- **Quality Documentation:** [Inspection reports, testing, certifications]
- **Financial Reporting:** [Invoicing, change orders, cost tracking]

## Constraints & Limitations

### Schedule Constraints
[Critical dates, blackout periods, seasonal limitations, coordination with other work]

### Site Constraints
[Access restrictions, working hours, noise limits, security requirements]

### Operational Constraints
[Client operations that must continue, safety zones, environmental restrictions]

### Budget Constraints
[Fixed budget, cost limitations, value engineering opportunities]

## Risk Factors

### Technical Risks
| Risk | Likelihood | Impact | Mitigation Approach |
|------|------------|--------|---------------------|
| [Risk 1] | [H/M/L] | [H/M/L] | [Initial thoughts] |
| [Risk 2] | [H/M/L] | [H/M/L] | [Initial thoughts] |

### External Risks
[Weather, supply chain, permitting delays, economic factors]

### Client-Related Risks
[Decision delays, scope changes, access issues, payment concerns]

## Success Criteria

### Client Evaluation Factors
| Factor | Weight | Our Strength | Strategy |
|--------|--------|--------------|----------|
| Price | [%] | [H/M/L] | [Approach] |
| Experience | [%] | [H/M/L] | [Approach] |
| Approach | [%] | [H/M/L] | [Approach] |
| Schedule | [%] | [H/M/L] | [Approach] |

### Project Success Metrics
[How client will measure project success once awarded and completed]

## Assumptions

### Basis of Understanding
[Key assumptions made due to incomplete information - flag for verification]

## Open Items

### Information Needed from Client
[Questions requiring client clarification before finalizing proposal]

### Internal Clarifications
[Items requiring internal team discussion or leadership decision]

---

## Appendices
- Related Document: [Link to opportunity-brief.md]
- Reference Materials: [RFP, client website, past project examples]
```

---

## Completion Checklist

Before finalizing documents:

- [ ] Both documents created with proper naming convention
- [ ] ISO timestamps in headers
- [ ] All major sections populated (use "TBD" or "Unknown" if information unavailable)
- [ ] Cross-references between documents included in appendices
- [ ] Open questions documented for client follow-up
- [ ] Assumptions clearly stated
- [ ] Risk factors identified (even if preliminary)
- [ ] Documents written in professional, clear language
- [ ] No contradictions between the two documents

---

## Tips for Effective Discovery

**Do:**
- Ask clarifying questions when answers are vague
- Document unknowns rather than guessing
- Note when assumptions are made
- Probe for hidden requirements or unstated needs
- Ask about past project failures or lessons learned
- Understand the political and relationship dynamics

**Don't:**
- Skip sections just because information is hard to gather
- Make up data or requirements
- Ignore red flags or risks
- Rush through the interview to get to proposal writing
- Forget to ask "What else should I know about this opportunity?"

**Remember:**
- Quality discovery drives proposal quality
- Time spent here saves rework later
- Unknowns now become risks later
- Client conversations during discovery build relationships
- These documents guide every subsequent step
