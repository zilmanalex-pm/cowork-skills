---
name: professional-website-builder
description: >
  Use this skill to plan and build a professional service website for any solo practitioner
  or small practice -- therapist, coach, lawyer, consultant, accountant, nutritionist,
  architect, or similar -- using the BMAD framework (Business, Model, Architecture, Delivery).
  Trigger whenever someone wants to build, plan, or launch a website for a professional
  service provider, mentions a "professional website", "practice website", "BMAD project",
  or asks how to structure a website for someone who sells expertise or services.
  This skill covers the full lifecycle: client intake questionnaire, brand strategy,
  content architecture, design system, frontend implementation, SEO, and deployment.
---

# Professional Website Builder (BMAD)

A structured approach to building trust-first websites for professional service providers — therapists, coaches, lawyers, consultants, and anyone else whose business depends on people trusting them before they ever make contact.

**The core insight:** a professional's website is not a portfolio. It is a trust-acquisition system. Someone lands on it already anxious about their problem and uncertain whether this particular person can help. The site's job is to resolve that uncertainty — quickly, credibly, humanly.

**Why BMAD?** The BMAD method (Business → Model → Architecture → Delivery) forces strategy before design and design before code. This prevents the most common failure mode: building something that looks nice but doesn't convert, because nobody thought about what the visitor actually needs to feel.

---

## How to use this skill

Work through the four phases in order. Each phase produces a deliverable that the next phase depends on. Never jump to design or code before the Business phase is complete.

Reference files:
- `references/phase-guides.md` — detailed step-by-step guidance for each phase
- `references/questionnaire-template.md` — template for generating the client intake questionnaire

---

## The Four Phases

### Phase 1 — BUSINESS
Establish the strategic foundation before anything is designed or built.

- Define the professional's niche and what makes them distinct
- Identify the target audience as specifically as possible
- Define the emotional outcome: what should a visitor feel within the first 5 seconds?
- Identify trust mechanisms: credentials, tone, bio, social proof, booking clarity

**Key first action:** Generate the Client Intake Questionnaire using `references/questionnaire-template.md` and collect answers before proceeding. The questionnaire covers who the professional is, who their clients are, what the site should accomplish, and what assets already exist.

**Deliverables:** Brand Strategy document, Messaging Guide, UX Goals document

---

### Phase 2 — MODEL
Define the information architecture before designing or coding anything.

- Map all content types: bio, services, specialties, FAQ, contact, booking, blog
- Define user journeys (how people will actually navigate to becoming a client)
- Build the design system: typography, spacing, colors, responsive behavior
- Define the technical model: static or CMS-driven, SEO approach, forms, localization

**Deliverables:** Site map, user journey map, Design Rules document

---

### Phase 3 — ARCHITECTURE
Set up the project structure before writing feature code.

**Recommended stack:** Next.js + Tailwind CSS + shadcn/ui + Vercel

```
/components
  /sections    -> HeroSection, BioSection, ServiceCards, FAQAccordion, ContactCTA
  /ui          -> Button, Card, Input (from shadcn)
/app
  /[lang]      -> for multilingual support if needed
/content       -> MDX or CMS-driven content
/public        -> images, fonts
```

**Deliverable:** Initialized project repo with folder structure and base component shells

---

### Phase 4 — DELIVERY (6 Sprints)

Work section by section. Never generate the whole site in one prompt.

| Sprint | Focus |
|--------|-------|
| 1 | Strategy and content architecture |
| 2 | Design system and visual direction |
| 3 | Homepage |
| 4 | Secondary pages (About, Services, FAQ, Contact) |
| 5 | SEO, accessibility, performance |
| 6 | Deployment, analytics, production polish |

---

## Three Source-of-Truth Documents

Create and maintain these throughout the project. Every Claude prompt becomes more accurate when it references one of these documents.

| Document | What it contains |
|----------|-----------------|
| **Product Brain** | Strategy, positioning, audience, emotional goals, core messaging |
| **Design Rules** | Typography, colors, spacing, component patterns, responsive rules |
| **Technical Decisions** | Stack choices, folder structure, naming conventions, deployment config |

---

## Claude Roles by Phase

Assign Claude a specific role for each task:

- **Brand Strategist** - Phase 1, positioning, tone of voice, messaging
- **UX Designer** - Phase 2, information architecture, user journeys
- **Frontend Engineer** - Phases 3-4, components and implementation
- **SEO Expert** - Phase 5, meta tags, structured data, performance
- **Accessibility Reviewer** - Phase 5, WCAG compliance, keyboard navigation

---

## Recommended Build Order

1. Professional's positioning and niche
2. Target audience definition
3. Emotional and trust strategy
4. Site structure and user journeys
5. Copywriting
6. Design system
7. Component build
8. Full implementation
9. SEO
10. Deployment
