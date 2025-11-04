# Task 04: Create Budget

## Purpose
Develop a comprehensive, accurate budget that accounts for all project costs, demonstrates value, and provides appropriate contingencies while remaining competitive.

## Context
The budget transforms the project plan into financial terms. It must be detailed enough for internal cost control but presentable for client consumption. It directly impacts win probability and project profitability.

## Prerequisites
- Completed Step 3 (Project Plan)
- `<proposal-id>-project-plan.md` exists
- `<proposal-id>-scope-of-work.md` exists
- Optional: `./templates/pricing-database.xlsx` for historical cost references
- Company standard rates and burden factors

## Output
- `<proposal-id>-budget.md` - Comprehensive budget with justifications and resource allocation

---

## Budget Document Structure

Create `<proposal-id>-budget.md` with the following structure:

```markdown
# Project Budget: [Project Name]

**Proposal ID:** [ID]
**Client:** [Client Name]
**Project:** [Project Name]
**Prepared:** [ISO Date and Time]
**Prepared By:** [Your company name]
**Budget Type:** [Fixed Price / Cost-Plus / Time & Materials / Hybrid]
**Currency:** USD

---

## 1. Executive Budget Summary

### 1.1 Total Project Cost
| Category | Amount | % of Total |
|----------|--------|------------|
| Direct Labor | $[XXX,XXX.XX] | [XX]% |
| Equipment & Tools | $[XXX,XXX.XX] | [XX]% |
| Materials & Supplies | $[XXX,XXX.XX] | [XX]% |
| Subcontractors | $[XXX,XXX.XX] | [XX]% |
| Other Direct Costs | $[XXX,XXX.XX] | [XX]% |
| **Subtotal Direct Costs** | **$[XXX,XXX.XX]** | **[XX]%** |
| Indirect Costs (Overhead) | $[XXX,XXX.XX] | [XX]% |
| **Subtotal Before Fee** | **$[XXX,XXX.XX]** | **[XX]%** |
| Fee (Profit) | $[XXX,XXX.XX] | [XX]% |
| **Total Project Cost** | **$[X,XXX,XXX.XX]** | **100%** |

### 1.2 Budget by Phase
| Phase | Duration | Cost | % of Total |
|-------|----------|------|------------|
| Phase 1: [Name] | [X weeks] | $[XXX,XXX.XX] | [XX]% |
| Phase 2: [Name] | [X weeks] | $[XXX,XXX.XX] | [XX]% |
| Phase N: [Name] | [X weeks] | $[XXX,XXX.XX] | [XX]% |
| Project Management | [Full duration] | $[XXX,XXX.XX] | [XX]% |
| **Total** | **[X weeks]** | **$[X,XXX,XXX.XX]** | **100%** |

### 1.3 Payment Milestones
| Milestone | Date | Invoice Amount | Cumulative % |
|-----------|------|----------------|--------------|
| Contract Execution | [Date] | $[XXX,XXX.XX] | [XX]% |
| [Milestone 2] | [Date] | $[XXX,XXX.XX] | [XX]% |
| [Milestone 3] | [Date] | $[XXX,XXX.XX] | [XX]% |
| Final Completion | [Date] | $[XXX,XXX.XX] | 100% |

---

## 2. Direct Labor Costs

### 2.1 Labor Rate Structure
| Role | Standard Rate | Overtime Rate | Burden Rate | Loaded Rate |
|------|---------------|---------------|-------------|-------------|
| Project Manager | $[XX.XX]/hr | $[XX.XX]/hr | [XX]% | $[XX.XX]/hr |
| [Role 2] | $[XX.XX]/hr | $[XX.XX]/hr | [XX]% | $[XX.XX]/hr |
| [Role 3] | $[XX.XX]/hr | $[XX.XX]/hr | [XX]% | $[XX.XX]/hr |

**Burden includes:** [List items - FICA, insurance, benefits, workers comp, etc.]

### 2.2 Labor Hours by Phase and Role

#### Phase 1: [Phase Name]
| Role | Hours | Loaded Rate | Total Cost | Notes |
|------|-------|-------------|------------|-------|
| Project Manager | [XXX] | $[XX.XX] | $[XX,XXX.XX] | [X% allocation] |
| [Role 2] | [XXX] | $[XX.XX] | $[XX,XXX.XX] | [Full-time / Part-time] |
| [Role 3] | [XXX] | $[XX.XX] | $[XX,XXX.XX] | [Notes] |
| **Phase 1 Subtotal** | **[X,XXX]** | | **$[XXX,XXX.XX]** | |

#### Phase 2: [Phase Name]
[Repeat structure for each phase]

### 2.3 Total Labor Summary
| Role | Total Hours | Total Cost | % of Labor Budget |
|------|-------------|------------|-------------------|
| Project Manager | [XXX] | $[XX,XXX.XX] | [XX]% |
| [Role 2] | [XXX] | $[XX,XXX.XX] | [XX]% |
| [Role 3] | [XXX] | $[XX,XXX.XX] | [XX]% |
| **Total Direct Labor** | **[X,XXX]** | **$[XXX,XXX.XX]** | **100%** |

---

## 3. Equipment & Tools

### 3.1 Equipment Costs
| Equipment | Quantity | Duration | Rate | Total Cost | Usage Basis |
|-----------|----------|----------|------|------------|-------------|
| [Equipment 1] | [#] | [X weeks] | $[XX,XXX]/week | $[XX,XXX.XX] | Rental |
| [Equipment 2] | [#] | [X months] | $[XX,XXX]/month | $[XX,XXX.XX] | Owned - allocated cost |
| [Equipment 3] | [#] | [X days] | $[XXX]/day | $[X,XXX.XX] | Rental |

### 3.2 Tools & Small Equipment
| Category | Quantity | Unit Cost | Total Cost | Notes |
|----------|----------|-----------|------------|-------|
| Hand Tools | [Set] | $[XXX] | $[X,XXX.XX] | Consumable/lost tool allowance |
| Safety Equipment | [X workers] | $[XXX]/worker | $[XX,XXX.XX] | PPE, harnesses, etc. |
| [Other tools] | [#] | $[XXX] | $[X,XXX.XX] | [Notes] |

### 3.3 Equipment Mobilization
| Item | Cost | Notes |
|------|------|-------|
| Mobilization | $[XX,XXX.XX] | Transport equipment to site |
| Demobilization | $[XX,XXX.XX] | Return equipment from site |

**Total Equipment & Tools:** $[XXX,XXX.XX]

---

## 4. Materials & Supplies

### 4.1 Major Materials

#### [Material Category 1]
| Item | Specification | Quantity | Unit | Unit Price | Total Cost | Supplier |
|------|---------------|----------|------|------------|------------|----------|
| [Material 1] | [Spec] | [XXX] | [Each/SF/CY] | $[XX.XX] | $[XX,XXX.XX] | [Name or TBD] |
| [Material 2] | [Spec] | [XXX] | [Unit] | $[XX.XX] | $[XX,XXX.XX] | [Name or TBD] |
| **Subtotal** | | | | | **$[XX,XXX.XX]** | |

#### [Material Category 2]
[Repeat structure for each major material category]

### 4.2 Consumable Supplies
| Category | Estimated Cost | Basis |
|----------|----------------|-------|
| Office Supplies | $[X,XXX.XX] | [X months @ $XXX/month] |
| Safety Supplies | $[X,XXX.XX] | [Restocking PPE, signs, barriers] |
| Fuel & Lubricants | $[XX,XXX.XX] | [Equipment fuel consumption] |
| Miscellaneous | $[X,XXX.XX] | [Contingency for small purchases] |

### 4.3 Material Escalation & Waste
| Factor | Amount | Basis |
|--------|--------|-------|
| Material Escalation | $[XX,XXX.XX] | [X% for price increases over project duration] |
| Waste Allowance | $[XX,XXX.XX] | [X% for normal waste/damage] |

**Total Materials & Supplies:** $[XXX,XXX.XX]

---

## 5. Subcontractor Costs

### 5.1 Subcontracted Work
| Subcontractor Scope | Vendor | Cost | Payment Terms | Notes |
|---------------------|--------|------|---------------|-------|
| [Specialty Trade 1] | [Name or TBD] | $[XX,XXX.XX] | [Terms] | [Qualifications, bonds required] |
| [Specialty Trade 2] | [Name or TBD] | $[XX,XXX.XX] | [Terms] | [Notes] |
| [Service 1] | [Name or TBD] | $[XX,XXX.XX] | [Terms] | [Testing, inspection, certification] |

### 5.2 Professional Services
| Service | Provider | Cost | Notes |
|---------|----------|------|-------|
| Engineering | [Firm or TBD] | $[XX,XXX.XX] | [Design, calculations, stamped drawings] |
| Legal | [Firm or TBD] | $[X,XXX.XX] | [Contract review, claims if needed] |
| Testing/Inspection | [Firm or TBD] | $[XX,XXX.XX] | [Third-party verification] |

**Total Subcontractor Costs:** $[XXX,XXX.XX]

---

## 6. Other Direct Costs

### 6.1 Permits & Fees
| Permit/Fee | Agency | Estimated Cost | Notes |
|------------|--------|----------------|-------|
| [Permit 1] | [Agency] | $[XX,XXX.XX] | [Building permit, impact fees] |
| [Permit 2] | [Agency] | $[X,XXX.XX] | [Environmental, special use] |
| Inspection Fees | [Agency] | $[X,XXX.XX] | [Multiple inspections] |

### 6.2 Insurance & Bonds
| Type | Cost | Basis |
|------|------|-------|
| Builder's Risk | $[XX,XXX.XX] | [X% of project value] |
| Additional Insured Endorsements | $[X,XXX.XX] | [Per contract requirements] |
| Performance Bond | $[XX,XXX.XX] | [X% of contract value] |
| Payment Bond | $[XX,XXX.XX] | [X% of contract value] |

### 6.3 Travel & Logistics
| Item | Cost | Basis |
|------|------|-------|
| Personnel Travel | $[XX,XXX.XX] | [X trips @ $XXX per trip] |
| Lodging | $[XX,XXX.XX] | [X person-weeks @ $XXX/week] |
| Per Diem | $[XX,XXX.XX] | [X person-days @ $XX/day] |
| Shipping/Freight | $[XX,XXX.XX] | [Equipment and material transport] |

### 6.4 Site Operations
| Item | Cost | Basis |
|------|------|-------|
| Temporary Facilities | $[XX,XXX.XX] | [Office trailers, restrooms, fencing] |
| Utilities | $[XX,XXX.XX] | [Temporary power, water, X months] |
| Site Security | $[XX,XXX.XX] | [Security service or cameras] |
| Signage | $[X,XXX.XX] | [Project signs, safety signs] |

### 6.5 Technology & Communication
| Item | Cost | Basis |
|------|------|-------|
| Project Management Software | $[X,XXX.XX] | [Subscription for X months] |
| Communication Equipment | $[X,XXX.XX] | [Radios, satellite phones if remote] |
| Document Control | $[X,XXX.XX] | [Plan distribution, RFIs, submittals] |

**Total Other Direct Costs:** $[XXX,XXX.XX]

---

## 7. Indirect Costs (Overhead)

### 7.1 Overhead Calculation
| Method | Rate | Basis | Amount |
|--------|------|-------|--------|
| [Method] | [XX]% | Direct Labor | $[XXX,XXX.XX] |

**Overhead includes:**
- Corporate administration
- Facilities cost allocation
- IT support
- HR and recruiting
- Accounting and finance
- Business development (non-project specific)
- Depreciation of corporate assets

**Total Overhead:** $[XXX,XXX.XX]

---

## 8. Fee (Profit)

### 8.1 Fee Calculation
| Basis | Rate | Amount |
|-------|------|--------|
| Total Cost (before fee) | [XX]% | $[XXX,XXX.XX] |

**Fee Rationale:**
[Justification for fee percentage - risk level, strategic value, competitive positioning, industry norms]

---

## 9. Contingency Analysis

### 9.1 Identified Contingencies

#### Direct Cost Contingencies (Built into line items above)
| Category | Base Estimate | Contingency % | Contingency $ | Total |
|----------|---------------|---------------|---------------|-------|
| Materials | $[XXX,XXX.XX] | [X]% | $[XX,XXX.XX] | $[XXX,XXX.XX] |
| Subcontractors | $[XXX,XXX.XX] | [X]% | $[XX,XXX.XX] | $[XXX,XXX.XX] |

#### Schedule Contingency
- **Weather Days:** [X days built into schedule = $X,XXX labor cost]
- **Approval Delays:** [X weeks buffer = $X,XXX holding costs]

### 9.2 Management Reserve
**Not included in budget presented to client:**
- Project complexity factors: [Description and $ amount]
- Unknown unknowns: [X% of base = $XXX,XXX]

---

## 10. Budget Assumptions

### 10.1 Rate Assumptions
- Labor rates effective as of [date]
- Material pricing based on [source] as of [date]
- Fuel costs at $[X.XX] per gallon
- Equipment rental rates from [source]

### 10.2 Productivity Assumptions
- [X] hours per [unit of work] based on [past project or industry standard]
- Weather delays: [X] days over [Y] month period
- Learning curve: [Description if applicable]

### 10.3 Schedule Assumptions
- Project duration: [X weeks/months]
- Crew size: [Avg X workers]
- Working hours: [X hours/day, Y days/week]
- Overtime: [X hours estimated at premium rates]

### 10.4 Scope Assumptions
- All work per scope of work dated [date]
- Site conditions as described in [source]
- Client-provided items as listed in SOW Section [X]
- Permit approval within [X weeks]

### 10.5 Exclusions from Budget
- [Items specifically excluded from scope of work]
- [Client responsibilities that would impact cost if changed]
- [Potential change order items if scope changes]

---

## 11. Cost Breakdown Structure (CBS)

```
1.0 [Project Name] - $[X,XXX,XXX.XX]
  1.1 Phase 1: [Name] - $[XXX,XXX.XX]
    1.1.1 Labor - $[XXX,XXX.XX]
    1.1.2 Equipment - $[XX,XXX.XX]
    1.1.3 Materials - $[XXX,XXX.XX]
    1.1.4 Subcontractors - $[XX,XXX.XX]
    1.1.5 Other Direct - $[XX,XXX.XX]
  1.2 Phase 2: [Name] - $[XXX,XXX.XX]
    [Continue structure]
  X.0 Project Management - $[XXX,XXX.XX]
  X.1 Overhead - $[XXX,XXX.XX]
  X.2 Fee - $[XXX,XXX.XX]
```

---

## 12. Cash Flow Projection

### 12.1 Monthly Cost Projection
| Month | Labor | Equipment | Materials | Subs | Other | Monthly Total | Cumulative |
|-------|-------|-----------|-----------|------|-------|---------------|------------|
| Month 1 | $[XX,XXX] | $[XX,XXX] | $[XX,XXX] | $[XX,XXX] | $[XX,XXX] | $[XXX,XXX] | $[XXX,XXX] |
| Month 2 | $[XX,XXX] | $[XX,XXX] | $[XX,XXX] | $[XX,XXX] | $[XX,XXX] | $[XXX,XXX] | $[XXX,XXX] |
[Continue for all months]

### 12.2 Cash Flow Analysis
- **Peak Monthly Cost:** Month [X] = $[XXX,XXX]
- **Average Monthly Cost:** $[XXX,XXX]
- **Working Capital Required:** $[XXX,XXX] (based on payment terms and cost timing)

---

## 13. Value Analysis

### 13.1 Cost Comparison
| Benchmark | Cost | Source | Variance |
|-----------|------|--------|----------|
| Similar Project A | $[X.XX] per [unit] | [Company history] | [±X%] |
| Similar Project B | $[X.XX] per [unit] | [Company history] | [±X%] |
| Industry Average | $[X.XX] per [unit] | [Industry data] | [±X%] |
| **This Proposal** | **$[X.XX] per [unit]** | | |

### 13.2 Value Proposition
[Explanation of why this budget represents good value - efficiency, quality, experience, innovation]

### 13.3 Cost Drivers
**Top 5 Cost Drivers:**
1. [Driver 1]: $[XXX,XXX] ([XX]% of total)
2. [Driver 2]: $[XXX,XXX] ([XX]% of total)
3. [Driver 3]: $[XXX,XXX] ([XX]% of total)
4. [Driver 4]: $[XXX,XXX] ([XX]% of total)
5. [Driver 5]: $[XXX,XXX] ([XX]% of total)

---

## 14. Budget Control Plan

### 14.1 Cost Tracking
- **Frequency:** [Weekly/biweekly cost updates]
- **Method:** [Project accounting system, earned value management]
- **Reporting:** [Cost variance reports to client monthly]

### 14.2 Change Order Process
- **Trigger:** [Scope changes outside baseline]
- **Pricing:** [Using rates from Section 2.1 plus [X]% markup]
- **Approval:** [Thresholds and authority levels]

### 14.3 Variance Management
- **Acceptable Variance:** [±X% or $X,XXX per line item]
- **Triggers Recovery Plan:** [>X% or $XX,XXX variance]
- **Escalation:** [When total project variance exceeds ±X%]

---

## 15. Pricing Strategy

### 15.1 Competitive Positioning
[Analysis of where this budget falls relative to expected competition]

### 15.2 Risk-Adjusted Pricing
[How risks identified in project plan influenced pricing]

### 15.3 Win Strategy Alignment
[How pricing supports the overall win strategy from opportunity brief]

---

## Appendices

### Appendix A: Related Documents
- [Link to project-plan.md]
- [Link to scope-of-work.md]
- [Link to requirements-analysis.md]

### Appendix B: Supporting Calculations
- [Detailed quantity takeoffs]
- [Equipment utilization calculations]
- [Labor productivity worksheets]

### Appendix C: Vendor Quotes
- [Subcontractor quotes obtained]
- [Material supplier quotes]
- [Equipment rental quotes]

### Appendix D: Reference Pricing
- [Historical project costs used for benchmarking]
- [Industry cost databases referenced]
```

---

## Development Guidelines

### Budget Accuracy

**Use Historical Data:**
- Reference `./templates/pricing-database.xlsx` for labor productivity rates
- Review similar past projects for actual costs vs. estimates
- Apply lessons learned from cost overruns and savings

**Validate Assumptions:**
- Cross-check quantities against scope of work
- Verify hours against project plan task durations
- Confirm material quantities with technical team
- Get actual quotes for major subcontracts and materials

**Build Appropriate Contingencies:**
- Known risks: Specific contingency line items
- Complexity: [X%] for moderately complex, [Y%] for highly complex
- Schedule risk: Buffer for weather, approvals, coordination
- Keep management reserve separate (not in client-facing budget)

### Pricing Strategy

**Understand Client's Budget:**
- If client budget known, ensure you're in the ballpark
- If significantly under client budget, add value-adds
- If over budget, identify value engineering options

**Competitive Intelligence:**
- Research likely competitor pricing approaches
- Consider client's evaluation criteria (if price is [X]% of score, adjust strategy)
- Balance competitiveness with profitability

**Risk-Based Pricing:**
- Higher risk = higher contingency and fee
- Well-defined scope = can price tighter
- Unknowns = need buffer or qualifications

### Common Pitfalls

- **Under-estimating indirect costs:** Missing overhead, insurance, bonds, permits
- **Optimistic productivity:** Using ideal rates vs. realistic field conditions
- **Scope gaps:** Missing work that's implied but not explicit
- **Escalation blindness:** Ignoring material cost trends over project duration
- **Inadequate contingency:** Not protecting for normal risks
- **Missing small costs:** Death by a thousand cuts of miscellaneous items

---

## Completion Checklist

Before finalizing the Budget:

- [ ] All cost categories addressed (labor, equipment, materials, subs, other, overhead, fee)
- [ ] Labor hours match project plan resource loading
- [ ] Equipment costs match project plan equipment usage
- [ ] Material quantities validated against scope
- [ ] Subcontractor costs based on quotes or reliable estimates
- [ ] Permits, insurance, bonds included
- [ ] Overhead and fee calculated correctly
- [ ] Contingencies appropriate for risk level
- [ ] Assumptions documented
- [ ] Cash flow realistic and workable
- [ ] Budget compared to historical data and benchmarks
- [ ] Pricing strategy aligns with win strategy
- [ ] All calculations verified (double-check math!)
- [ ] Professional formatting
- [ ] ISO timestamp in header
- [ ] Cross-references to related documents

---

## Next Steps

After completing the Budget:
1. **Internal review** with estimating team and finance
2. **Reality check** with project manager who will execute
3. **Leadership approval** if budget exceeds authority threshold
4. **Proceed to Step 5** (Compliance & Risk) with cost data
5. **Prepare budget summary** for executive summary in final proposal

The budget drives pricing decisions and becomes the baseline for cost control if you win.
