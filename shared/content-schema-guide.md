# Content Schema Guide

This document explains the content structure for every page of the Safe Harbor site. Use it when filling in the JSON content files under `/content/he/` and `/content/ru/`.

Each JSON file is a page. Each field is a content slot. The Content Writer fills in the values. The Developer reads the files to populate components. Neither touches the other's work.

---

## Rules for filling in content

- **Empty string `""`** = not yet written. Never delete a key.
- **Arrays** = keep the structure, fill in each item.
- **`meta.title`** = 50–60 characters. Therapist name + primary keyword.
- **`meta.description`** = 140–160 characters. What the page is about + implicit invitation.
- All values in the file must be in the language of the locale (`/he/` = Hebrew, `/ru/` = Russian).
- Do not translate. Write each locale independently.

---

## shared.json — appears on every page

```
nav.home          → Navigation label for the homepage
nav.about         → Navigation label for the About page
nav.services      → Navigation label for the Services page
nav.faq           → Navigation label for the FAQ page
nav.contact       → Navigation label for the Contact page
nav.cta           → The button in the nav (e.g. "Let's talk")

footer.tagline    → One short line under the name in the footer
footer.copyright  → Copyright line (e.g. "© 2025 Sonya Zilman")
```

---

## home.json

```
meta.title        → Page title tag (50–60 chars)
meta.description  → Meta description (140–160 chars)

hero.headline     → 5–9 words. Direct. Specific. Not a tagline.
hero.subheadline  → 1–2 sentences. Who she works with and what happens here.
hero.ctaLabel     → Button text. Low pressure. (e.g. "Let's talk")

intro.body        → 2–3 sentences. Therapist speaking directly to visitor.
                    Not a bio. An acknowledgment of what the visitor is carrying.

services[].name         → Short plain-language name (e.g. "Anxiety and worry")
services[].description  → 1 sentence. Name the situation, not the modality.
                          3–4 items total.

cta.body          → 1 sentence invitation. Direct, warm, no urgency.
cta.buttonLabel   → Button text (can match hero CTA or differ slightly)
```

---

## about.json

```
meta.title        → Page title tag
meta.description  → Meta description

opening.body      → First paragraph. First person. Person before credentials.
                    What brought her to this work, or how she sees her role.

approach.body     → Second paragraph. How she actually works, in plain language.
                    Not modality names — describe the experience of working with her.

background.body   → Third paragraph. Credentials and training woven into narrative.
                    Not a CV list. A story.

closing.body      → Final line or short paragraph. Personal and direct.
                    What she wants for the people she works with.
```

---

## services.json

```
meta.title        → Page title tag
meta.description  → Meta description

headline          → Page heading (e.g. "What I work with")
subheadline       → 1 sentence framing the page (optional)

services[].name         → Plain language name (not clinical)
services[].description  → 2–4 sentences. Who this is for, what it feels like,
                          what happens in the work. No symptom lists.
services[].slug         → URL-safe identifier (e.g. "anxiety", "relationships")
                          Used for linking. Do not change after set.
```

---

## faq.json

```
meta.title        → Page title tag
meta.description  → Meta description

headline          → Page heading (e.g. "Questions people ask before reaching out")

questions[].question  → Written from visitor's perspective.
                        The hesitation they actually have, not a therapist's framing.
questions[].answer    → Direct, warm, 3–6 sentences. No jargon.
```

---

## contact.json

```
meta.title        → Page title tag
meta.description  → Meta description

intro.body        → 2–3 sentences. Normalizes the act of reaching out.
                    Should feel like the therapist is saying: it's okay to write.

responseTime      → Specific expectation (e.g. "I usually respond within one business day")

form.nameLabel        → Label for name field
form.emailLabel       → Label for email field
form.phoneLabel       → Label for phone field (if included)
form.messageLabel     → Label for message field
form.submitLabel      → Submit button text

alternativeContact    → Optional. Direct phone or WhatsApp number with context.
                        (e.g. "Prefer to call? +972 50 000 0000")
```

---

## How the Content Writer and Developer interact

The Content Writer fills in values. The Developer reads values. Neither edits the other's file.

If a field is genuinely not needed for this site (e.g. no phone number), set it to `null` — don't delete the key. This keeps the schema consistent and prevents the Developer from having to handle missing keys.

If new fields are needed that aren't in the schema, add them to this guide first, then to the JSON files. Both roles must agree on new fields before they're used.
