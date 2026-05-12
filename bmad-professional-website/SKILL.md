---
name: bmad-professional-website
description: >
  Use this skill to build a professional service website (therapist, coach, lawyer, consultant,
  or similar) using the BMAD framework -- Business, Model, Architecture, Delivery.
  Trigger whenever someone says they want to build, plan, or launch a website for a professional
  service provider, a solo practitioner, or a small practice. Also trigger when someone mentions
  a "therapist website", "professional service site", "BMAD project", or asks how to structure
  or plan a professional website from scratch. This skill covers the entire lifecycle: strategy
  questionnaire, brand positioning, content architecture, design system, frontend build, SEO,
  and deployment.
---

# BMAD Professional Website Builder

A structured approach to building trust-first websites for professional service providers using the BMAD method: **B**usiness → **M**odel → **A**rchitecture → **D**elivery.

The core insight behind this skill: **the earlier the strategic thinking happens, the better the AI-generated implementation becomes**. BMAD prevents chaos, inconsistency, redesign loops, and vague prompting — because design and code serve strategy, not the other way around.

---

## How to use this skill

Work through the phases in order. Never jump to design or code before the Business phase is complete. Each phase produces a deliverable that feeds the next.

At the start of a new project, read `references/phase-guides.md` for detailed guidance on each phase. When generating the Business questionnaire, read `references/questionnaire-template.md`.

---

## The BMAD Phases

### Phase 1 — BUSINESS
The website is a **trust-acquisition and emotional reassurance system**, not a portfolio.

Before any design or code, establish:
- The practitioner's niche (anxiety, trauma, couples, burnout, etc.)
- Target audience (as specifically as possible — "adults in their 30s dealing with career transitions" beats "people who need help")
- Emotional outcome: what should a visitor feel within the first 5 seconds? (calm, safe, understood, hopeful)
- Trust mechanisms: credentials, tone of voice, bio, FAQ, booking clarity

**Deliverables:** Brand Strategy doc, Messaging Guide, UX Goals

**Key action:** Before starting, generate the Business Phase Questionnaire (see `references/questionnaire-template.md`) and collect answers from the client. Do not proceed to Phase 2 without these answers.

---

### Phase 2 — MODEL
Define the information architecture before designing or coding anything.

- Map all content types: bio, services, specialties, blog, FAQ, contact, booking, languages
- Define user journeys (e.g., Google → Blog → About → Book a call)
- Create a design system: typography, spacing, buttons, colors, responsive behavior
- Define the technical model: static vs CMS-driven, SEO strategy, forms, localization, deployment

**Deliverable:** Site map, user journey map, design system spec (the "Design Rules" source-of-truth doc)

---

### Phase 3 — ARCHITECTURE
Set up the project structure before writing feature code.

**Recommended stack:** Next.js + Tailwind CSS + shadcn/ui + Vercel

Project structure:
```
/components
  /sections    → HeroSection, TherapistBio, ServiceCards, FAQAccordion, ContactCTA
  /ui          → Button, Card, Input (from shadcn)
/app
  /[lang]      → for multilingual support
/content       → MDX or CMS-driven content
/public        → images, fonts
```

**Deliverable:** Initialized project repo, folder structure, base component shells

---

### Phase 4 — DELIVERY (6 Sprints)

Work iteratively. Never generate the whole site in one prompt. Build section by section, review each piece before continuing.

| Sprint | Focus |
|--------|-------|
| 1 | Strategy and content architecture |
| 2 | Design system and visual direction |
| 3 | Homepage implementation |
| 4 | Secondary pages (About, Services, Contact, FAQ) |
| 5 | SEO, accessibility, performance optimization |
| 6 | Deployment, analytics, production polish |

---

## Three Source-of-Truth Documents

Maintain these throughout the project. Update them as decisions are made. They prevent drift and make every Claude prompt more precise.

1. **Product Brain** — Strategy, positioning, audience, emotional goals, core messaging
2. **Design Rules** — Typography, colors, spacing, component patterns, responsive rules
3. **Technical Decisions** — Stack choices, folder structure, naming conventions, deployment config

---

## Claude Roles by Phase

Use Claude in specialized roles — one role per conversation or per task:
- **Brand Strategist** — Phase 1, messaging, tone of voice
- **UX Designer** — Phase 2, information architecture, user journeys
- **Frontend Engineer** — Phase 3–4, components and implementation
- **SEO Expert** — Phase 5, meta tags, structured data, performance
- **Accessibility Reviewer** — Phase 5, WCAG compliance, keyboard navigation

---

## Recommended Project Order

1. Positioning and niche
2. Audience definition
3. Emotional strategy
4. Site structure
5. Copywriting
6. Design system
7. Components
8. Frontend implementation
9. SEO
10. Deployment

---

## Reference Files

- `references/phase-guides.md` — Detailed step-by-step guidance for each phase
- `references/questionnaire-template.md` — Full Business Phase questionnaire structure (for generating client intake docs)
