---
name: release-version-bump-and-bundle
description: Workflow command scaffold for release-version-bump-and-bundle in GitHub-Dark.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /release-version-bump-and-bundle

Use this workflow when working on **release-version-bump-and-bundle** in `GitHub-Dark`.

## Goal

Prepares a new release by bumping version, updating package.json, and bundling regenerated CSS files.

## Common Files

- `package.json`
- `github-dark.user.css`
- `github-custom-fonts.user.css`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Update version in package.json
- Regenerate CSS files (github-dark.user.css, github-custom-fonts.user.css)
- Commit updated package.json and CSS files

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.