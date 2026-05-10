---
name: update-github-actions-workflow
description: Workflow command scaffold for update-github-actions-workflow in GKI_KernelSU_SUSFS.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /update-github-actions-workflow

Use this workflow when working on **update-github-actions-workflow** in `GKI_KernelSU_SUSFS`.

## Goal

Update or tweak one or more GitHub Actions workflow files, often for build, test, or release automation.

## Common Files

- `.github/workflows/gki-kernel.yml`
- `.github/workflows/test_release.yml`
- `.github/workflows/Auto_Trigger.yml`
- `.github/workflows/get-manager.yml`
- `.github/workflows/build-kernel-a12-5-10.yml`
- `.github/workflows/build-kernel-a13-5-10.yml`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit one or more files under .github/workflows/
- Commit with a message referencing the workflow or build process

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.