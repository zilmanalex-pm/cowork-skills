# Handoff Protocol

This document defines what each specialist produces and passes to the next. Following this protocol keeps the project moving without gaps or repeated work.

---

## The Chain

```
Brand Strategist
      ↓
  produces: product-brain.md (complete)
      ↓
Web Designer
      ↓
  produces: design-rules.md (complete and LOCKED)
      ↓
Content Writer
      ↓
  produces: copy for all pages (approved)
      ↓
Web Developer
      ↓
  produces: working site (all pages implemented)
      ↓
Growth Specialist
      ↓
  produces: SEO, analytics, deployment
```

---

## Handoff Definitions

### Brand Strategist → Web Designer

**What must be complete before the designer starts:**
- Positioning statement written
- Target audience defined
- Emotional strategy defined (what visitors should feel per page)
- Tone of voice adjectives agreed
- Core messaging pillars written
- Primary CTA confirmed

**Format:** product-brain.md with all sections marked LOCKED or DRAFT (no TBDs remaining)

---

### Web Designer → Content Writer + Web Developer

**What must be complete before either starts:**
- Typography selected (fonts, scale, weights)
- Color palette defined (all 5 colors with hex codes)
- Spacing scale defined
- Button styles defined
- Key component patterns sketched or described
- Responsive breakpoints defined
- Imagery direction described

**Format:** design-rules.md with all sections marked LOCKED

---

### Content Writer → Web Developer

**What must be complete before the developer starts:**
- Headline and subheadline for every page
- Body copy for all sections
- All CTA button labels
- FAQ questions and answers
- About/Bio copy approved by the professional

**Format:** A content document or folder with one file per page, clearly labelled

---

### Web Developer → Growth Specialist

**What must be complete before SEO/marketing work starts:**
- All pages implemented and rendering correctly
- Contact form working end-to-end
- Site deployed to Vercel with custom domain
- technical-decisions.md updated and complete

**Format:** Live staging URL + technical-decisions.md

---

## Mid-Sprint Handoffs

Not every task is a full phase handoff. For smaller tasks within a sprint:

1. The specialist completes the task
2. Updates the relevant source-of-truth document
3. Notes what was done and what is next in the document's decisions log
4. The next session picks up from the decisions log

---

## What Never Gets Handed Off

- Context from conversation history — always write decisions into the source-of-truth docs
- Assumptions — if it's not written down, it hasn't been decided
- Unresolved questions — flag them explicitly with `TBD` and a note
