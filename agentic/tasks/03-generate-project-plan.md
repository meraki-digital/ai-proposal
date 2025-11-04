# Task 03: Generate Project Plan

## Purpose
Develop a comprehensive project plan that breaks down the scope of work into executable tasks, defines sequencing and dependencies, identifies resource needs, and establishes the critical path for successful delivery.

## Context
The project plan translates the scope of work into an actionable roadmap. It demonstrates to the client that you understand the work, have a logical execution strategy, and can deliver on time.

## Prerequisites
- Completed Step 2 (Scope of Work)
- `<proposal-id>-scope-of-work.md` exists
- Understanding of resource availability and constraints

## Output
- `<proposal-id>-project-plan.md` - Detailed execution plan with tasks, timeline, and resources

---

## Project Plan Structure

Create `<proposal-id>-project-plan.md` with the following structure:

```markdown
# Project Plan: [Project Name]

**Proposal ID:** [ID]
**Client:** [Client Name]
**Project:** [Project Name]
**Prepared:** [ISO Date and Time]
**Prepared By:** [Your company name]
**Planning Horizon:** [Start Date] to [End Date]

---

## 1. Executive Summary

### 1.1 Project Overview
[1-2 paragraphs summarizing project objectives, approach, and timeline]

### 1.2 Key Metrics
- **Total Duration:** [X weeks/months]
- **Number of Phases:** [X]
- **Number of Milestones:** [X]
- **Peak Resources:** [X personnel, Y equipment units]
- **Critical Path Duration:** [X weeks/months]

### 1.3 Major Milestones
| Milestone | Target Date | Status Gate |
|-----------|-------------|-------------|
| Project Kickoff | [Date] | Contract executed, site access secured |
| [Milestone 2] | [Date] | [Completion criteria] |
| [Milestone 3] | [Date] | [Completion criteria] |
| Substantial Completion | [Date] | [All major deliverables accepted] |
| Final Closeout | [Date] | [All documentation, punchlist complete] |

---

## 2. Project Phases

### Phase 1: [Phase Name] ([Start Date] - [End Date])

**Objective:** [What this phase accomplishes]

**Duration:** [X weeks]

**Phase Overview:**
[Description of what happens during this phase and why it's structured this way]

**Key Activities:**

#### Activity 1.1: [Activity Name]
- **Duration:** [X days/weeks]
- **Owner:** [Role or name]
- **Resources Required:**
  - Personnel: [List roles and quantities]
  - Equipment: [List equipment needed]
  - Materials: [Key materials]
- **Dependencies:**
  - Predecessor: [What must complete before this starts]
  - Concurrent: [What runs in parallel]
- **Deliverables:** [What this activity produces]
- **Acceptance Criteria:** [How completion is verified]

#### Activity 1.2: [Activity Name]
[Repeat structure for each activity in the phase]

**Phase Deliverables:**
| Deliverable | Due Date | Owner | Client Review Required |
|-------------|----------|-------|------------------------|
| [Item 1] | [Date] | [Name/role] | Yes/No |
| [Item 2] | [Date] | [Name/role] | Yes/No |

**Phase Exit Criteria:**
- [Criterion 1 that must be met to proceed]
- [Criterion 2]
- [Criterion 3]

**Risks & Mitigation:**
| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| [Phase-specific risk 1] | H/M/L | H/M/L | [Strategy] |
| [Phase-specific risk 2] | H/M/L | H/M/L | [Strategy] |

---

### Phase 2: [Phase Name] ([Start Date] - [End Date])
[Repeat full structure for each phase]

---

### Phase N: [Final Phase Name] ([Start Date] - [End Date])
[Final phase including closeout activities]

---

## 3. Work Breakdown Structure (WBS)

```
1.0 [Project Name]
  1.1 [Phase 1 Name]
    1.1.1 [Work Package]
      1.1.1.1 [Task]
      1.1.1.2 [Task]
    1.1.2 [Work Package]
      1.1.2.1 [Task]
      1.1.2.2 [Task]
  1.2 [Phase 2 Name]
    1.2.1 [Work Package]
      1.2.1.1 [Task]
      1.2.1.2 [Task]
    1.2.2 [Work Package]
  [Continue for all phases]
  X.0 Project Management
    X.1 Planning & Control
    X.2 Client Communication
    X.3 Quality Management
    X.4 Risk Management
```

---

## 4. Detailed Task List

### Phase 1 Tasks

| Task ID | Task Name | Duration | Start | Finish | Owner | Dependencies | Resources |
|---------|-----------|----------|-------|--------|-------|--------------|-----------|
| 1.1.1 | [Task] | [X days] | [Date] | [Date] | [Role] | [Predecessor IDs] | [List] |
| 1.1.2 | [Task] | [X days] | [Date] | [Date] | [Role] | [1.1.1] | [List] |
| 1.1.3 | [Task] | [X days] | [Date] | [Date] | [Role] | [1.1.1] | [List] |

### Phase 2 Tasks
[Repeat for all phases]

**Notes:**
- FS = Finish-to-Start dependency
- SS = Start-to-Start dependency
- FF = Finish-to-Finish dependency
- Lag times shown in days where applicable

---

## 5. Schedule Management

### 5.1 Critical Path
The critical path consists of the following task sequence:

```
[Task ID] → [Task ID] → [Task ID] → [Task ID] → ... → Completion
Total Critical Path Duration: [X weeks/months]
```

**Critical Path Management Strategy:**
- [How you'll monitor and protect the critical path]
- [Buffer management approach]
- [Acceleration options if needed]

### 5.2 Schedule Contingency
- **Weather Days:** [X days built into schedule for weather delays]
- **Client Review Buffer:** [X days per review cycle for client approvals]
- **Permit Contingency:** [X weeks for permitting uncertainties]
- **Total Float:** [X days of float in non-critical activities]

### 5.3 Schedule Baseline
[Description of how baseline will be established and managed]

### 5.4 Schedule Monitoring
- **Update Frequency:** [Weekly, biweekly, monthly]
- **Reporting Method:** [Gantt charts, dashboards, narrative reports]
- **Variance Thresholds:** [When recovery plan is triggered]
- **Look-Ahead Window:** [Rolling X-week look-ahead maintained]

---

## 6. Resource Management

### 6.1 Resource Loading

#### Labor Resources
| Phase | Role | Quantity | Duration | Total Hours | Notes |
|-------|------|----------|----------|-------------|-------|
| Phase 1 | Project Manager | 1 | [X weeks] | [Hours] | Full-time |
| Phase 1 | [Role 2] | [#] | [X weeks] | [Hours] | [Notes] |
| Phase 2 | [Role] | [#] | [X weeks] | [Hours] | [Notes] |
[Continue for all phases and roles]

**Total Labor Hours:** [Sum]

#### Equipment Resources
| Equipment Type | Quantity | Start Date | End Date | Duration | Usage Rate |
|----------------|----------|------------|----------|----------|------------|
| [Equipment 1] | [#] | [Date] | [Date] | [X weeks] | [%] |
| [Equipment 2] | [#] | [Date] | [Date] | [X weeks] | [%] |

### 6.2 Resource Histogram
[Description of resource loading over time, peak periods, and leveling strategy]

**Peak Resource Periods:**
- **Week [X]:** [Y] personnel, [Z] equipment units
- **Week [X]:** [Y] personnel, [Z] equipment units

**Resource Constraints:**
- [Any resource availability limitations]
- [Approaches to manage constraints]

### 6.3 Procurement Plan
| Item | Type | Lead Time | Order Date | Delivery Date | Criticality |
|------|------|-----------|------------|---------------|-------------|
| [Material/Equipment 1] | [Type] | [X weeks] | [Date] | [Date] | High/Med/Low |
| [Material/Equipment 2] | [Type] | [X weeks] | [Date] | [Date] | High/Med/Low |

---

## 7. Dependencies & Interfaces

### 7.1 Client Dependencies
| Dependency | Required By | Lead Time | Risk if Delayed |
|------------|-------------|-----------|-----------------|
| [Client approval/info] | [Date] | [X weeks] | [Impact] |
| [Site access] | [Date] | [X weeks] | [Impact] |
| [Client resource] | [Date] | [X weeks] | [Impact] |

### 7.2 Third-Party Dependencies
| Party | Dependency | Required By | Coordination Plan |
|-------|------------|-------------|-------------------|
| [Utility company] | [Service] | [Date] | [How coordinated] |
| [Permit agency] | [Approval] | [Date] | [How coordinated] |
| [Other contractor] | [Work completion] | [Date] | [How coordinated] |

### 7.3 Internal Dependencies
[Cross-functional dependencies within your organization - procurement, design, fabrication, etc.]

---

## 8. Quality Management

### 8.1 Quality Milestones
| Milestone | Quality Activity | Success Criteria | Owner |
|-----------|------------------|------------------|-------|
| [Milestone 1] | [Inspection, test, review] | [Pass criteria] | [Role] |
| [Milestone 2] | [QA activity] | [Pass criteria] | [Role] |

### 8.2 Quality Control Points
[Description of when and how quality will be verified throughout the project]

### 8.3 Testing & Commissioning
[If applicable - testing plans, commissioning activities, performance validation]

---

## 9. Communication Plan

### 9.1 Regular Meetings
| Meeting | Frequency | Participants | Purpose | Duration |
|---------|-----------|--------------|---------|----------|
| Project Status | [Weekly] | [Client PM, Our PM] | Status update | 1 hour |
| Team Standup | [Daily] | [Project team] | Coordination | 15 min |
| Executive Review | [Monthly] | [Executives] | High-level status | 1 hour |

### 9.2 Reporting Schedule
| Report | Frequency | Recipients | Content |
|--------|-----------|------------|---------|
| Progress Report | [Weekly] | [Client stakeholders] | Status, schedule, issues |
| Financial Report | [Monthly] | [Client finance] | Budget, invoicing |
| Risk Report | [Monthly] | [Client PM] | Risk status, mitigations |

### 9.3 Escalation Procedures
[How and when issues are escalated, escalation path, response time expectations]

---

## 10. Risk Management

### 10.1 Risk Register
| ID | Risk Description | Category | Probability | Impact | Score | Mitigation Strategy | Owner | Status |
|----|------------------|----------|-------------|--------|-------|---------------------|-------|--------|
| R-001 | [Risk 1] | [Schedule/Cost/Technical] | H/M/L | H/M/L | [#] | [Strategy] | [Name] | Active |
| R-002 | [Risk 2] | [Category] | H/M/L | H/M/L | [#] | [Strategy] | [Name] | Active |

**Risk Scoring:** High=3, Medium=2, Low=1; Score = Probability × Impact

### 10.2 Risk Response Plans
**High-Priority Risks (Score ≥ 6):**

#### Risk ID: [ID] - [Risk Name]
- **Description:** [Detailed description]
- **Triggers:** [Early warning signs]
- **Avoidance:** [How to prevent]
- **Mitigation:** [How to reduce likelihood or impact]
- **Contingency:** [Plan if risk occurs]
- **Owner:** [Who monitors and responds]
- **Budget Impact:** [Contingency allocation if applicable]

### 10.3 Risk Monitoring
[How risks will be tracked, reviewed, and updated throughout the project]

---

## 11. Change Management

### 11.1 Change Control Process
1. **Identification:** [How changes are identified]
2. **Documentation:** [Change request form/process]
3. **Impact Analysis:** [Schedule, cost, scope impact assessment]
4. **Approval:** [Who approves, thresholds]
5. **Implementation:** [How approved changes are incorporated]
6. **Communication:** [How changes are communicated]

### 11.2 Baseline Management
[How the project baseline is established, protected, and updated]

---

## 12. Closeout Plan

### 12.1 Closeout Activities
| Activity | Start | Duration | Owner | Deliverable |
|----------|-------|----------|-------|-------------|
| Punchlist Development | [Date] | [X days] | [Role] | Punchlist document |
| Final Inspections | [Date] | [X days] | [Role] | Inspection reports |
| As-Built Documentation | [Date] | [X days] | [Role] | Final drawings/docs |
| Training Delivery | [Date] | [X days] | [Role] | Training materials |
| Warranty Documentation | [Date] | [X days] | [Role] | Warranty package |
| Final Billing | [Date] | [X days] | [Role] | Final invoice |
| Lessons Learned | [Date] | [X days] | [Role] | LL document |

### 12.2 Acceptance Criteria
[Final acceptance criteria and procedure]

### 12.3 Transition to Operations
[If applicable - how project transitions to operational phase or client ownership]

---

## 13. Success Metrics

### 13.1 Schedule Performance
- **On-Time Delivery:** [Target: 100% of milestones within ±X days]
- **Schedule Variance:** [Target: <X% variance from baseline]
- **Critical Path Adherence:** [Target: Zero critical path delays]

### 13.2 Quality Performance
- **First-Time Quality:** [Target: X% of deliverables accepted without rework]
- **Defect Rate:** [Target: <X defects per deliverable]
- **Inspection Pass Rate:** [Target: >X% pass rate]

### 13.3 Safety Performance
- **Recordable Incidents:** [Target: Zero]
- **Near-Miss Reporting:** [Target: >X near-misses reported monthly - indicates engagement]
- **Safety Training:** [Target: 100% completion]

### 13.4 Client Satisfaction
- **Communication Rating:** [Target: ≥X/5]
- **Responsiveness:** [Target: <X hours to respond to inquiries]
- **Overall Satisfaction:** [Target: ≥X/5]

---

## Appendices

### Appendix A: Related Documents
- [Link to scope-of-work.md]
- [Link to opportunity-brief.md]
- [Link to requirements-analysis.md]

### Appendix B: Supporting Schedules
- [Gantt chart (if created)]
- [Network diagram (if created)]
- [Resource histograms (if created)]

### Appendix C: Reference Information
- [Company project management methodology]
- [Industry scheduling standards]
```

---

## Development Guidelines

### Planning Principles

**Be Realistic:**
- Use actual historical data from past projects
- Don't compress durations beyond what's achievable
- Build in appropriate buffers and contingencies
- Account for learning curves and ramp-up time

**Be Logical:**
- Sequence activities in a practical order
- Identify and respect dependencies
- Consider resource constraints and availability
- Plan for predictable delays (weather, approvals, etc.)

**Be Detailed:**
- Break work down to manageable task sizes (typically 1-2 weeks)
- Define clear completion criteria for each task
- Assign ownership to every task
- Quantify resource needs specifically

**Be Client-Focused:**
- Highlight client decision points and review periods
- Show how you'll minimize client disruption
- Demonstrate understanding of client constraints
- Align milestones with client priorities

### Common Planning Pitfalls

- **Over-optimistic durations:** Not accounting for reality of execution
- **Missing dependencies:** Creating impossible parallel paths
- **Insufficient detail:** Tasks too large to manage or price
- **Ignoring constraints:** Planning work during blackout periods or without necessary resources
- **Unrealistic critical path:** Making everything critical vs. identifying true drivers
- **Poor resource loading:** Assuming unlimited resources or ignoring peaks/valleys

### Leveraging Past Projects

- Review similar projects from `./company/past-projects/`
- Use actual duration data rather than estimates
- Learn from what went wrong in past projects
- Apply lessons learned to risk mitigation
- Reference proven sequencing and methodologies

---

## Completion Checklist

Before finalizing the Project Plan:

- [ ] All phases defined with clear objectives and exit criteria
- [ ] Activities broken down to manageable task level
- [ ] Dependencies identified and logical
- [ ] Resources quantified for all major activities
- [ ] Critical path identified and realistic
- [ ] Contingencies and buffers included
- [ ] Client dependencies clearly called out
- [ ] Quality control points integrated
- [ ] Communication plan defined
- [ ] Risk register populated with mitigation strategies
- [ ] Closeout activities planned
- [ ] Success metrics defined and measurable
- [ ] Aligns with scope of work
- [ ] Timeline meets client expectations
- [ ] Professional formatting and language
- [ ] ISO timestamp in header
- [ ] Cross-references to related documents

---

## Next Steps

After completing the Project Plan:
1. **Validate resource assumptions** with your team
2. **Review critical path** with experienced PMs
3. **Verify client dependencies** with client if possible
4. **Use plan to drive budget** in Step 4 (resource hours × rates)
5. **Prepare for project plan presentation** if proposal includes oral component

The project plan demonstrates execution capability and becomes the foundation for project control if you win.
