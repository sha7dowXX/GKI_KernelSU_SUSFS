```markdown
# GKI_KernelSU_SUSFS Development Patterns

> Auto-generated skill from repository analysis

## Overview

This skill teaches you the development patterns, coding conventions, and key workflows used in the `GKI_KernelSU_SUSFS` repository. The project is primarily JavaScript-based (no framework detected) and focuses on kernel patching, CI/CD automation, and documentation for KernelSU integration. You'll learn how to contribute code, manage patches, update automation workflows, and maintain documentation following the repository's conventions.

## Coding Conventions

- **File Naming:**  
  Use `snake_case` for all file names.  
  _Example:_  
  ```
  kernel_patch_manager.js
  fix_core_hook.c.patch
  ```

- **Import Style:**  
  Use relative imports for JavaScript modules.  
  _Example:_  
  ```javascript
  import { applyPatch } from './patch_utils.js';
  ```

- **Export Style:**  
  Use named exports in JavaScript files.  
  _Example:_  
  ```javascript
  export function applyPatch(patch) { ... }
  export const PATCH_VERSION = '1.2.3';
  ```

- **Commit Message Patterns:**  
  Use prefixes such as `fix:`, `ci:`, `docs:`, `chore:`, `feat:`, `style:`, `refactor:`.  
  Keep commit messages concise (average ~31 characters).  
  _Example:_  
  ```
  fix: correct selinux patch logic
  feat: add a14-6.1 kernel workflow
  docs: update README with new patch
  ```

## Workflows

### Update GitHub Actions Workflow
**Trigger:** When you need to change CI/CD behavior, add new build targets, or fix automation issues.  
**Command:** `/update-workflow`

1. Edit one or more files under `.github/workflows/`.  
   _Example:_  
   ```
   .github/workflows/gki-kernel.yml
   .github/workflows/build-kernel-a14-6-1.yml
   ```
2. Commit your changes with a message referencing the workflow or build process.  
   _Example:_  
   ```
   ci: add kernel-a15-6.6 workflow
   ```

---

### Update README Documentation
**Trigger:** When you want to update documentation for users or developers.  
**Command:** `/update-readme`

1. Edit `README.md` to reflect recent changes, document new features, or fix errors.
2. Commit with a message referencing documentation or README.  
   _Example:_  
   ```
   docs: document new patch process
   ```

---

### Patch Update (next-patch)
**Trigger:** When you need to fix or enhance kernel patching logic or compatibility.  
**Command:** `/update-patch`

1. Edit or add files in the `next-patch/` directory.  
   _Example:_  
   ```
   next-patch/fix_core_hook.c.patch
   next-patch/fix_selinux.h.patch
   ```
2. Optionally update `.github/workflows/gki-kernel.yml` to reference new/changed patches.
3. Commit with a message referencing patch or fix.  
   _Example:_  
   ```
   fix: update fix_sucompat.c.patch for a14
   ```

---

### Multi-file Release or Feature Update
**Trigger:** When releasing a new version, adding a major feature, or synchronizing multiple aspects of the project.  
**Command:** `/release-update`

1. Edit several `.github/workflows/*.yml` files as needed.
2. Edit `next-patch/*.patch` files to include new fixes or features.
3. Update `README.md` to document the changes.
4. Commit all changes together with a descriptive message.  
   _Example:_  
   ```
   feat: release kernel a15-6.6 support and update docs
   ```

## Testing Patterns

- **Test File Naming:**  
  Test files follow the pattern `*.test.*`.  
  _Example:_  
  ```
  patch_utils.test.js
  ```

- **Framework:**  
  No specific testing framework detected.  
  _Tip:_ Follow the existing test file patterns and structure for consistency.

## Commands

| Command           | Purpose                                                        |
|-------------------|----------------------------------------------------------------|
| /update-workflow  | Update or tweak GitHub Actions workflow files                  |
| /update-readme    | Update the README documentation                                |
| /update-patch     | Update or add patch files in the next-patch directory          |
| /release-update   | Coordinate a release or major feature update across workflows, patches, and docs |
```
