# Frontend AppSec Road – Secure Frontend Architecture Journey

**From mid-level React/Next.js developer → Senior / Staff Frontend Engineer**
**Security-first mindset • System design • AI as engineering tool**

**Start:** January 2026  
**Pace:** 2–4 hours/week (realistic, long-term)  
**Location:** Chapel Hill, NC (Research Triangle tech / cyber market)  

---

## 🎯 Long-term Goal

Become a **Senior / Staff Frontend Engineer** who:
- designs **secure frontend architectures**, not just components
- understands **browser + HTTP + trust boundaries deeply**
- makes **conscious trade-offs** (security vs performance vs DX)
- uses AI for **code review, refactoring and validation**, not as a crutch

This is **not a learning repo**.
This is a **decision-making and architecture repo**.

---

## Why this repo exists

AI is rapidly automating:
- CRUD UI
- component generation
- basic refactors
- repetitive frontend work

The future belongs to engineers who:
- design secure systems (BFF, CSP, auth flows)
- understand **what the browser can and cannot protect**
- can **review and reject insecure AI-generated code**
- think in terms of **risk, trust, and boundaries**

This repository documents that journey.

---

## 2026 Roadmap

### Phase 0 — Browser & HTTP Fundamentals (Jan–Feb 2026)
Security and architecture start with fundamentals.

Focus:
- Browser internals: rendering pipeline, event loop, memory management
- HTTP deep dive:
  - cookies (SameSite, Secure, HttpOnly)
  - CSP fundamentals
  - caching (Cache-Control, ETag, CDN)
  - Same-Origin Policy

Goal:
> Understand what the browser guarantees — and what it does not.

---

### Phase 1 — Client-Side Security Fundamentals (Feb–Apr 2026)
Hands-on vulnerabilities with **system-level prevention mindset**.

Main resource:  
https://portswigger.net/web-security

Priority labs:
- XSS (reflected, stored, DOM)
- CSRF
- CORS misconfigurations
- Clickjacking

For each lab (documented in `/labs`):
- What failed?
- Why this is a *system* problem, not a component bug
- How to design the app so the issue is impossible

---

### OWASP Top 10:2025
https://owasp.org/Top10/2025/

Focus areas:
- A01 Broken Access Control
- A02 Security Misconfiguration
- A03 Injection (XSS)
- A07 Identification & Authentication Failures

Cheat Sheets:  
https://cheatsheetseries.owasp.org/

---

### Phase 2 — Frontend Architecture & Security-by-Design (Apr–Aug 2026)
This is the **core value phase**.

Topics:
- Authentication architecture:
  - BFF pattern
  - session vs JWT
  - refresh token strategy
  - token rotation
- Trust boundaries:
  - trusted vs untrusted code
  - third-party scripts isolation
- Frontend threat modeling:
  - STRIDE for frontend features
  - what user controls vs what backend trusts
- Content Security Policy:
  - nonce-based CSP
  - strict-dynamic
  - reporting & monitoring

Goal:
> Move from “fixing vulnerabilities” to “designing systems that prevent them”.

---

### Phase 3 — AI as Engineering Tool (Aug–Oct 2026)
No “prompt engineering”.
AI is integrated into daily engineering workflow.

Use cases:
- security-focused code review
- architecture critique
- refactoring validation
- detecting insecure patterns in generated code

Example AI review prompt (used in `/prompts`):

> Review the following React/Next.js code from a security and architecture perspective.
> Identify risks (XSS, auth, data exposure, CSP conflicts).
> Suggest improvements and explain trade-offs.
> Assume production-scale application.

Tools:
- Cursor
- Claude
- GPT

---

### Phase 4 — Real Projects & Market Positioning (Nov 2026 →)

#### Secure Lofi Beats Player
A real-world frontend app showcasing **security + architecture decisions**.

Features:
- strict CSP with reporting
- input sanitization
- BFF-style auth mock
- dependency auditing
- documented trade-offs (security vs DX vs complexity)

Each project README explains:
- what decision was made
- why
- alternatives considered

---

## Repo Structure

