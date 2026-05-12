# BMAD Phase Guides — Detailed Reference

## Phase 1: Business — Step by Step

### Step 1: Run the Client Intake
Before anything else, generate and send the Client Intake Questionnaire (see questionnaire-template.md).

The questionnaire covers 8 areas:
1. Who the professional is (credentials, background, approach, character)
2. What they do (specialties, client types, methods, what makes them different)
3. Who their clients are (ideal client, pain points, desired transformation)
4. Practice logistics (location, format, languages, fees)
5. Website goals (primary goal, desired visitor emotion, main CTA)
6. Tone and look (aesthetic direction, color preferences, references)
7. Existing assets (bio, photos, written content)
8. Timeline and concerns

### Step 2: Produce the Brand Strategy Document

**Positioning Statement**
Format: "For [audience] who [situation or need], [professional's name] provides [approach] that delivers [outcome]. Unlike [alternative], [differentiator]."

**Tone of Voice**
3-5 adjectives describing how the site should feel to read.
Examples by profession:
- Therapist: warm, grounded, calm, direct, non-clinical
- Lawyer: clear, confident, approachable, no-nonsense
- Coach: energetic, practical, honest, no-fluff
- Consultant: sharp, credible, specific, peer-level

**Core Messaging Pillars**
3-4 themes the site consistently communicates.
Generic structure: Credibility > Relevance > Connection > Clear next step

**Emotional Journey Map**
Define the desired emotional state at each stage:
- Landing on the page
- Reading the bio
- Reviewing services
- Reaching the contact form

**Trust Mechanisms**
Specific elements that will build credibility: credential format, photo style, social proof, FAQ topics, booking flow.

### Step 3: Produce the UX Goals Document
- Primary CTA (the one action the site is optimized for)
- Secondary actions
- Required pages and their priority
- Content that must appear above the fold on mobile

---

## Phase 2: Model — Step by Step

### Standard Site Map
Adapt based on the professional's situation:
- Home
- About / Bio
- Services / Specialties
- FAQ
- Contact / Book a Session
- Blog (optional, strong for SEO)
- Online / Remote Services (if applicable)

### User Journey Definition
Map the 2-3 most common paths a visitor takes:
1. Direct referral: Home > Bio > Services > Contact
2. Search discovery: Blog article > CTA > About > Contact
3. Skeptical browser: Home > FAQ > Services > About > Contact

Each journey tells you what content each page must carry and what CTA it needs.

### Design System Spec

**Typography:** 1-2 fonts (heading + body). Readability over personality.

**Color palette principles by profession:**
- Healthcare / wellness: warm neutrals, soft greens or blues, avoid clinical white
- Legal / financial: navy, charcoal, warm white — serious but not cold
- Coaching / consulting: more contrast and stronger accent colors acceptable
- Creative: more latitude for personality

**Standard palette:** 1 primary, 1 accent, 2 neutrals, 1 background

**Spacing scale:** base 8px, scale: 8, 16, 24, 32, 48, 64, 96

---

## Phase 3: Architecture — Step by Step

### Project Initialization
```bash
npx create-next-app@latest [project-name] --typescript --tailwind --eslint --app
cd [project-name]
npx shadcn-ui@latest init
```

### Folder Structure
```
/app
  layout.tsx
  page.tsx
  /about/page.tsx
  /services/page.tsx
  /faq/page.tsx
  /contact/page.tsx
  /blog/[slug]/page.tsx

/components
  /sections     -> HeroSection, BioSection, ServiceCards, etc.
  /ui           -> primitive UI components
  /layout       -> Header, Footer, Nav

/content        -> MDX or JSON data files
/public
  /images
  /fonts
```

### Standard Section Components
- HeroSection — headline, subheadline, CTA
- BioSection — professional's story and credentials
- ServiceCards — what they offer
- TrustBar — credentials, years of experience, associations
- FAQAccordion — common questions and hesitations
- TestimonialsSection — social proof (if available)
- ContactCTA — final conversion block

---

## Phase 4: Delivery — Sprint Details

### Sprint 1: Strategy and Content Architecture
- Finalize Brand Strategy doc
- Write copy for all pages
- Lock Design Rules doc
- Initialize Technical Decisions doc

### Sprint 2: Design System
- Configure Tailwind (colors, fonts, spacing)
- Build base UI components
- Build Header and Footer
- Establish responsive grid

### Sprint 3: Homepage
Build in order: HeroSection > IntroSection > ServicesPreview > TrustBar > Testimonials > ContactCTA

### Sprint 4: Secondary Pages
- About / Bio — invest in the copy, this is often the most visited page
- Services — one section per service, not a bulleted list
- FAQ — focus on hesitations a new client would actually have
- Contact — minimal friction, one clear form, response time expectation

### Sprint 5: SEO, Accessibility, Performance
- Metadata on every page (title, description, og:image)
- Structured data (LocalBusiness and/or Person schema)
- Alt text on all images
- Keyboard navigation and focus states
- Lighthouse targets: Performance >90, Accessibility >95
- sitemap.xml and robots.txt

### Sprint 6: Deployment and Polish
- Deploy to Vercel (connect GitHub repo)
- Configure custom domain
- Set up analytics
- Test contact form end-to-end
- Test on a real mobile device
- Final copy review

---

## Common Mistakes to Avoid

- Skipping the intake questionnaire and guessing at positioning
- Generic headlines like "Welcome" or "Here to help you"
- Writing for the professional's ego rather than the visitor's anxiety
- Too many fonts or colors
- Generating the entire site in one prompt — always work section by section
- Forgetting mobile-first layout
