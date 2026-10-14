---
description: i18n rules for user-facing text
globs: "**/*.{tsx,jsx,ts}"
alwaysApply: false
---

# Internationalization

- Never hardcode visible text — all user-facing strings go through i18n
- Use locale-aware formatting (`Intl`) for dates, numbers, and currency
- Translation keys should be descriptive and namespaced by feature
