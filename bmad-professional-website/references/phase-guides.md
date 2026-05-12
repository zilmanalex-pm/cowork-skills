# BMAD Phase Guides — Detailed Reference

## Phase 1: Business — Step by Step

### Step 1: Collect the Brief
Before anything else, generate and send the Business Phase Questionnaire to the client. See `questionnaire-template.md`.

The questionnaire covers 8 areas:
1. Who the practitioner is (credentials, approach, character)
2. What they do (specialties, client types, methods)
3. Who their clients are (ideal client, pain points, transformation)
4. Practice logistics (location, format, languages, fees)
5. Website goals (primary goal, desired visitor emotion, CTA)
6. Tone and look (aesthetic direction, color preferences)
7. Existing assets (bio, photos, written content)
8. Timeline and concerns

### Step 2: Produce the Brand Strategy Document
Once questionnaire answers are collected, produce a Brand Strategy document containing:

**Positioning Statement**
Who the practitioner serves, what they offer, and what makes them different.
Format: "For [audience] who [situation/need], [practitioner name] provides [approach] that [outcome]. Unlike [alternative], [differentiator]."

**Tone of Voice Guidelines**
3–5 adjectives that describe how the site should feel to read.
Examples: warm but grounded / direct and non-clinical / calm and unhurried

**Core Messaging Pillars**
3–4 thematic messages the site will consistently communicate.
Example: Safety first → Professional credibility → Personal connection → Clear path to booking

**Emotional Journey Map**
What should the visitor feel at each stage:
- Landing on the page → [feeling]
- Reading the bio → [feeling]
- Seeing services → [feeling]
- Reaching the contact form → [feeling]

**Trust Mechanisms**
Specific elements that will build trust: credentials format, photo style, FAQ topics, booking flow.

### Step 3: Produce the UX Goals Document
- Primary CTA (one action the site is optimized for)
- Secondary actions
- Pages needed and their priority
- Content that must be above the fold on mobile

---

## Phase 2: Model — Step by Step

### Site Map
Define every page. For a typical therapist site:
- Home
- About / Bio
- Services / Specialties
- FAQ
- Contact / Book a Session
- Blog (optional, but strong for SEO)
- Online Therapy (if applicable)

### User Journey Definition
Map the 2–3 most common paths a visitor will take:
1. **Direct referral:** lands on Home → reads Bio → checks Services → contacts
2. **Search discovery:** lands on Blog → reads article → sees CTA → About → contacts
3. **Skeptical browser:** Home → FAQ → Services → About → contacts

Each journey tells you what content each page must carry and what CTA each page needs.

### Design System Spec
Before any visual design:
- **Typography:** Choose 1–2 fonts (one for headings, one for body). Prioritize readability over personality.
- **Color palette:** 1 primary color, 1 accent, 2 neutral tones, 1 background. For therapy sites: avoid clinical white, harsh contrasts; prefer warm neutrals, soft greens/blues.
- **Spacing scale:** Define base unit (8px recommended) and scale (8, 16, 24, 32, 48, 64, 96)
- **Button styles:** Primary, secondary, ghost. Always include hover states.
- **Component patterns:** Card style, section layout, divider style

---

## Phase 3: Architecture — Step by Step

### Project Initialization
```bash
npx create-next-app@latest therapist-site --typescript --tailwind --eslint --app
cd therapist-site
npx shadcn-ui@latest init
```

### Folder Structure
```
/app
  layout.tsx         → global layout, fonts, metadata
  page.tsx           → homepage
  /about/page.tsx
  /services/page.tsx
  /faq/page.tsx
  /contact/page.tsx
  /blog/[slug]/page.tsx

/components
  /sections          → full-page sections (HeroSection, BioSection, etc.)
  /ui                → primitive UI (from shadcn or custom)
  /layout            → Header, Footer, Nav

/lib
  utils.ts           → shared utilities
  content.ts         → content helpers or CMS client

/content             → MDX files or JSON data
/public
  /images
  /fonts
```

### Component Naming Convention
- Section components: `[Name]Section.tsx` (e.g., `HeroSection.tsx`)
- Page-level wrappers: `[Page]Page.tsx`
- Reusable primitives: single word or short compound (e.g., `Card.tsx`, `CTAButton.tsx`)

---

## Phase 4: Delivery — Sprint Details

### Sprint 1: Strategy and Content Architecture
- Finalize Brand Strategy doc
- Write copy for all pages (or draft outlines)
- Define and lock Design Rules doc
- Set up Technical Decisions doc

### Sprint 2: Design System and Visual Direction
- Implement Tailwind config (colors, fonts, spacing)
- Build base UI components (Button, Card, Section wrapper)
- Build Header and Footer
- Establish responsive grid

### Sprint 3: Homepage
Build in this order:
1. HeroSection (headline, subheadline, CTA)
2. IntroSection (short bio teaser or core message)
3. ServicesPreview (cards linking to Services page)
4. TrustBar (credentials, years of experience, associations)
5. TestimonialSection (if client has them)
6. ContactCTA (final CTA block)

### Sprint 4: Secondary Pages
- About / Bio page — this is often the most important page; spend real time on copy
- Services / Specialties page — one section per specialty, not a bulleted list
- FAQ page — use accordion; focus on hesitations a new client would have
- Contact page — minimal friction; one form, clear instructions, response time expectation

### Sprint 5: SEO, Accessibility, Performance
- Add metadata to every page (title, description, og:image)
- Add structured data (LocalBusiness, Person schema)
- Ensure all images have alt text
- Keyboard navigation and focus states
- Lighthouse score targets: Performance >90, Accessibility >95
- Add sitemap.xml and robots.txt

### Sprint 6: Deployment and Polish
- Deploy to Vercel (connect GitHub repo)
- Configure custom domain
- Set up Google Analytics or Plausible
- Test contact form end-to-end
- Test on mobile (real device, not just DevTools)
- Final copy review

---

## Common Mistakes to Avoid

**Strategy phase:**
- Skipping the questionnaire and guessing at positioning
- Using clinical language when human language would work
- Generic headlines like "Welcome to my practice"

**Design phase:**
- Too many fonts
- Low contrast text (especially on soft background colors)
- Hiding the contact information

**Build phase:**
- Generating the full site in one prompt — always work section by section
- Forgetting mobile-first layout
- Skipping the loading/error states on the contact form
