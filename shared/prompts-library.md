# Prompts Micro-Library

Pre-written prompts for the harder sub-tasks within each agent role.
Unlike session starters (which open a full session), these are for specific moments
where the task is well-defined and getting the prompt right matters.

Copy the relevant block, paste into the active session, fill in anything in [brackets].

---

## Brand Strategist

### Extract the real differentiator

Use after reading the questionnaire when the differentiator isn't immediately obvious.

```
Read Section 2 (What You Do) and Section 3 (Your Clients) of the questionnaire again.

I am looking for the real differentiator — not the credential, not the modality,
not the technique. The human thing. The way she describes a first session. The thing
clients say that she hears over and over.

It is often buried in:
- A parenthetical ("but I should also mention...")
- An answer to a different question than the one being asked
- The most specific thing she said about how she actually works

Identify the 2–3 most specific, concrete things she said about herself or her work.
For each one, tell me: is this something another therapist in Tel Aviv could say? If yes,
it is not the differentiator. If no, it might be.

Then write one sentence — her differentiator — that could not appear on anyone else's site.
```

---

### Write the positioning statement

Use once the differentiator and audience are clear.

```
Using the information in product-brain.md, write the positioning statement.

Format: "For [specific audience] who [specific situation], [name] provides
[specific approach] that [specific outcome]. Unlike [alternative], [specific differentiator]."

Every word in brackets must be replaced with something specific.
Test each element: could it describe any therapist? If yes, make it more specific.

Write 3 versions, each emphasizing a slightly different angle. Then tell me which one
you think is strongest and why.
```

---

### Define the Russian audience separately

Use when the Hebrew positioning is done but the Russian version needs its own framing.

```
The Hebrew positioning statement is now written. The Russian-speaking audience
is a distinct community with different cultural context around therapy.

Read the bilingual notes in product-brain.md.

Consider:
- The Russian-speaking community in Israel may carry specific associations with
  mental health that the Hebrew audience does not
- "Being understood" and "being spoken to in your language" carry extra weight here
- The mere fact of a Russian-language site is itself a signal — it says "I see you"

Write a version of the positioning statement calibrated for the Russian-speaking audience.
Note where it differs from the Hebrew version and why.
```

---

## Web Designer

### Extract a color palette from a photo

Use when working from Sonya's professional photo.

```
I am looking at [describe the photo: e.g. "a woman in a cream blazer, sitting in a
warm-lit room with wooden furniture and book spines in the background"].

Extract a 5-color palette from this photo suitable for a therapy website.
The palette must feel like an extension of the room she is sitting in —
not a mood board, not a brand exercise. The actual colors from the photo.

For each color:
- Name it semantically (background, text, primary, neutral, surface)
- Give the hex code
- Describe exactly where in the photo it comes from
- Describe its use on the site

Then check: do any two colors fail WCAG AA contrast (4.5:1) when used as
text on background? If yes, adjust and note the adjustment.
```

---

### Define a typography pairing

Use when typography is TBD and tone adjectives are set.

```
The tone of voice adjectives for this site are: [list from product-brain.md]
The audience is: [description from product-brain.md]
The languages are Hebrew and Russian.

Hebrew font must: support Hebrew script fully, feel warm and readable, not clinical.
Russian font must: support Cyrillic fully, pair visually with the Hebrew font.

Suggest a Hebrew + Russian font pairing. For each:
- Name the font
- Why it fits the tone
- What it must not feel like (the anti-tone)
- Confirm it is available via Google Fonts (for next/font loading)

Then define the full type scale:
H1, H2, H3, body, small — with size (px), weight, and line height for each.
```

---

## Content Writer

### Write the Hebrew About page

Use once product-brain.md is complete and Sonya's questionnaire answers are available.

```
Write the About page in Hebrew.

Read product-brain.md completely before writing a single word.
The emotional goal of this page is: the visitor leaves feeling they can trust this person.

Structure:
1. Opening paragraph — first person, person before credentials.
   Do not start with "I am a psychotherapist." Start with something true about
   how she shows up in the room.
2. Approach paragraph — how she actually works, in plain language.
   Not: "I use CBT and somatic approaches." Instead: what the experience of
   working with her feels like.
3. Background paragraph — credentials and training woven in as narrative, not listed.
4. Closing line — something personal and direct. What she wants for the people
   she works with.

Length: 300–500 words total.

Use the client's actual words from Section 3 of the questionnaire where they fit.
Avoid every cliché on the list in content-writer/SKILL.md.

Write the full Hebrew text, then flag any sentence you are uncertain about
and explain why.
```

---

### Write the Russian About page independently

Use after the Hebrew About page is approved.

```
The Hebrew About page is written and approved. Now write the Russian version.

Do not translate. Read the Russian audience notes in product-brain.md.

The Russian-speaking community may bring specific cultural associations with
therapy — normalization and warmth matter more here than credentials.
The tone can be slightly softer, slightly more personal.

Write the full Russian text as if you were writing it fresh for this audience,
with the Hebrew version only as a reference for the facts (credentials, years,
approach). The voice, emphasis, and framing may differ where it serves the reader.

After writing, note every meaningful difference between the Hebrew and Russian
versions and explain the reasoning. Sonya will review these differences specifically.
```

---

### Write FAQ answers that don't sound like FAQ answers

Use when drafting the FAQ page.

```
The FAQ page answers the question: is it safe to reach out?

The questions are:
[paste questions from content/he/faq.json or content/ru/faq.json]

Write each answer as if Sonya is speaking directly to one person — the specific
person who almost didn't write in.

Rules:
- 3–6 sentences per answer
- No jargon, no clinical language
- No bullet points inside answers
- If the honest answer is "it depends" — say that, then explain what it depends on
- If the answer involves uncertainty (like how long therapy takes) — acknowledge
  the uncertainty honestly rather than hedging with vague language

Write in [Hebrew / Russian]. Then flag any answer where the tone felt off
or the content is something Sonya should confirm.
```

---

## Web Developer

### Translate design-rules.md into Tailwind config

Use at the start of Sprint 2 to configure the design system in code.

```
Read design-rules.md completely.

Translate every LOCKED design decision into tailwind.config.ts.
Use the template at templates/tailwind.config.template.ts as your base.

For each value you add:
- Use semantic names (primary, not teal; surface, not white)
- Add a comment referencing the design-rules.md section it came from

After writing the config, list any design-rules.md values that are still DRAFT
or TBD — these need to be resolved before Sprint 3 begins.

Do not make any design decisions yourself. If a value is missing from design-rules.md,
flag it rather than inventing it.
```

---

### Implement RTL/LTR layout switching

Use when building any component that behaves differently between Hebrew and Russian.

```
I am building [component name]. It needs to work correctly in both:
- Hebrew (RTL, dir="rtl" on <html>)
- Russian (LTR, dir="ltr" on <html>)

Read templates/lib/rtl.template.ts for the available RTL utilities.

Rules:
- Never use text-left or text-right — use text-start and text-end
- Never use ml-* or mr-* for layout spacing — use ms-* and me-*
- Use the rtl: prefix for anything that needs to physically flip
- Test mentally: if I switch dir="rtl" to dir="ltr", does this component
  still make sense?

Build the component. Then describe exactly which classes handle the RTL/LTR
difference and why each one is necessary.
```

---

### Set up next-intl locale routing

Use during Sprint 1 when configuring the i18n system.

```
Set up next-intl locale routing for Safe Harbor.

Languages: Hebrew (he, RTL, default) and Russian (ru, LTR).
Routes: /he/* and /ru/* — always show locale prefix.

Use these templates as your starting point:
- templates/middleware.template.ts
- templates/i18n.template.ts
- templates/app/layout.template.tsx

Steps:
1. Install next-intl
2. Drop middleware.ts into project root
3. Drop i18n.ts into project root
4. Create /app/[locale]/layout.tsx from the layout template
5. Move /app/page.tsx to /app/[locale]/page.tsx
6. Verify: visiting / redirects to /he/, visiting /ru/ loads correctly

After completing each step, confirm it is working before moving to the next.
Update technical-decisions.md with the next-intl version installed.
```

---

## Growth Specialist

### Keyword research for the Russian-speaking audience in Israel

Use at the start of the growth phase, before writing any meta copy.

```
The target audience is Russian-speaking adults living in Israel who are considering
therapy. Many have never been to therapy before. Mental health stigma is a real
consideration in this community.

Generate two lists of search phrases — the kind a person would actually type,
not keyword-tool output:

List 1 — Problem-first searches (what they're feeling)
List 2 — Practical searches (what they're looking for)

For each phrase:
- Write it in Russian (as they would actually search)
- Note the likely intent behind it
- Note whether it signals someone early in consideration or ready to contact

Then identify the 3 highest-opportunity phrases — high intent, low competition
(because very little Russian-language therapy content exists for Israeli audiences).
These become the primary keywords for the Russian locale meta copy.
```

---

### Write meta copy for both locales

Use after all page copy is written and approved.

```
Write title tags and meta descriptions for all pages in both languages.

Read content-schema-guide.md for the format requirements:
- Title tags: 50–60 characters, includes therapist name + primary keyword
- Meta descriptions: 140–160 characters, what the page is about + implicit invitation

Pages: home, about, services, faq, contact.

For each page:
1. Write the Hebrew version
2. Write the Russian version independently (not a translation)
3. Count the characters and confirm both are within range

Write meta copy for Hebrew, then Russian — in that order.
The meta copy must match the tone of the page copy and feel consistent with the
overall site voice.

After writing, note any page where the meta copy was harder to write and why —
this often signals the page copy itself needs tightening.
```
