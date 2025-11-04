# Proposal Development Framework

An AI-assisted framework for building comprehensive, professional business proposals through structured discovery and iterative refinement.

## Overview

This framework guides executives through a systematic process to create formal proposals for large-scale projects (construction, infrastructure, consulting, etc.). Using an interactive interview approach, it helps you:

- Capture opportunity requirements and constraints
- Define clear scope of work and deliverables
- Develop detailed project plans and timelines
- Generate accurate budgets and resource allocations
- Document compliance requirements and risk mitigation
- Compile polished, client-ready proposal documents

## Quick Start

1. **Set up your company profile** in `./company/` with capabilities, past projects, and credentials
2. **Add templates** to `./templates/` for pricing databases, compliance requirements, and proposal formats
3. **Create a new proposal folder** under `./agentic/proposals/` (e.g., `P-001`)
4. **Run the 6-step workflow** using the commands in AGENTS.md

### The 6-Step Proposal Workflow

```
Do Step 1  →  Discovery & Requirements
Do Step 2  →  Scope of Work
Do Step 3  →  Project Plan & Timeline
Do Step 4  →  Budget & Resources
Do Step 5  →  Compliance & Risk
Do Step 6  →  Final Proposal Compilation
```

## Folder Structure

```
framework/
├── AGENTS.md                      # Command definitions and workflow
├── README.md                      # This file
├── agentic/
│   ├── agents.d/                  # Company-specific rules and templates
│   ├── tasks/                     # Step-by-step instruction files
│   ├── proposals/                 # Active proposals
│   │   ├── P-001/                 # Individual proposal folder
│   │   │   ├── P-001-seed.md      # Initial opportunity description (optional)
│   │   │   ├── P-001-opportunity-brief.md
│   │   │   ├── P-001-requirements-analysis.md
│   │   │   ├── P-001-scope-of-work.md
│   │   │   ├── P-001-project-plan.md
│   │   │   ├── P-001-budget.md
│   │   │   ├── P-001-compliance.md
│   │   │   ├── P-001-risk-register.md
│   │   │   ├── P-001-final-proposal.md
│   │   │   └── exports/           # PDF exports
│   │   └── P-002/
│   └── checkpoints/               # Session snapshots
├── agents.local.d/                # Private overrides (git-ignored)
├── company/                       # Company profile and capabilities
│   ├── profile.md
│   ├── capabilities.md
│   └── past-projects/
├── templates/                     # Reusable templates and databases
│   ├── proposal-template.md
│   ├── pricing-database.xlsx
│   └── compliance-requirements.md
└── archive/                       # Completed proposals
    └── INDEX.md
```

## How It Works

### Starting a New Proposal

1. **Create a proposal folder**: `mkdir -p agentic/proposals/P-001`
2. **Optional: Add a seed file** with initial opportunity details: `P-001-seed.md`
3. **Run Step 1**: `Do Step 1` and specify proposal folder `P-001`

The AI will interview you to understand:
- Client background and project context
- Technical requirements and constraints
- Budget range and timeline expectations
- Success criteria and evaluation factors
- Competitive landscape

### Building the Proposal

Each step generates specific artifacts:

**Step 1: Discovery**
- Opportunity Brief (executive summary of the opportunity)
- Requirements Analysis (detailed technical and business requirements)

**Step 2: Scope Definition**
- Scope of Work (deliverables, exclusions, assumptions)
- Success criteria and acceptance standards

**Step 3: Project Planning**
- Project Plan (phases, milestones, tasks)
- Timeline with dependencies and critical path
- Resource requirements

**Step 4: Budget Development**
- Detailed budget breakdown
- Cost justifications and assumptions
- Resource allocation matrix
- Contingency planning

**Step 5: Compliance & Risk**
- Compliance documentation (permits, certifications, regulations)
- Risk register with mitigation strategies
- Safety and quality assurance plans

**Step 6: Final Assembly**
- Compiled proposal document
- Executive summary
- Table of contents and cross-references
- Professional formatting

### Quality Control

Use built-in quality commands:

```
Review Proposal         # Comprehensive quality check
Compliance Check        # Verify regulatory requirements
Price Comparison        # Compare against historical data
Generate Executive Summary  # Create standalone summary
```

### Exporting

```
Export to PDF           # Convert to client-ready PDF
Generate Budget Summary # High-level cost overview
```

## Key Commands

See `AGENTS.md` for the complete command reference. Essential commands:

### Proposal Workflow
- `Do Step 1` through `Do Step 6` - Execute proposal development steps
- `Generate Executive Summary` - Create standalone summary
- `Export to PDF` - Generate client-ready documents

### Quality & Review
- `Review Proposal` - Quality check
- `Compliance Check` - Verify requirements
- `Price Comparison` - Validate pricing

### Management
- `List Proposals` - View all active proposals
- `Archive Proposal` - Move completed proposal to archive
- `Checkpoint` - Save current state
- `Restart` - Resume from checkpoint
- `Show Commands` - Display available commands

## Customization

### Company-Specific Templates

Add your company's templates to `./agentic/agents.d/company-config.md`:

```markdown
# Company Configuration

## Pricing Standards
- Labor rates by role
- Equipment hourly rates
- Material markup percentages
- Overhead allocation method

## Compliance Requirements
- Required certifications
- Insurance minimums
- Bond requirements
- Safety standards

## Proposal Standards
- Cover page template
- Executive summary format
- Appendix requirements
- Branding guidelines
```

### Custom Commands

Create new commands in `./agentic/agents.d/` using the command schema:

```markdown
name: Custom Command
intent: What it does
inputs: What information is needed
writes: Files it creates/modifies
steps:
  - Step 1
  - Step 2
done: What to return
```

## Best Practices

1. **Start with a seed file** - Create `<proposal-id>-seed.md` with initial opportunity details for faster discovery
2. **Use checkpoints** - Save state after major milestones or before significant revisions
3. **Maintain pricing databases** - Keep historical cost data current for accurate estimates
4. **Review before export** - Always run `Review Proposal` and `Compliance Check` before client delivery
5. **Archive completed work** - Move won/lost proposals to archive with status metadata
6. **Reuse winning patterns** - Reference past successful proposals from archive

## Example Workflow

```
# New construction proposal for municipal project

1. Create folder: P-001
2. Add seed: P-001-seed.md (project basics from RFP)
3. Run: Do Step 1
   → Interview covers site conditions, permits, timeline
4. Run: Do Step 2
   → Scope includes phasing, utilities, site work
5. Run: Do Step 3
   → 18-month timeline with 5 phases
6. Run: Do Step 4
   → $4.2M budget with 12% contingency
7. Run: Do Step 5
   → Environmental permits, OSHA compliance, risk mitigation
8. Run: Do Step 6
   → Final 45-page proposal compiled
9. Run: Review Proposal
   → 95% quality score, minor edits needed
10. Run: Export to PDF
    → Client-ready document generated
```

## Support Files

### Required in `./company/`
- Company profile and history
- Key personnel qualifications
- Past project portfolio
- Certifications and licenses
- Financial strength indicators

### Recommended in `./templates/`
- Proposal cover page template
- Pricing database (Excel or CSV)
- Compliance checklist by industry
- Standard terms and conditions
- Insurance and bonding information

## Tips for Success

**Discovery Phase**
- Be thorough in requirements gathering
- Ask about unstated constraints
- Understand client evaluation criteria
- Identify differentiators early

**Scope Development**
- Be explicit about exclusions
- Document assumptions clearly
- Define acceptance criteria upfront
- Align deliverables with client goals

**Budget Creation**
- Use historical data for validation
- Include adequate contingencies
- Justify pricing clearly
- Consider lifecycle costs

**Risk Management**
- Identify risks proactively
- Quantify impact and probability
- Define clear mitigation strategies
- Assign ownership

**Final Review**
- Verify all cross-references
- Check calculations and totals
- Ensure compliance completeness
- Review for clarity and professionalism

## Version History

- v1.0.0 - Initial release
- Framework adapted from software development methodology
- Optimized for construction, infrastructure, and consulting proposals

## License

See LICENSE file in root directory.

## Contributing

Company-specific improvements should be added to `./agentic/agents.d/` to keep the base framework clean and reusable across projects.
