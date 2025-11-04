# agents.md (Proposal Framework)

Purpose: A control file that defines commands, style, and structure for building formal business proposals through an interactive interview process.
Extensible by loading supplemental rule files so each company can add templates and rules without editing this base.

Load order and overrides:
1. `./AGENTS.md`  (this file)
2. `./agentic/agents.d/*.md`  (company-specific rules, optional)
3. `./agents.local.d/*.md`  (user or machine specific, git-ignored, optional)

If two files define a command with the same `name`, the last loaded definition wins.

---

## Global defaults

- Timezone: America/Chicago
- Style: professional, direct, executive-appropriate language
- Encoding: UTF-8
- Line endings: LF
- Confirm only on destructive actions
- Use ISO timestamps `YYYY-MM-DD HH:MM`
- Currency: USD with two decimal places
- Do not create new folders from this base file

---

## Folder expectations

This base file assumes only these paths exist by default:
- `/` root with `AGENTS.md`
- `./agentic/agents.d/`
- `./agents.local.d/`
- `./agentic/tasks/`
- `./agentic/proposals/`  (contains per-proposal folders like `P-001`, `P-002`, etc.)
- `./agentic/checkpoints/`
- `./company/` (company profile, capabilities, past projects)
- `./templates/` (proposal templates, pricing databases, compliance requirements)

Company-level files in `agentic/agents.d/` may introduce additional folders if needed.

---

## Command schema

Each command must follow this schema for machine parsing and human readability:

```
name: <Trigger>
intent: <One-line purpose>
inputs: <Questions or auto-detection rules>
writes: <Files created or modified>
steps:
  - <Action 1>
  - <Action 2>
done: <What to return to chat>
```

Rules:
- `name` must be unique, case insensitive
- If `inputs` is empty, run immediately
- Never delete user content unless the command states to do so
- Only write to files under the existing folders listed above

---

## Proposal Development Workflow Commands

### 1) Do Step 1
```
name: Do Step 1
intent: Run discovery using ./agentic/tasks/01-discover-opportunity.md as instructions
inputs:
  - Determine target proposal folder with this precedence:
      1) If user explicitly specifies one in the current message, use that
      2) Else if a proposal folder was established earlier in this conversation thread, use that
      3) Else ask: "Which proposal folder under agentic/proposals should I work on? (example: P-001)"
writes: ./agentic/proposals/<proposal-folder>/<proposal-folder>-opportunity-brief.md, ./agentic/proposals/<proposal-folder>/<proposal-folder>-requirements-analysis.md
steps:
  - Read ./agentic/tasks/01-discover-opportunity.md
  - Check if proposal folder and seed file (e.g., <proposal-folder>-seed.md) exist
  - If seed file is present, read it as the initial opportunity and conduct discovery interview to clarify any gaps
  - If seed file is not present, conduct full discovery interview to gather opportunity details
  - Generate Opportunity Brief and Requirements Analysis documents
  - Write both documents to ./agentic/proposals/<proposal-folder>/ with ISO timestamps in headers
  - Cross-reference the documents in their appendices
done: Return short bullet summaries of both documents and their saved file paths
```

### 2) Do Step 2
```
name: Do Step 2
intent: Create a Scope of Work using
  - ./agentic/tasks/02-create-scope-of-work.md as instructions
  - ./company/capabilities.md (if exists) to understand company strengths and past projects
  - ./agentic/proposals/<proposal-folder>/<proposal-folder>-opportunity-brief.md as context
  - ./agentic/proposals/<proposal-folder>/<proposal-folder>-requirements-analysis.md as context
inputs:
  - Resolve proposal folder using the same precedence as Do Step 1
writes: ./agentic/proposals/<proposal-folder>/<proposal-folder>-scope-of-work.md
steps:
  - Generate a complete Scope of Work for the chosen proposal folder
  - Include project objectives, deliverables, exclusions, assumptions, constraints, and success criteria
  - Ensure alignment with company capabilities and past project patterns
done: Return the Scope of Work title, section list, and file path
```

### 3) Do Step 3
```
name: Do Step 3
intent: Generate project plan and task breakdown using
  - ./agentic/tasks/03-generate-project-plan.md as instructions
  - ./agentic/proposals/<proposal-folder>/<proposal-folder>-scope-of-work.md as context
inputs:
  - Resolve proposal folder using the same precedence as Do Step 1
writes: ./agentic/proposals/<proposal-folder>/<proposal-folder>-project-plan.md
steps:
  - Produce a structured project plan with phases, milestones, tasks, durations, dependencies, and resource requirements
  - Include critical path analysis and risk mitigation strategies
done: Return milestone count, critical path items, and file path
```

### 4) Do Step 4
```
name: Do Step 4
intent: Produce budget and resource allocation using
  - ./agentic/tasks/04-create-budget.md as instructions
  - ./templates/pricing-database.xlsx (if exists) for cost references
  - ./agentic/proposals/<proposal-folder>/<proposal-folder>-project-plan.md as context
  - ./agentic/proposals/<proposal-folder>/<proposal-folder>-scope-of-work.md as context
inputs:
  - Resolve proposal folder using the same precedence as Do Step 1
writes: ./agentic/proposals/<proposal-folder>/<proposal-folder>-budget.md
steps:
  - Create detailed budget with line items, labor costs, materials, equipment, overhead, and contingencies
  - Include pricing justifications and cost breakdown structure
  - Generate resource allocation matrix
done: Return total budget, contingency percentage, and file path
```

### 5) Do Step 5
```
name: Do Step 5
intent: Generate compliance and risk documentation using ./agentic/tasks/05-compliance-risk.md
inputs:
  - Resolve proposal folder using the same precedence as Do Step 1
writes: ./agentic/proposals/<proposal-folder>/<proposal-folder>-compliance.md, ./agentic/proposals/<proposal-folder>/<proposal-folder>-risk-register.md
steps:
  - Read ./templates/compliance-requirements.md (if exists) for regulatory standards
  - Read ./agentic/tasks/05-compliance-risk.md
  - Generate compliance documentation covering all applicable regulations, permits, certifications
  - Create risk register with mitigation strategies and contingency plans
  - Save both documents to ./agentic/proposals/<proposal-folder>/
done: Return compliance item count, high-priority risks, and file paths
```

### 6) Do Step 6
```
name: Do Step 6
intent: Compile final proposal document using
  - ./agentic/tasks/06-compile-proposal.md as instructions
inputs:
  - Resolve proposal folder using the same precedence as Do Step 1
writes: ./agentic/proposals/<proposal-folder>/<proposal-folder>-final-proposal.md
steps:
  - Read all generated documents from the proposal folder
  - Read ./templates/proposal-template.md (if exists) for formatting standards
  - Compile executive summary, company qualifications, scope, timeline, budget, compliance, and appendices
  - Apply professional formatting and ensure consistency
  - Generate table of contents and document cross-references
done: Return page count estimate, key highlights, and file path
```

---

## Document Management Commands

### Generate Executive Summary
```
name: Generate Executive Summary
intent: Create standalone executive summary from proposal documents
inputs:
  - Resolve proposal folder using standard precedence
writes: ./agentic/proposals/<proposal-folder>/<proposal-folder>-executive-summary.md
steps:
  - Read all proposal documents
  - Extract key points: opportunity, solution, value proposition, investment, timeline
  - Limit to 2 pages maximum
  - Use executive-appropriate language
done: Return summary highlights and file path
```

### Export to PDF
```
name: Export to PDF
intent: Convert proposal markdown to PDF format
inputs:
  - Ask: "Which document should I export? (final-proposal, executive-summary, or specific document name)"
  - Resolve proposal folder using standard precedence
writes: ./agentic/proposals/<proposal-folder>/exports/<document-name>.pdf
steps:
  - Create exports folder if it doesn't exist
  - Convert specified markdown document to PDF using pandoc or similar
  - Apply company branding template if available in ./templates/
done: Return PDF file path and page count
```

### Generate Budget Summary
```
name: Generate Budget Summary
intent: Create high-level budget overview for stakeholder review
inputs:
  - Resolve proposal folder using standard precedence
writes: ./agentic/proposals/<proposal-folder>/<proposal-folder>-budget-summary.md
steps:
  - Read full budget document
  - Extract major cost categories and totals
  - Create summary table with percentages
  - Highlight contingencies and assumptions
done: Return total project cost and file path
```

### Compliance Check
```
name: Compliance Check
intent: Verify proposal meets all regulatory and company requirements
inputs:
  - Resolve proposal folder using standard precedence
writes: ./agentic/proposals/<proposal-folder>/<proposal-folder>-compliance-report.md
steps:
  - Read ./templates/compliance-requirements.md
  - Review all proposal documents
  - Check for required sections, certifications, disclosures
  - Generate compliance checklist with pass/fail/missing status
done: Return compliance percentage and critical missing items
```

---

## Quality Commands

### Review Proposal
```
name: Review Proposal
intent: Comprehensive review of proposal for completeness and quality
inputs:
  - Resolve proposal folder using standard precedence
writes: ./agentic/proposals/<proposal-folder>/<proposal-folder>-review-report.md
steps:
  - Check all required documents exist
  - Verify cross-references and consistency
  - Flag missing information, unclear sections, or errors
  - Assess alignment with company standards
done: Return quality score and top 3 improvement areas
```

### Price Comparison
```
name: Price Comparison
intent: Compare proposal budget against historical data
inputs:
  - Resolve proposal folder using standard precedence
writes: none
steps:
  - Read current proposal budget
  - Read ./templates/pricing-database.xlsx or similar historical data
  - Compare line items against past projects
  - Flag significant variances (>15%)
done: Return variance summary and outlier items
```

---

## Archive and Tracking Commands

### Archive Proposal
```
name: Archive Proposal
intent: Move completed proposal to archive with metadata
inputs:
  - Resolve proposal folder using standard precedence
  - Ask: "Proposal status? (won, lost, withdrawn, on-hold)"
writes: ./archive/<proposal-folder>/, ./archive/INDEX.md
steps:
  - Create archive folder if needed
  - Move proposal folder to ./archive/
  - Add entry to ./archive/INDEX.md with date, status, value, client
done: Return archive location
```

### List Proposals
```
name: List Proposals
intent: Show all active proposals with status
inputs:
  - None
writes: none
steps:
  - Scan ./agentic/proposals/ for all proposal folders
  - Extract key metadata from each (client, value, status, last modified)
  - Display in table format sorted by last modified
done: Return proposal count and table
```

---

## Agentic Commands

### Checkpoint
```
name: Checkpoint
intent: Generate a checkpoint for the current proposal state
inputs:
  - None (auto-detect proposal state)
writes: ./agentic/checkpoints/YYYY-MM-DD_HHMM-<proposal-id>_checkpoint_vNN.md
steps:
  - Parse the current proposal state from working memory and open files
  - Generate a checkpoint documenting progress, decisions, and next actions
  - Write the file to `./agentic/checkpoints/` using this naming rule: `YYYY-MM-DD-HHMM-<proposal-id>_checkpoint_vNN.md`
  - Update or create `./agentic/checkpoints/INDEX.md` with the newest entry at the top
done: Reply with the file path written, a 3-line "Next actions" summary
```

### Restart
```
name: Restart
intent: Restart from a checkpoint
inputs:
  - Ask: "Restart from [latest_checkpoint.md]? (yes/no or specify another filename)"
writes: none
steps:
  - Read the ./agentic/checkpoints folder
  - Identify the most recent checkpoint file
  - Display a list of available checkpoints (most recent first)
  - If user says "yes", load that checkpoint's contents as the new active context
  - If user names another checkpoint, load that one instead
done: Confirm reload success and display proposal ID + objective line
```

### Show Commands
```
name: Show Commands
intent: Display all available commands from AGENTS.md and agents.d/
inputs:
  - Optional filter keyword (e.g., "Show Commands budget")
writes: none
steps:
  - Read AGENTS.md and scan for command blocks (sections starting with "name:")
  - Read all *.md files in agents.d/ and scan for command blocks
  - Extract name + intent from each command
  - If filter provided, show only commands matching the filter in name or intent
  - Group commands by category (Proposal Development, Document Management, Quality, etc.)
  - Display in formatted markdown list
done: Return categorized command list with command names and one-line intents
```

---

## Style guidelines

- GitHub-flavored Markdown for all documents
- Professional, executive-appropriate language
- Active voice preferred
- Naming conventions:
  - Proposal folders: P-001, P-002, etc.
  - Documents: <proposal-id>-<document-type>.md
  - Exports: <proposal-id>-<document-type>-YYYY-MM-DD.pdf
- Currency: Always USD with format $X,XXX.XX
- Dates: YYYY-MM-DD for ISO format, "Month DD, YYYY" for client-facing documents
- Numbers: Use commas for thousands separator (1,000 not 1000)
- Headings: Sentence case, not title case

---

## Company-Specific Configuration

**Note:** Company-specific templates, pricing, and compliance requirements are documented in `./agentic/agents.d/company-config.md`.

Add:
- Company profile and capabilities
- Pricing databases and historical cost data
- Compliance requirements by industry/region
- Standard terms and conditions
- Proposal templates and branding
- Contact information and certifications

---

## Repo structure reference

- `AGENTS.md` at repo root
- `agentic/agents.d/` for shared company rules and templates
- `agents.local.d/` for private overrides, git-ignored
- `agentic/tasks/` for task instruction files
- `agentic/proposals/` for per-proposal artifacts (folders like `P-001`, `P-002`, etc.)
- `agentic/checkpoints/` for session checkpoints
- `company/` for company profile, capabilities, past projects
- `templates/` for proposal templates, pricing databases, compliance docs
- `archive/` for completed proposals

---

## Extending with supplemental rules

Add new commands or overrides in:
- `./agentic/agents.d/` for shared, company-level rules
- `./agents.local.d/` for private overrides that should not be committed

Use the same command schema. Reuse an existing `name` to override a command. Use a new `name` to add commands.
