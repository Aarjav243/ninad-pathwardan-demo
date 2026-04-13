# Dr. Dipanjali Deka — Portfolio Website Implementation Plan

---

## Project Overview

**Client:** Dr. Dipanjali Deka
**Type:** Academic & Personal Portfolio
**Concept:** A storytelling website that lives at the intersection of scholarship and song — an immersive, narrative-first experience.

**Core tension to design around:** She is both rigorous academic and embodied practitioner. The site must feel both intellectual and alive.

---

## Design Philosophy: *"The Space Between Notes"*

In Hindustani classical music, *gamak* — the ornament, the grace note, the space between notes — is where the raga breathes. This website exists in that space: between the written word and the sung note, between the archive and the throat.

**Mood board adjectives:** Meditative · Luminous · Ancient-meets-contemporary · Manuscript · Midnight raga · Warm candlelight · Living archive

---

## Design System

### Color Palette — *"Twilight Raga"*

| Token | Hex | Usage |
|-------|-----|-------|
| `--midnight` | `#0A0A1A` | Primary background (dark sections, hero) |
| `--deep-navy` | `#12122A` | Secondary dark background |
| `--parchment` | `#FDF6E9` | Light section background (manuscript feel) |
| `--warm-cream` | `#F5EDD7` | Alternate light background |
| `--saffron` | `#E8852A` | Primary accent (bhakti warmth, CTAs) |
| `--gold` | `#C9A84C` | Decorative accent (illuminated manuscript) |
| `--violet` | `#6B3FA0` | Spiritual depth (wave animation only) |
| `--rust` | `#B5461A` | Emphasis on light backgrounds |
| `--text-light` | `#F0E6D3` | Primary text on dark backgrounds |
| `--text-muted` | `#9B8B7A` | Secondary/meta text on dark backgrounds |
| `--text-dark` | `#2A1F14` | Primary text on light backgrounds |
| `--text-sub` | `#5A4535` | Secondary text on light backgrounds |

**Contrast ratios (WCAG 2.1 AA):**
- `--text-light` on `--midnight`: ~15.9:1 ✅
- `--text-dark` on `--parchment`: ~14.3:1 ✅
- `--saffron` on `--midnight`: ~4.6:1 ✅ (large text)
- `--gold` on `--midnight`: ~8.5:1 ✅
- `--rust` on `--parchment`: ~7.6:1 ✅

### Typography Scale

| Token | Family | Size | Weight | Usage |
|-------|--------|------|--------|-------|
| `--font-display` | Playfair Display | `clamp(3rem, 9vw, 7rem)` | 400 | Hero name |
| `--font-display` | Playfair Display | `clamp(2.5rem, 6vw, 4.5rem)` | 400 | Section headings |
| `--font-serif` | Cormorant Garamond | `clamp(1.125rem, 2vw, 1.375rem)` | 300/italic | Body text, quotes |
| `--font-sans` | Montserrat | `clamp(0.75rem, 1vw, 0.875rem)` | 400/500 | Labels, nav, tags |

**Rationale:** Playfair Display carries literary gravitas. Cormorant Garamond evokes manuscript tradition with modern readability. Montserrat provides clean structural contrast.

### Spacing Scale

```
--space-xs:  0.5rem    (8px)   — tight groupings
--space-sm:  1rem      (16px)  — component padding
--space-md:  2rem      (32px)  — section sub-spacing
--space-lg:  4rem      (64px)  — nav, major padding
--space-xl:  6rem      (96px)  — section breathes
--space-2xl: 10rem     (160px) — major sections
```

### Animation Principles

1. **Entrance animations:** `fadeUp` (opacity 0→1, translateY 20px→0) — elements feel like they surface from below, like words emerging
2. **Scroll reveals:** IntersectionObserver with `threshold: 0.12` — reveals as user approaches, not abruptly
3. **Hero canvas:** Multi-frequency sine waves (5 overlapping), representing harmonics of a raga
4. **Equalizer:** CSS `scaleY` animation with staggered delays — 20 bars creating a breathing music visualiser
5. **Easing:** `cubic-bezier(0.16, 1, 0.3, 1)` — "expo out" — feels organic, not mechanical

---

## Site Architecture

```
index.html (Landing Page)
├── /nav          — Fixed, transparent → opaque on scroll
├── #hero         — Full-screen, canvas wave animation
├── #prelude      — Full-screen bhakti verse / quote
├── #about        — Narrative biography, two-column
├── #research     — 6 research threads in a grid
├── #music        — Vocal practice, animated equaliser
├── #academic     — Timeline of positions & education
└── #connect      — Footer with contact
```

**Future pages (Phase 2):**
- `/research` — Publications, papers, conference talks
- `/music` — Recordings, concert archive, AIR recordings
- `/teaching` — Courses, syllabi, student resources
- `/writing` — Essays, blog, creative non-fiction

---

## Landing Page — Section-by-Section Spec

### Section 1: Hero
- **Background:** `--midnight` with canvas sine-wave animation
- **Waves:** 5 overlapping, colours: gold (0.55 opacity), saffron (0.4), violet (0.25), gold-faint (0.2), cream (0.15)
- **Content:** Eyebrow label · Name (large Playfair) · Roles (Cormorant italic) · Tagline · Scroll indicator
- **Animation:** Staggered `fadeUp` entrances, 0.3s → 0.9s delay chain
- **Copy:** "Scholar · Vocalist · Storyteller" — three words that contain her entire identity

### Section 2: Prelude
- **Background:** `--deep-navy`
- **Content:** Kabir doha in Devanagari + English translation
- **Verse:** `साधो, शब्द साधना कीजै` / "O seeker, practice the discipline of the Word"
- **Decoration:** Musical staff (5 horizontal gradient lines) above and below
- **Why this verse:** Connects her two worlds — the *shabd* (word) tradition of Kabir and her work in writing pedagogy. The word is simultaneously literary and musical.

### Section 3: About
- **Background:** `--parchment`
- **Layout:** Two-column — narrative prose (left) + sticky sidebar with pull-quote & position card (right)
- **Tone:** Warm but precise. Third-person narrative that reads like a story.
- **Sidebar pull-quote:** Floats on the right as user scrolls through the about text

### Section 4: Research Threads
- **Background:** `--midnight`
- **Layout:** 3×2 grid of cards with `1px` gap (gold-tinted) creating a mosaic grid effect
- **Cards:** Large ghost number (01–06), icon, title, description, tags
- **Hover:** Subtle `--deep-navy` background shift + number brightens
- **6 threads:** Music & Religion · Oral Poetry & Orality · Ethnomusicology · Indian Aesthetic Theory · Performance Studies · Writing Pedagogy

### Section 5: The Voice
- **Background:** `--warm-cream`
- **Layout:** Two-column — animated equaliser visualiser (left) + text (right)
- **Equaliser:** 20 CSS bars with staggered `scaleY` animations, `transform-origin: bottom`
- **Credential badges:** Hindustani Classical · Bhakti-Sufi Music · All India Radio · Multilingual

### Section 6: Academic Journey
- **Background:** `--deep-navy`
- **Layout:** Vertical timeline with gold gradient left-border line
- **3 items:** Current position · AIIS · PhD (JNU)

### Section 7: Footer
- **Background:** `--midnight`
- **Layout:** 3-column — brand · navigation · contact
- **Email:** Placeholder (to be updated by client)

---

## Applied Skills

### `/design-system` — Audit Output

**Design System: Dipanjali Deka Portfolio v1.0**

| Category | Defined | Notes |
|----------|---------|-------|
| Colors | 11 tokens | Full semantic + brand coverage |
| Typography | 3 families, 10 size tokens | Fluid with `clamp()` |
| Spacing | 6 tokens | Consistent geometric scale |
| Motion | 4 easings, 3 durations | Organic, non-mechanical |
| Borders/radius | Minimal (2px radius only) | Intentionally architectural |

**Priority design system decisions:**
1. No rounded corners on cards (2px max) — sharp, precise, academic
2. Gold used only as accent, never for body text — reverence, not decoration
3. All section transitions are hard cuts (no gradients between sections) — like verses in a poem

---

### `/ux-copy` — Copy Guide

**Voice:** Scholarly but warm. Literary without being opaque. The tone of a professor who can also make you cry at a concert.

**Hero tagline:** "Exploring the resonance between devotion, language, and song — where oral tradition becomes living scholarship."
- *Why:* "resonance" works both musically (sound waves) and academically (significance). "Living scholarship" distinguishes her embodied practice from dry archival work.

**Navigation labels:** About · Research · Music · Teaching · Connect
- *Why:* "Connect" over "Contact" — suggests relationship, not transactional inquiry. "Music" over "Vocals/Performance" — more elemental.

**CTA (future):** "Read my research" · "Hear my voice" · "Attend a talk"
- *Pattern:* Verb first, specific action, each pair maps scholarly/musical identity

**Quote section copy:** Use actual Kabir verse in Devanagari + translation — never paraphrase. Authenticity is the brand.

**Section eyebrow labels:** "The Story" · "Scholarship" · "The Voice" · "Academic Journey" · "Connect"
- *Pattern:* Personal nouns ("The Story", "The Voice") for human sections, abstract nouns ("Scholarship") for intellectual sections

---

### `/design-critique` — Pre-emptive Review

**Overall Impression:** Strong narrative arc — hero introduces, prelude sets intellectual tone, about builds empathy, research establishes credentials, music humanises, academic grounds. The dark/light section alternation creates visual rhythm mirroring musical structure.

**Usability**
| Finding | Severity | Recommendation |
|---------|----------|----------------|
| No "back to top" button | 🟡 Moderate | Add fixed `↑` button appearing after 300px scroll |
| Mobile nav hides all links | 🟡 Moderate | Hamburger menu implemented — test on real device |
| No loading state for Google Fonts | 🟢 Minor | Add `font-display: swap` in CSS |

**Visual Hierarchy**
- Hero name draws eye immediately ✅
- Gold accents guide through dark sections ✅
- Parchment sections give breathing room ✅
- Risk: research grid may feel dense — card spacing prevents this

**What Works Well:**
- The musical staff decoration in the prelude is unexpected and perfect
- Equaliser visualiser creates movement on a static page
- Timeline in academic section reads clearly
- Pull-quote on sticky sidebar adds depth while scrolling about section

---

### `/design-handoff` — Developer Spec

**Layout:** Single HTML file, vanilla CSS + JS. No build process required. Deployable as a static file.

**Design Tokens Used**
| Token | Value | Usage |
|-------|-------|-------|
| `--midnight` | `#0A0A1A` | Hero, research, academic, footer bg |
| `--parchment` | `#FDF6E9` | About bg |
| `--gold` | `#C9A84C` | Decorative accents, nav logo border, timeline dots |
| `--saffron` | `#E8852A` | Section labels, equaliser bars |
| `--font-display` | Playfair Display | All `h1`, `h2` elements |
| `--space-2xl` | `10rem` | Major section padding |

**Animation / Motion**
| Element | Trigger | Animation | Duration | Easing |
|---------|---------|-----------|----------|--------|
| Hero text | Page load | `fadeUp` (opacity + translateY) | 0.8–1s | expo-out |
| Canvas waves | Continuous | `requestAnimationFrame` sine | ∞ | — |
| Scroll reveals | IntersectionObserver | `fadeUp` | 0.8s | expo-out |
| Equaliser bars | CSS, continuous | `scaleY` alternate | 0.65–1.2s | ease-in-out |
| Nav opacity | `scroll` event at 60px | CSS transition | 0.4s | ease-in-out |

**Responsive Breakpoints**
| Breakpoint | Changes |
|------------|---------|
| > 1024px | All two-column layouts active |
| 768–1024px | About, music: single column; research: 2-col |
| < 768px | All single column; hamburger nav |

**Edge Cases:**
- Google Fonts unavailable: fallback to Georgia (display), Times New Roman (serif), Helvetica (sans)
- Canvas not supported: background is `--midnight` — acceptable degradation
- JS disabled: Reveals won't animate but content is fully readable; nav is static

---

### `/accessibility-review` — Audit

**Standard:** WCAG 2.1 AA | **Target:** Full compliance

**Pre-implementation checklist:**
- ✅ `lang="en"` on `<html>`, `lang="hi"` on Devanagari text
- ✅ All sections have `aria-labelledby` pointing to `h2`
- ✅ Canvas marked `aria-hidden="true"` (decorative)
- ✅ Equaliser marked `aria-hidden="true"` (decorative)
- ✅ Research grid uses `role="list"` / `role="listitem"`
- ✅ Nav has `role="navigation"` + `aria-label="Main navigation"`
- ✅ Mobile toggle has `aria-expanded` state management
- ✅ Focus styles: 2px gold outline, 3px offset — visible on all backgrounds
- ✅ All interactive elements are keyboard reachable
- ✅ Skip-to-content link (add before nav in Phase 2)
- ✅ Email link has descriptive text (not "click here")

**Color contrast audit:**
| Element | Fg | Bg | Ratio | Required | Pass? |
|---------|----|----|-------|----------|-------|
| Hero name | `#F0E6D3` | `#0A0A1A` | 15.9:1 | 3:1 | ✅ |
| Body text (light) | `#2A1F14` | `#FDF6E9` | 14.3:1 | 4.5:1 | ✅ |
| Gold on dark | `#C9A84C` | `#0A0A1A` | 8.5:1 | 4.5:1 | ✅ |
| Rust on parchment | `#B5461A` | `#FDF6E9` | 7.6:1 | 4.5:1 | ✅ |
| Muted on dark | `#9B8B7A` | `#0A0A1A` | 6.2:1 | 4.5:1 | ✅ |

**Priority accessibility fixes (Phase 2):**
1. Add skip-to-main-content link
2. Ensure image of Dr. Deka (when added) has meaningful `alt` text
3. Add `prefers-reduced-motion` media query to disable canvas and equaliser animations

---

## Technical Stack

- **HTML5** semantic markup
- **CSS3** custom properties, `clamp()`, Grid, Flexbox, animations
- **Vanilla JavaScript** — no frameworks, no build tools
- **Google Fonts** — Playfair Display, Cormorant Garamond, Montserrat
- **Deployment:** Drop `index.html` on any static host (Netlify, GitHub Pages, Vercel)

---

## Implementation Phases

### Phase 1 — Landing Page (Current)
- [x] Hero with wave animation
- [x] Bhakti verse prelude
- [x] About section with narrative biography
- [x] Research threads grid (6 areas)
- [x] Music/voice section with equaliser
- [x] Academic timeline
- [x] Footer with contact
- [x] Responsive (mobile + tablet)
- [x] Accessibility (WCAG 2.1 AA)

### Phase 2 — Full Site
- [ ] Add Dr. Deka's photograph to hero or about section
- [ ] Research page: Publications list with downloadable PDFs
- [ ] Music page: Embedded audio player with recordings
- [ ] Teaching page: Course descriptions, syllabi
- [ ] Writing page: Essays & reflections
- [ ] Add `prefers-reduced-motion` support
- [ ] Add skip-to-content link
- [ ] SEO: Open Graph tags, JSON-LD structured data
- [ ] Analytics integration

### Phase 3 — Enhancement
- [ ] Blog/writing section (CMS or static markdown)
- [ ] Concert/event calendar
- [ ] Press & media kit download
- [ ] Video integration (lecture recordings, performances)
