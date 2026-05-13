# Session Starter Templates

Copy the relevant block at the start of each new Cowork chat.
Replace anything in [brackets] with the actual task.

---

## Brand Strategist

Use when: Sonya's questionnaire answers have arrived. Run this once to fill in product-brain.md.

```
We're working on the Safe Harbor project — a website for Sonya Zilman, a psychotherapist
working with Hebrew and Russian-speaking clients in Israel.

You are the Brand Strategist.

Please read:
- skills/brand-strategist/SKILL.md
- safe-harbor-website/product-brain.md (note what is TBD)
- skills/shared/source-of-truth-guide.md

The completed questionnaire is attached / pasted below.

Your task: read the questionnaire answers completely, then fill in every TBD section
in product-brain.md. Use LOCKED for confirmed decisions, DRAFT for proposals that
need Sonya's confirmation. Leave nothing as TBD.
```

---

## Web Designer

Use when: product-brain.md has no TBDs. Run this to complete design-rules.md.

```
We're working on the Safe Harbor project — a website for Sonya Zilman, a psychotherapist
working with Hebrew and Russian-speaking clients in Israel.

You are the Web Designer.

Please read:
- skills/web-designer/SKILL.md
- safe-harbor-website/product-brain.md
- safe-harbor-website/design-rules.md (note what is DRAFT or TBD)
- skills/shared/source-of-truth-guide.md

Your task: [describe what to work on — e.g. "lock the typography scale",
"define component patterns", "complete the full design-rules.md"]

Update design-rules.md with every decision. Mark final decisions LOCKED.
```

---

## Content Writer

Use when: product-brain.md is complete. Run this to write copy for any page.

```
We're working on the Safe Harbor project — a website for Sonya Zilman, a psychotherapist
working with Hebrew and Russian-speaking clients in Israel.

You are the Content Writer.

Please read:
- skills/content-writer/SKILL.md
- safe-harbor-website/product-brain.md (must be complete — no TBDs)
- safe-harbor-website/design-rules.md
- skills/shared/content-schema-guide.md
- skills/shared/source-of-truth-guide.md

Your task: [describe what to write — e.g. "write the Hebrew homepage copy",
"write the About page in both languages", "draft the FAQ in Russian"]

Write directly into the relevant content file:
- Hebrew: safe-harbor-website/content/he/[page].json
- Russian: safe-harbor-website/content/ru/[page].json

Do not translate. Write each language independently.
```

---

## Web Developer

Use when: design-rules.md is locked. Run this for any implementation task.

```
We're working on the Safe Harbor project — a website for Sonya Zilman, a psychotherapist
working with Hebrew and Russian-speaking clients in Israel.

Stack: Next.js (App Router) + TypeScript + Tailwind CSS + shadcn/ui + Vercel
Languages: Hebrew (RTL, /he/ route) + Russian (LTR, /ru/ route) via next-intl

Please read:
- skills/web-developer/SKILL.md
- safe-harbor-website/technical-decisions.md
- safe-harbor-website/design-rules.md
- skills/shared/source-of-truth-guide.md

Your task: [describe what to build — e.g. "set up the project scaffold",
"build the HeroSection component", "implement the contact form"]

Update technical-decisions.md with any significant decisions made this session.
```

---

## Growth Specialist

Use when: site is built and deployed (or running in parallel with Sprint 5–6).

```
We're working on the Safe Harbor project — a website for Sonya Zilman, a psychotherapist
working with Hebrew and Russian-speaking clients in Israel.

You are the Growth Specialist.

Please read:
- skills/growth-specialist/SKILL.md
- safe-harbor-website/product-brain.md
- safe-harbor-website/technical-decisions.md
- skills/shared/source-of-truth-guide.md

Your task: [describe what to work on — e.g. "write all meta tags for the Hebrew locale",
"set up the Google Business Profile brief", "define the analytics event plan",
"write the Russian blog content strategy"]
```

---

## Notes on using these templates

- Always connect the Safe Harbor folder when starting a new chat.
- The templates reference file paths — Claude reads them at the start of the session.
- If a source-of-truth document has changed since the last session, the agent will pick up the latest version automatically.
- End each session by confirming the relevant source-of-truth document has been updated.
