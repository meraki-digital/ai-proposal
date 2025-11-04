# Checkpoints

This folder stores checkpoint files that capture proposal development state at specific points in time.

## Purpose

Checkpoints allow you to:
- Save progress during proposal development
- Resume work from a known state
- Track decisions and rationale
- Review proposal evolution over time

## File Naming

Checkpoints follow this naming pattern:
```
YYYY-MM-DD-HHMM-<proposal-id>_checkpoint_vNN.md
```

Example: `2025-11-04-1430-P-001_checkpoint_v01.md`

## Usage

**Create a checkpoint:**
```
Checkpoint
```

**Restart from a checkpoint:**
```
Restart
```

The system will show available checkpoints and let you choose which one to reload.

## INDEX.md

An INDEX.md file is automatically maintained with entries for all checkpoints, newest first.

## Best Practices

- Create checkpoints after completing major steps
- Create checkpoints before significant revisions
- Use checkpoints when switching between proposals
- Include clear "Next actions" in each checkpoint
