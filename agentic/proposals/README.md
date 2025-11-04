# Active Proposals

This folder contains all active proposal folders, organized by proposal ID.

## Structure

Each proposal gets its own folder:

```
proposals/
├── P-001/
│   ├── P-001-seed.md (optional - initial opportunity details)
│   ├── P-001-opportunity-brief.md
│   ├── P-001-requirements-analysis.md
│   ├── P-001-scope-of-work.md
│   ├── P-001-project-plan.md
│   ├── P-001-budget.md
│   ├── P-001-compliance.md
│   ├── P-001-risk-register.md
│   ├── P-001-final-proposal.md
│   └── exports/
│       └── P-001-final-proposal.pdf
├── P-002/
└── P-003/
```

## Naming Convention

- Proposal folders: `P-001`, `P-002`, `P-003`, etc.
- Documents: `<proposal-id>-<document-type>.md`
- Exports: PDF files in `exports/` subfolder

## Workflow

1. Create new folder: `mkdir P-001`
2. Optional: Add seed file with initial details
3. Run `Do Step 1` through `Do Step 6` to build proposal
4. Export final proposal to PDF
5. Archive when complete using `Archive Proposal` command

## Status Management

Use the `List Proposals` command to see all active proposals with status and metadata.
