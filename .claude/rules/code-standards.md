---
paths:
  - "**/*.html"
  - "**/*.css"
  - "**/*.js"
  - "**/*.ts"
  - "**/*.tsx"
  - "**/*.jsx"
  - "**/*.py"
  - "**/*.go"
  - "**/*.rs"
---

# Code Standards

## Philosophy First

- Before any code change, confirm WHY this change is needed by tying it to a CLAUDE.md value
- Define the correct state before implementing (Pattern: TDD thinking)
- Do not start implementation if you cannot explain the methodology choice

## Code Quality

- Follow existing codebase conventions and patterns
- Keep change scope minimal — only make the requested change, do not "improve" surrounding code
- Security: validate user input, be aware of OWASP Top 10

## Review (Philosophy Scrum Phase 3)

- Which CLAUDE.md value does this code serve?
- Is there any decision in this code not tied to the philosophy?
- Does it touch any Prohibition?
