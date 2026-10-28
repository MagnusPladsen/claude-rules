---
description: No hardcoded hex/rgb colors in components
globs: "**/*.{tsx,jsx}"
alwaysApply: false
paths:
  - "**/*.{tsx,jsx}"
---

# No Hardcoded Colors

- Use Tailwind classes for `className` color styling
- For raw hex props (icon `color`, `tintColor`), use a centralized colors export derived from your Tailwind/theme config
- Never put hex literals directly in component code
