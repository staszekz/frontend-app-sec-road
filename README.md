# Frontend AppSec Road – Secure Frontend Architecture Journey

**From mid-level React/Next.js developer → Senior / Staff Frontend Engineer**  
**Security-first mindset • System design • AI as engineering tool**  
**Start:** January 2026  
**Pace:** 2–4 hours/week (realistic, long-term)  
**Location:** Chapel Hill, NC (Research Triangle tech / cyber market)

## Current Status (as of January 2026)

Phase 0: In progress – Browser & HTTP fundamentals  

Next milestone: First PortSwigger XSS labs + system prevention notes

## 🎯 Long-term Goal

Scope: frontend-led systems (browser, BFF, auth flows, integration layer).  
Not aiming to become a backend or pure AppSec engineer.

Become a **Senior / Staff Frontend Engineer** who:  

- designs **secure frontend architectures** , not just components  
- understands **browser + HTTP + trust boundaries deeply**  
- makes **conscious trade-offs** (security vs performance vs DX)  
- uses AI for **code review, refactoring and validation** , not as a crutch  

This is **not a learning repo** .  

This is a **decision-making and architecture repo** .

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

## 2026 Roadmap

### Phase 0 — Browser & HTTP Fundamentals (Jan–Feb 2026)

Security and architecture start with fundamentals.  

Focus:  

- Browser internals: rendering pipeline, event loop, memory management  
- HTTP deep dive:  
  * cookies (SameSite, Secure, HttpOnly)  
  * CSP fundamentals  
  * caching (Cache-Control, ETag, CDN)  
  * Same-Origin Policy  

Goal: Understand what the browser guarantees — and what it does not.  

Output:  

- short write-up per vulnerability  
- one architectural rule derived from each lab  
- one “never do this again” guideline  

**Dodatek:** Quick refresh na Next.js basics (SSR/SSG w kontekście security).

### Phase 1 — Client-Side Security Fundamentals (Feb–Apr 2026)

Hands-on vulnerabilities with **system-level prevention mindset** .  

Main resource: [https://portswigger.net/web-security](https://portswigger.net/web-security)  

Priority labs:  

- XSS (reflected, stored, DOM)  
- CSRF  
- CORS misconfigurations  
- Clickjacking  

For each lab (documented in `/labs` ):  

- What failed?  
- Why this is a *system* problem, not a component bug  
- How to design the app so the issue is impossible  

**OWASP Top 10:2025** → [https://owasp.org/Top10/2025/](https://owasp.org/Top10/2025/)  

Focus: A01 Broken Access Control, A02 Security Misconfiguration, A03 Injection, A07 Identification & Authentication Failures  

Cheat Sheets: [https://cheatsheetseries.owasp.org/](https://cheatsheetseries.owasp.org/)  

**Dodatek:** Więcej na OWASP 2025 updates.

### Phase 2 — Frontend Architecture & Security-by-Design (Apr–Aug 2026)

This is the **core value phase** .  

Topics:  

- Authentication architecture: BFF pattern, session vs JWT, refresh token strategy, token rotation  
- Trust boundaries: trusted vs untrusted code, third-party scripts isolation  
- Frontend threat modeling: STRIDE for frontend features (what user controls vs what backend trusts)  
- Content Security Policy: nonce-based, strict-dynamic, reporting & monitoring  

Goal: Move from “fixing vulnerabilities” to “designing systems that prevent them”.  

**Dodatek:** Integracja z headless CMS (np. Sanity) – secure API tokens, data validation.

### Phase 3 — AI as Engineering Tool (Aug–Oct 2026)

AI is used after human design decisions are made, not before.  
No “prompt engineering”. AI is integrated into daily engineering workflow.  

Use cases: security-focused code review, architecture critique, refactoring validation  

Example AI review prompt (used in `/prompts` ):  

> Review the following React/Next.js code from a security and architecture perspective. Identify risks (XSS, auth, data exposure, CSP conflicts). Suggest improvements and explain trade-offs. Assume production-scale application.  

Tools: Cursor, Claude, GPT  

Full master prompt → [/prompts/master-prompt.md](/staszekz/frontend-app-sec-road/blob/master/prompts/master-prompt.md)  

**Dodatek:** Prompts dla CMS/blog: "Review Sanity schema for injection risks".

### Phase 4 — Real Projects & Market Positioning (Nov 2026 →)

#### Secure Travel Blog (Next.js + Sanity)

A real-world frontend app showcasing **security + architecture decisions** , combined with personal passion for travel.  

Features:  

- Headless CMS (Sanity) for blog posts about travels (tags, galleries, maps)  
- Strict CSP with reporting  
- Input sanitization and validation (e.g. for user comments or search)  
- BFF pattern (mock backend for frontend isolation)  
- Authentication (e.g. NextAuth for user accounts)  
- Dependency auditing  
- Documented trade-offs (security vs DX vs complexity)  
- Podstrona "Lofi Beats" z embedami linków Spotify (nie hostowana muzyka – safer CSP i legal)  

Each project README explains: what decision was made, why, alternatives considered.  

**Integration with Personal Projects:** Łączy AppSec z blogiem o podróżach – np. secure handling user-generated content (relacje z tripów).

## Repo Structure

- /labs → write-ups, screenshots & system-level takeaways from PortSwigger labs  
- /projects → real apps (e.g. Secure Travel Blog) with architecture decisions & trade-offs  
- /prompts → custom AI templates (master prompt, review templates, etc.)  
- /notes → architecture sketches, threat models, HTTP/browser deep-dive summaries  
- /meta → this README + future updates  

Feel free to follow, fork or suggest resources – happy to connect with other learners/devs in RTP area!  

🔒💻✈️  

Last updated: January 2026  

## About

My journey from mid-level frontend developer to secure frontend / AppSec engineer with AI tooling support. Tracking progress: OWASP Top 10 labs (PortSwigger), secure coding practices in React/Next.js, prompt engineering for secure code generation.
