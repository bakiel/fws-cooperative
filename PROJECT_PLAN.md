# Family World School Cooperative — Project Plan
*Managed by Aleph Creative-Hub | April 2026*

---

## PROJECT OVERVIEW

**Client:** Family World School (FWS) Cooperative
**Stakeholder:** Daisy Ross
**Brief Received:** 2026-01-26 (full scope clarified through 2026-03-30)
**Logo:** Crimson red (#c72028) — school building + world/globe motif — SVG V2 Option 2

**What FWS Is:**
A learning support cooperative for independent education programs (home schools, private non-govt schools, cooperative groups). Part of the It's My Miracle nonprofit + Miraculous Transitions + DCA Network.

**What FWS Offers:**
1. **ESI (Educator Support Initiative)** — substitute + regular educators via calendar + contracts
2. **FWS Courses** — educator-produced 10-video course libraries
3. **Tutoring Subscriptions** — monthly plan, book sessions via availability calendar
4. **Virtual Classroom Access** — Zoom, VEDAMO, BigBlue Button links
5. **Booking** — Square Appointments (already available, embed ready)

---

## DESIGN SYSTEM

### The Sovereign (Theme)
> "A warm, scholarly cooperative that brings the world's best educators into every home and learning community."

### Royal Family Decisions
- **KING (Layout):** Multi-portal architecture — 3 pathways (Educators / Institutions / Individuals). Clean zones, zero dead space, full-utilization sections.
- **QUEEN (Typography):** Cormorant Garamond (display/headers) + DM Sans (body/UI). Scholarly warmth meets digital clarity. NO Inter, Roboto, Arial.
- **PRINCE (Contrast):** Crimson on deep navy. Cream text on charcoal. Gold on dark. All 4.5:1+ minimum.
- **PRINCESS (Texture):** Linen/paper texture at 10-15% — educational, warm, physical. WebP quality 55.

### Brand Palette
```
Primary:   #c72028  Crimson Red (logo color — primary action, CTA, brand marks)
Dark:      #0f1a2e  Deep Navy (backgrounds, headers)
Surface:   #1a2a3a  Navy Surface (cards, panels)
Accent:    #c9a84c  Heritage Gold (highlights, premium elements)
Cream:     #f5f0e8  Warm Cream (body text on dark)
Light:     #f8f5f0  Off-White (light sections)
Dark text: #1a1a1a  Near Black (text on light)
Muted:     #6b7a8d  Cool Grey (labels, secondary)
```

### Typography Scale
```
Display (hero):    Cormorant Garamond, 700, 72-96px, tight tracking
Heading H1:       Cormorant Garamond, 600, 48-64px
Heading H2:       Cormorant Garamond, 600, 36-48px
Heading H3:       DM Sans, 700, 24-30px
Body:             DM Sans, 400, 16-18px, 1.7 line-height
Label/UI:         DM Sans, 600, 12-14px, uppercase, 2px tracking
Button:           DM Sans, 700, 14-16px
```

### Image Plan (NB2 Engine)
Generate via: `python3 /Users/mac/Downloads/design-system/scripts/gen_image.py "prompt" output.jpg 16:9 nb2`
API Key: `doppler secrets get GEMINI_API_KEY --plain -p jasper-crm -c dev`

| # | Asset | Prompt | Format | Use |
|---|-------|--------|--------|-----|
| 01 | hero-home | "multi-generational diverse family learning together at home, warm afternoon light, books and laptop, joyful, community, editorial photography, cinematic" | 16:9 | Home hero |
| 02 | hero-educators | "confident professional Black female educator teaching via video call, modern home office, bright, warm tones, laptop screen glowing, editorial photography" | 16:9 | Educators page hero |
| 03 | hero-institutions | "independent school building exterior, warm afternoon light, diverse children, welcoming, academic, architectural photography" | 16:9 | Institutions hero |
| 04 | hero-courses | "person learning online from laptop, cozy home environment, books nearby, warm golden light, focused, editorial lifestyle" | 16:9 | Courses page hero |
| 05 | hero-about | "diverse cooperative group of educators meeting, collaborative, warm discussion, community, documentary photography" | 16:9 | About hero |
| 06 | card-substitute | "substitute teacher entering classroom confidently, diverse school setting, warm lighting" | 4:3 | ESI card |
| 07 | card-tutor | "one-on-one tutoring session via video call, student and tutor smiling, screen glow" | 4:3 | Tutoring card |
| 08 | card-courses | "stack of educational videos on screen, modern clean interface, learning progress" | 4:3 | Courses card |
| 09 | card-contracts | "professional signing a digital contract on tablet, clean office, warm tones" | 4:3 | Contracts card |
| 10 | texture-linen | "seamless linen fabric texture, warm cream, educational paper feel, subtle weave" | 1:1 | Background texture |
| 11 | brand-dark-bg | "deep navy academic library background, books, warm lights, atmospheric depth" | 16:9 | Brand presentation bg |
| 12 | brand-light-bg | "clean cream paper texture, subtle grain, warm minimal academic" | 1:1 | Brand presentation light |

---

## WEBSITE ARCHITECTURE

### Site Map
```
fws-cooperative/
├── index.html              [HOME] — Hero, Mission, 3 Portals, Testimonials, CTA
├── pages/
│   ├── about.html          [ABOUT] — Story, DCA Network, nonprofit, team
│   ├── educators.html      [FOR EDUCATORS] — ESI + FWS Courses signup
│   ├── institutions.html   [FOR INSTITUTIONS] — ESI + membership
│   ├── members.html        [FOR INDIVIDUALS] — Courses + Tutoring
│   ├── courses.html        [COURSE CATALOG] — Browse available courses
│   ├── booking.html        [BOOKING] — Square embed + info
│   ├── esi.html            [ESI DETAIL] — Substitute + Regular educator program
│   └── contact.html        [CONTACT] — Inquiry form + info
├── brand/
│   ├── brand-presentation.html    [BRAND DECK] — Rendered to PDF
│   └── style-guide.html           [LIVING STYLE GUIDE]
├── components/
│   ├── nav.html            Shared navigation component
│   └── footer.html         Shared footer component
└── assets/
    ├── icons/fws-logo.svg  Brand logo
    ├── images/             Generated NB2 images
    └── fonts/              Downloaded woff2 files
```

### Page Specifications

#### 1. HOME (index.html)
**Sections:**
- **Hero** — Full-screen with parallax background, FWS logo, headline "Learning. Together. Everywhere.", sub "A cooperative of world-class educators supporting homes and schools globally." + CTA "Explore FWS"
- **Mission Strip** — 3-column: "For Educators" / "For Institutions" / "For Families" with crimson icons + portal links
- **What is FWS?** — Textured dark section, brand story paragraph + 4 key stats
- **Three Pathways** — Bento-grid cards: ESI / Courses / Tutoring — each with imagery and CTA
- **How It Works** — Animated timeline steps: Sign Up → Contract → Teach/Learn → Grow
- **Testimonials** — Cream background, 3 quotes with educator/institution names
- **Brand Partners** — It's My Miracle + Miraculous Transitions + DCA Network logos
- **CTA Banner** — Crimson full-width: "Ready to Join FWS?" with dual buttons
- **Footer** — Deep navy, 4 columns: FWS Info / Quick Links / Contact / Social

#### 2. EDUCATORS (pages/educators.html)
**Two Tracks:**
- **Track A: ESI** — Substitute or Regular educator: calendar availability, per-hour rates, semester contracts
- **Track B: FWS Courses** — Create 1 course (10 videos), earn per purchase, offer tutoring, track sales
**Sections:** Hero, Track Comparison Cards, ESI Details, Course Creation Details, Earnings Calculator (static), Signup CTA

#### 3. INSTITUTIONS (pages/institutions.html)
**Sections:** Hero, What You Get (ESI access, substitute pool, contract management, Zoom integration), Membership Tiers, How to Join, Booking embed

#### 4. MEMBERS (pages/members.html)
**Sections:** Hero, Individual vs Family Plans, Course Library Preview (4 cards), Tutoring Process (book via subscription), Booking Calendar embed, FAQ

#### 5. COURSES (pages/courses.html)
**Sections:** Hero, Course Grid (6-8 example cards: subject, educator, video count, price), Subscription Plans, How to Book Tutoring, Educator Profiles teaser

#### 6. ESI DETAIL (pages/esi.html)
**Sections:** What is ESI, Substitute Educators (availability, rates: hourly ≤2hrs, daily after), Regular Educators (semester contract, same schedule weekly, absence penalty), How Contracts Work, Zoom/Google Meets integration, Apply CTA

#### 7. BOOKING (pages/booking.html)
**Sections:** Intro, Square Appointments embed (`<script src='https://square.site/appointments/buyer/widget/0l7acyau8d0ckn/LCDJYH06M93DM.js'></script>`), FAQ below

#### 8. ABOUT (pages/about.html)
**Sections:** Hero, Our Story, Part of the Network (It's My Miracle / Miraculous Transitions / DCA Network), Our Values, Advisory / Leadership, Contact

#### 9. CONTACT (pages/contact.html)
**Sections:** Header, Contact form (name, email, type: Educator/Institution/Individual, message), Contact info, Social links

---

## BRAND PRESENTATION (PDF)

**File:** `brand/brand-presentation.html` → rendered to `brand/fws-brand-presentation.pdf`

**Pages (A4):**
1. Cover — Logo centered on deep navy with gold accent
2. Brand Story — "What FWS Is" paragraph + mission statement
3. Logo System — Logo on dark/light/colored backgrounds, clear space, minimum size
4. Color Palette — Swatches with hex, RGB, CMYK, usage
5. Typography — Font specimens, hierarchy demo
6. Photography Style — 4 image examples with style notes
7. UI Components — Buttons, cards, form elements
8. Application Examples — Website screenshot mock, email header, document header

---

## VIRTUAL CLASSROOM INTEGRATION NOTES

For future portal development (post-MVP):
- **Square Appointments** — READY (embed code confirmed)
- **Zoom** — Educator posts meeting link; institution/member can join via portal link
- **VEDAMO** — Virtual classroom SaaS; evaluate for ESI regular educators
- **BigBlue Button** — Open-source option; self-hosted or Greenlight frontend
- **Recommendation for MVP** — Zoom links embedded per educator profile; VEDAMO evaluation in Month 2

---

## PORTAL ARCHITECTURE (Post-MVP Wireframes)

Three authenticated dashboards (Phase 2):

### Educator Dashboard
- Profile & bio editor
- Availability calendar (substitute slots)
- Contract history + active contracts
- Course management (upload videos, view purchases)
- Tutoring bookings (upcoming sessions)
- Earnings summary

### Institution Dashboard
- Request substitute educator (calendar + filter by subject)
- View/sign contracts
- Zoom/Google Meets link management
- Regular educator schedule view
- Billing summary

### Individual Member Dashboard
- Purchased courses (video progress)
- Subscription status
- Book tutoring session (educator calendar)
- Upcoming tutoring sessions
- Past sessions + notes

---

## BUILD SEQUENCE

### Phase 0 - Assets (2-3 hours) — COMPLETE 2026-04-01
- [x] Generate 9 images via NB2 engine (hero-home, hero-educators, hero-about, hero-institutions, hero-courses, card-tutor, card-substitute, card-contracts, brand-dark-bg)
- [x] Download font woff2 files (Cormorant Garamond 400/600/700, DM Sans 400/600/700)
- [x] Copy logo to assets/icons/fws-logo.svg
- [ ] Generate texture-linen.jpg (deferred - optional polish)

### Phase 1 - Brand Presentation — COMPLETE 2026-04-01
- [x] Build `brand/brand-presentation.html` (8 pages A4)
- [x] Rendered to `brand/fws-brand-presentation.pdf` (10.6MB, 8 pages)
- [x] Vision review - all 8 pages pass, clean layout, fonts correct

### Phase 2 - Shared Components — Embedded in pages (sufficient for Phase 1)
- [x] Nav component (crimson CTA, active states, backdrop blur)
- [x] Footer (full 4-col on home, minimal on inner pages)
- [x] CSS design tokens (custom properties in each page)

### Phase 3 - Home Page — COMPLETE 2026-04-01
- [x] index.html - all 9 sections built
- [x] Hero with parallax + entrance animations
- [x] Portal strip (3 pathways)
- [x] About strip (mission + stats grid)
- [x] Bento grid (3 programs)
- [x] How It Works (4 steps)
- [x] ESI Spotlight
- [x] Testimonials
- [x] Network logos
- [x] CTA banner
- [x] Full footer
- [x] Scroll reveal + IntersectionObserver JS
- [x] Mobile responsive

### Phase 4 - Core Pages — COMPLETE 2026-04-01
- [x] educators.html (hero, 2-track comparison, 5-step process, requirements, CTA)
- [x] institutions.html (hero, what-you-get, 4-step join process, CTA)
- [x] members.html (plans, tutoring flow, course preview, booking)
- [x] courses.html (hero, subject filter, 6-course grid, how it works)

### Phase 5 - Supporting Pages — COMPLETE 2026-04-01
- [x] esi.html (ESI deep-dive: sub/regular tracks, rate cards, virtual classroom, requirements)
- [x] booking.html (Square embed + FAQ + sidebar)
- [x] about.html (hero with image, mission quote, network, values, team)
- [x] contact.html (form + sidebar with quick links)

### Onboarding Forms — COMPLETE 2026-04-01
- [x] apply-educator.html (ESI track A/B, qualifications, subjects, availability, consent)
- [x] apply-institution.html (institution type, contact, ESI needs, subjects, consent)
- [x] apply-member.html (plan selector, learner profiles, interests, dynamic add learner)
- [x] All forms wired from educators/institutions/members CTA buttons

### Phase 6 - Style Guide
- [ ] `brand/style-guide.html` — Living component library (deferred, optional)

### Phase 7 - QA & Delivery
- [x] Visual review all pages via render engine
- [x] Brand PDF vision review - 8 pages pass
- [ ] Mobile responsive check (375px, 768px, 1024px, 1440px)
- [ ] Package for delivery / VPS deploy

---

## SKILLS LOCKED IN

These skills are always used for this project:

| Skill | File | When |
|-------|------|------|
| Aleph Design Agent | `~/.claude/skills/aleph-design-agent/SKILL.md` | Every design decision |
| Aleph Web Design Engine | `~/.claude/skills/aleph-web-design-engine/SKILL.md` | Every page build |
| Image Generation | `~/.claude/skills/image-gen/SKILL.md` | NB2 asset generation |
| Gemini Vision Review | `~/.claude/skills/gemini-vision-review/SKILL.md` | QA gate after every render |
| Web Visual Effects | `~/.claude/skills/web-visual-effects/SKILL.md` | Premium UI polish |
| Design Soul | `~/.claude/skills/design/SOUL-DESIGN.md` | Royal Family enforcement |

**Image engine:** NB2 (`nb2` flag in gen_image.py) for all hero images
**Render engine:** Aleph PDF engine for all PDFs
**QA gate:** Gemini Vision Review — min 9/10, all `needs_fix: false`

---

## TECHNICAL STACK

**Website:** Pure HTML/CSS/JS (no framework for Phase 1)
- GSAP for scroll animations
- CSS custom properties for design tokens
- Intersection Observer for reveals
- Vanilla JS for interactions

**Future Portal (Phase 2):** Next.js + Tailwind + Framer Motion
**Backend (Phase 3):** FastAPI + PostgreSQL (Pure Python, no n8n)
**Deployment:** Hostinger VPS or Netlify static for Phase 1

---

## CONTEXT FILES

- Logo: `/Users/mac/Downloads/fws-cooperative/assets/icons/fws-logo.svg`
- Booking embed: `<script src='https://square.site/appointments/buyer/widget/0l7acyau8d0ckn/LCDJYH06M93DM.js'></script>`
- Contact email: luciusmel@gmail.com (from Gahn Eden records — verify with Daisy)
- Zoom link (from convo): `https://us06web.zoom.us/j/87006182517?pwd=OjisM1FnEl9U5aD0kJmtOuGoK1AmIx.1`

---

## NOTES & DECISIONS LOG

| Date | Decision | Reason |
|------|----------|--------|
| 2026-04-01 | NB2 for all hero images | Premium quality, client-facing |
| 2026-04-01 | Cormorant Garamond + DM Sans | Scholarly warmth, academic tone |
| 2026-04-01 | Deep navy primary bg, not black | Warmer, academic, less harsh |
| 2026-04-01 | Square Appointments for MVP booking | Already confirmed and coded by Daisy |
| 2026-04-01 | VEDAMO/BBB evaluation deferred | Phase 2 — need Daisy input on budget |
| 2026-04-01 | Pure HTML Phase 1, Next.js Phase 2 | Faster delivery, no framework overhead |
| 2026-04-01 | Font woff2 local (no Google Fonts CDN) | Headless render compatibility |

---

*Next action: Phase 0 - Generate assets. Run `gen_image.py` for all 12 images.*
*Confirm with Daisy: contact email, Zoom link usage rights, network logos for Partners section.*
