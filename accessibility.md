---
description: Accessibility standards for interactive UI
globs: "**/*.{tsx,jsx}"
alwaysApply: false
---

# Accessibility

- All interactive elements need meaningful `accessibilityLabel` / `aria-label`
- Minimum touch targets: 44x44pt (iOS), 48x48dp (Android)
- WCAG AA contrast ratios for all text
- Keyboard navigable on web — visible focus indicators
- Use semantic elements (`button`, `heading`, `link`) not generic `View`/`div` with click handlers
