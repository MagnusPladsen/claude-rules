---
description: Responsive layout strategy for cross-platform apps
globs: "**/*.{tsx,jsx}"
alwaysApply: false
paths:
  - "**/*.{tsx,jsx}"
---

# Responsive Web UI

- Build mobile-first, then add desktop breakpoints
- Use a `useIsDesktop()` hook for layout decisions — not `Platform.OS === "web"`
- Use `Platform.OS` only for true platform-specific behavior (camera, haptics, etc.)
- Prefer `flex-col` base + `md:flex-row` upgrades
- Constrain desktop width with `max-w-*` containers
