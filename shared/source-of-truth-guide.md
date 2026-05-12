# Source of Truth Guide

Every professional website project built with this skill system maintains three source-of-truth documents. These live in the website project's repository. Every specialist reads from them before starting work, and updates them when decisions are made.

---

## The Three Documents

### product-brain.md
**Owner:** Brand Strategist  
**Read by:** All specialists  
**Contains:** Positioning, target audience, emotional goals, core messaging, tone of voice, trust mechanisms, primary CTA

This is the strategic foundation. If something isn't in here, it hasn't been decided yet. Designers and developers treat this as the brief — it tells them who the site is for and how it should make people feel.

**When to update:** After the client intake questionnaire is returned. After any positioning or messaging decision is made.

---

### design-rules.md
**Owner:** Web Designer  
**Read by:** Web Developer, Content Writer  
**Contains:** Typography, color palette, spacing scale, button styles, component patterns, imagery direction, responsive breakpoints

This document is the visual contract. Once locked, the developer implements it exactly. No design decisions should be made during development that aren't already here.

**When to update:** During the design phase (Sprint 2). Lock it before Sprint 3 begins.

---

### technical-decisions.md
**Owner:** Web Developer  
**Read by:** Growth Specialist (for SEO/analytics setup), all specialists when referencing stack  
**Contains:** Stack choices, folder structure, naming conventions, deployment config, decisions log

Every significant technical decision gets recorded here with the reason. This prevents revisiting the same decisions and gives future agents full context.

**When to update:** Continuously during development. Always record the reason alongside the decision.

---

## How to Use These Documents in a Prompt

When starting a task, reference the relevant document explicitly:

> "Read product-brain.md and design-rules.md, then design the HeroSection component."

> "Read technical-decisions.md and design-rules.md, then implement the color palette in tailwind.config.ts."

> "Update design-rules.md with the final color palette decisions from this session."

The more specific the reference, the more consistent the output.

---

## Document Status Indicators

Use these at the top of each section within the documents:

- `TBD` — not yet decided
- `DRAFT` — proposed but not confirmed
- `LOCKED` — decided and should not change without explicit discussion

Once a section is LOCKED, no specialist should change it without flagging it first.
