---
name: automated-css-regeneration
description: Workflow command scaffold for automated-css-regeneration in GitHub-Dark.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /automated-css-regeneration

Use this workflow when working on **automated-css-regeneration** in `GitHub-Dark`.

## Goal

Regenerates the user CSS file(s) automatically, likely after source or config changes.

## Common Files

- `github-dark.user.css`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Detect changes in source or config files
- Run CSS generation script or workflow
- Overwrite or update 'github-dark.user.css' (and sometimes related CSS files)
- Commit regenerated CSS file(s)

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.