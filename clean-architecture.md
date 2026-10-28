---
description: Clean architecture layer boundaries
globs: "**/*.cs"
alwaysApply: false
paths:
  - "**/*.cs"
---

# Clean Architecture

Standard 6-project layout with strict dependency direction:

- **Domain** — zero dependencies, pure business logic
- **Application** — depends on Domain only, defines interfaces
- **Infrastructure** — implements Application interfaces
- **Persistence** — EF Core, entities, configurations
- **Api** — controllers, middleware, DI composition root
- **Common** — shared utilities, referenced by all

Dependency direction: `Api → Application → Domain`, `Api → Infrastructure → Persistence`

Never reference a higher layer from a lower one.
