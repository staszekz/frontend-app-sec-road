# Browser Trust Model – Frontend Security Foundation

## What the browser protects by default
- Same-Origin Policy
- Cookie isolation (origin-based)
- Sandboxing of JS execution
- Automatic URL encoding (limited)

## What the browser DOES NOT protect
- XSS (developer responsibility)
- Business logic flaws
- Authorization decisions
- Data integrity across trust boundaries

## Implication for frontend architecture
- Frontend must treat all user-controlled input as hostile
- Frontend cannot be trusted for authorization
- Security must be enforced via architecture, not components