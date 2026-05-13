# Phase Quality Checklists

Use these at the end of each agent session to confirm the work is truly done before handing off to the next role. "Done" means every item is checked — not mostly done, not almost done.

These are more granular than the handoff protocol. The handoff protocol defines *what the next agent needs*. These checklists define *how to know you've produced it properly*.

---

## Brand Strategist — done when:

**Positioning**
- [ ] Positioning statement written and specific — no generic phrases ("people who are struggling" is not an audience)
- [ ] The real differentiator identified — the human thing, not the credential or modality
- [ ] Ideal client described as a specific person in a specific situation

**Audience**
- [ ] What they come in saying — their actual words, preserved not paraphrased
- [ ] What they're afraid of before starting — specific fear, not abstract
- [ ] What transformation they're hoping for — concrete, not "feel better"

**Emotional strategy**
- [ ] Home page emotional goal defined — what "am I in the right place?" resolves to for this specific audience
- [ ] About page emotional goal defined
- [ ] Services page emotional goal defined
- [ ] Contact page emotional goal defined

**Tone**
- [ ] 3–5 tone adjectives chosen — each one earns its place (no "warm, caring, professional")
- [ ] Anti-tone defined — what the site must never sound like
- [ ] Tone is specific to this therapist, not generic therapy-site tone

**Messaging**
- [ ] 3–4 messaging pillars written — themes, not taglines
- [ ] Primary CTA confirmed — one action, not several

**Trust**
- [ ] Credentials: format and placement specified
- [ ] Photo: confirmed, style described
- [ ] Social proof: yes/no decision made
- [ ] FAQ: hesitations to address listed

**Bilingual**
- [ ] Hebrew audience considerations noted
- [ ] Russian audience differences noted explicitly
- [ ] Any messaging that needs two versions flagged

**Final**
- [ ] product-brain.md has zero TBDs
- [ ] All sections marked LOCKED or DRAFT
- [ ] Sonya has reviewed DRAFT items (or flagged for review)

---

## Web Designer — done when:

**Typography**
- [ ] Heading font selected with rationale tied to tone of voice
- [ ] Body font selected — readable at 16–18px confirmed
- [ ] Maximum 2 fonts — no exceptions
- [ ] Full type scale defined: H1, H2, H3, body, small — sizes, weights, line heights
- [ ] Hebrew font confirmed (Heebo or equivalent)
- [ ] Russian font confirmed (Inter or equivalent)

**Color**
- [ ] All 5 palette colors defined with hex codes: background, text, primary, neutral, surface
- [ ] Each color has a documented use case
- [ ] Primary on background contrast ratio checked — passes WCAG AA (4.5:1 minimum)
- [ ] Text on background contrast ratio checked — passes WCAG AAA (7:1 preferred)
- [ ] Colors avoided list confirmed

**Spacing and layout**
- [ ] Base unit confirmed (8px)
- [ ] Full spacing scale documented
- [ ] Max content width defined
- [ ] Column grid defined
- [ ] Section padding values defined for mobile and desktop

**Components**
- [ ] Primary button: background, text color, border radius, hover state
- [ ] Secondary button defined
- [ ] Card: background, border, shadow, padding
- [ ] Input field: height, border, focus state
- [ ] All component states defined (default, hover, active, disabled)

**Imagery**
- [ ] Photo style described
- [ ] Sonya's photo placement confirmed
- [ ] Stock photo guidance defined (or explicitly excluded)

**Final**
- [ ] design-rules.md has zero TBDs
- [ ] All sections marked LOCKED
- [ ] Developer could implement from this document without asking a single question

---

## Content Writer — done when:

**Homepage**
- [ ] Headline: 5–9 words, direct, audience-specific — not a tagline
- [ ] Subheadline: 1–2 sentences, expands on audience + what happens here
- [ ] Intro: 2–3 sentences, therapist speaking directly — acknowledgment not bio
- [ ] 3–4 service cards: plain-language names + 1 sentence each
- [ ] CTA: low-pressure, direct

**About page**
- [ ] Opening paragraph: first person, person before credentials
- [ ] Approach paragraph: plain language, not modality names
- [ ] Background paragraph: credentials woven in as narrative, not listed
- [ ] Closing: personal, direct, what she wants for clients
- [ ] Total length: 300–500 words

**Services page**
- [ ] Each service name: plain language, no clinical terms
- [ ] Each description: 2–4 sentences, describes the person's experience not the symptoms

**FAQ**
- [ ] All questions written from visitor's perspective
- [ ] All answers: direct, warm, 3–6 sentences, no jargon
- [ ] Covers the core hesitations: first session, pace, how long, languages, payment

**Contact page**
- [ ] Intro normalizes reaching out — no pressure, no urgency
- [ ] Response time is specific ("within one business day" not "soon")
- [ ] Form labels clear and minimal

**Writing quality**
- [ ] No therapy clichés present (safe space, healing journey, take the first step, etc.)
- [ ] Client's actual words used where possible — not paraphrased
- [ ] Short sentences used for landing moments, longer for building

**Bilingual**
- [ ] Hebrew version written first
- [ ] Russian version written as independent draft — not a translation
- [ ] Differences in meaning or emphasis between versions flagged for Sonya's review

**Meta copy**
- [ ] Title tag written for each page: 50–60 characters, includes name + keyword
- [ ] Meta description written for each page: 140–160 characters

**Final**
- [ ] All content JSON files populated (no empty strings remaining)
- [ ] Sonya has reviewed and approved all copy in both languages

---

## Web Developer — done when:

**Sprint 1 — Setup**
- [ ] Next.js initialized with TypeScript + Tailwind + ESLint + App Router
- [ ] shadcn/ui initialized
- [ ] Tailwind config matches design-rules.md exactly — no hardcoded colors
- [ ] Fonts loaded via next/font, CSS variables set
- [ ] Folder structure matches technical-decisions.md
- [ ] Header and Footer shells created
- [ ] technical-decisions.md updated

**Sprint 2 — Design system**
- [ ] All color tokens live in Tailwind config — no inline styles
- [ ] Typography scale implemented and tested at real sizes
- [ ] Spacing verified against design-rules.md
- [ ] Button components built — all states working
- [ ] Card component built
- [ ] Responsive grid verified at 375px, 768px, 1280px

**Sprint 3 — Homepage**
- [ ] All sections implemented: Hero, Intro, Services, TrustBar, CTA
- [ ] Mobile layout verified on real device or accurate emulator
- [ ] No hardcoded copy in components — all text from content JSON

**Sprint 4 — Secondary pages**
- [ ] About page implemented
- [ ] Services page implemented
- [ ] FAQ page with working accordion
- [ ] Contact page with working form
- [ ] All pages reachable from navigation
- [ ] Contact form tested end-to-end — submission confirmed received

**Sprint 5 — Polish**
- [ ] generateMetadata() on every page
- [ ] OG images created and referenced
- [ ] LocalBusiness schema on homepage and contact page
- [ ] Person schema on About page
- [ ] Schemas validated at schema.org/validator
- [ ] All images have descriptive alt text
- [ ] Keyboard navigation tested — all interactive elements reachable
- [ ] Lighthouse Performance > 90
- [ ] Lighthouse Accessibility > 95
- [ ] RTL layout verified in Hebrew — no broken alignments
- [ ] LTR layout verified in Russian

**Sprint 6 — Deployment**
- [ ] Vercel connected to GitHub repo
- [ ] Custom domain configured and resolving
- [ ] Environment variables set in Vercel (email, API keys)
- [ ] sitemap.xml generating and accessible
- [ ] robots.txt confirmed
- [ ] Analytics installed and events firing
- [ ] Contact form tested on production
- [ ] Tested on real iOS and Android device

---

## Growth Specialist — done when:

**SEO**
- [ ] Title tags: written for all pages in Hebrew and Russian (50–60 chars each)
- [ ] Meta descriptions: written for all pages in both languages (140–160 chars)
- [ ] H1 on every page: unique, matches intent of title tag
- [ ] Alt text on all images including Sonya's photo
- [ ] Internal links: contact page reachable from every page

**Structured data**
- [ ] LocalBusiness schema: all fields populated, validated
- [ ] Person schema: all fields populated, validated
- [ ] availableLanguage includes Hebrew and Russian

**Search Console**
- [ ] Google Search Console property created
- [ ] Domain verified
- [ ] Sitemap submitted
- [ ] No crawl errors reported

**Google Business Profile**
- [ ] Profile created or claimed
- [ ] Category: Psychotherapist
- [ ] Languages spoken: Hebrew, Russian listed explicitly
- [ ] Website link correct
- [ ] Same photo as site

**Analytics**
- [ ] Tool selected and installed (Plausible or GA4)
- [ ] Page views tracking
- [ ] Contact form submission event firing
- [ ] CTA click event firing
- [ ] Locale-level tracking confirmed (/he/ vs /ru/ visible in dashboard)

**Performance**
- [ ] Core Web Vitals green in PageSpeed Insights
- [ ] Sonya's photo optimized (WebP, correct dimensions)
- [ ] No render-blocking scripts

**Final**
- [ ] All launch checklist items from growth-specialist/SKILL.md checked
- [ ] Sonya briefed on Google Business Profile maintenance
- [ ] Analytics access shared with Sonya
