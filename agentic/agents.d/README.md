# Company-Specific Configuration

This folder contains company-specific rules, templates, and extensions to the base proposal framework.

## Purpose

Add custom commands, pricing standards, compliance requirements, and proposal templates specific to your organization without modifying the base AGENTS.md file.

## Usage

Create `.md` files in this folder following the command schema from AGENTS.md:

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

## Examples

- `company-config.md` - Company profile, capabilities, pricing standards
- `custom-commands.md` - Additional workflow commands
- `industry-templates.md` - Industry-specific proposal sections

## Load Order

Files in this folder are loaded after the base AGENTS.md, so you can override base commands or add new ones.
