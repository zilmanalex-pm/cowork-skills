# Cowork Skills

A collection of skills for Claude Cowork — installable tools that give Claude a structured, repeatable process for complex multi-step projects.

---

## What is a skill?

A skill is a set of instructions that Claude follows when working on a specific type of task. Instead of figuring out the approach from scratch each time, Claude reads the skill and follows a proven process. Think of it as a playbook for a particular kind of work.

Skills in this repo are designed to be installed in [Claude Cowork](https://claude.ai).

---

## Skills in this repo

### `professional-website-builder`

**What it does:** Guides Claude through building a complete professional service website using the BMAD framework — Business, Model, Architecture, Delivery.

**Who it's for:** Anyone building a website for a solo practitioner or small practice: therapist, coach, lawyer, consultant, accountant, nutritionist, architect, or similar.

**What you get:**
- A structured client intake questionnaire (Word document) to gather everything needed before a line is written or designed
- A brand strategy process: positioning, messaging, emotional goals, trust mechanisms
- A full information architecture: site map, user journeys, design system
- A 6-sprint delivery plan with a recommended tech stack (Next.js, Tailwind CSS, Vercel)
- Three source-of-truth documents that keep the project consistent from start to finish

**When to use it:** Say something like "I want to build a website for my [profession]" or "help me plan a professional service website" and Claude will load the skill automatically.

### `brand-strategist`

**What it does:** Takes a completed client intake questionnaire and produces a full brand strategy — positioning statement, target audience profile, emotional strategy per page, tone of voice, messaging pillars, and trust mechanisms. Everything goes into `product-brain.md`.

**Who it's for:** Use this before writing a single word of copy or making any design decisions. The designer and writer both depend on what this skill produces.

**When to use it:** Share the completed questionnaire and say "run the brand strategy" or "fill in the product brain."

---

### `web-designer`

**What it does:** Translates brand strategy into a complete visual system — typography, color palette, spacing, components, imagery direction, and responsive behavior. All decisions go into `design-rules.md`.

**Who it's for:** Use this after the brand strategy is locked. The developer reads `design-rules.md` to implement the design.

**When to use it:** "Design the site" or "set up the visual system" after `product-brain.md` is complete.

---

### `content-writer`

**What it does:** Writes all copy that appears on the site — headlines, body text, service descriptions, About page bio, FAQ answers, CTAs, and meta tags. Covers every page, in the right register, for the right audience.

**Who it's for:** Use after the brand strategy is complete. For bilingual sites, writes Hebrew and Russian as independent drafts (not translations).

**When to use it:** "Write the homepage copy," "draft the about page," "write the FAQ," or any request to write text for the site.

---

### `web-developer`

**What it does:** Implements the site using Next.js, Tailwind CSS, shadcn/ui, and Vercel. Follows a 6-sprint delivery checklist from scaffold to launch. Reads `design-rules.md` and `technical-decisions.md` to translate design into code.

**Who it's for:** Use after the design system is locked. Handles all code: components, i18n routing, forms, SEO, and deployment.

**When to use it:** "Build the site," "implement the design," or "start sprint 1."

---

### `growth-specialist`

**What it does:** Handles everything that makes the site findable — keyword strategy, on-page SEO, structured data, Google Business Profile, analytics setup, and content strategy. Covers both Hebrew and Russian audiences with separate strategies per language.

**Who it's for:** Use in parallel with the final development sprint, or immediately after launch.

**When to use it:** "Set up SEO," "add analytics," "help me get found on Google," or "what should I do after the site goes live."

---

## How to install

1. Download the `.skill` file for the skill you want
2. Open Claude Cowork
3. Go to **Settings → Skills → Install from file**
4. Select the downloaded `.skill` file

The skill will appear in your available skills list and trigger automatically when relevant.

---

## About

These skills were built as part of real projects — not as abstract templates. The `professional-website-builder` skill was developed during the Safe Harbor project, a website for a psychotherapist, and generalized from there.

Contributions and improvements welcome.
