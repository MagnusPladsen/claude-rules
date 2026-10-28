---
description: Component structure and naming conventions
globs: "**/*.{tsx,jsx}"
alwaysApply: false
paths:
  - "**/*.{tsx,jsx}"
---

# Component Conventions

- Files: `ComponentName.component.tsx`, types in `ComponentName.types.ts`
- Use `index.ts` re-exports for folder-based components
- Never use array index as React `key` — use stable identifiers
- Check for existing shared components before creating new ones
- New components follow rules immediately; edited components align opportunistically
