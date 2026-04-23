# CLAUDE.md

## Project Overview
Marketing agency website for **Dirty Hands Marketing** — web design, local SEO, and Google Business Profile optimization for contractors and home service businesses across North Carolina.

Founded by Davis Rapp (web/marketing) and Jason Lott (contractor). Based near Charlotte, NC. Serving all of NC.

## Tech Stack
- Pure static HTML/CSS/JS (no frameworks — Astro migration deferred until 5+ clients)
- Hosted on Vercel via GitHub
- Contact form: Formspree (action URL already in form tag)
- Fonts: Geist (body) + JetBrains Mono (mono/labels) via Google Fonts
- No build step. No npm. No dependencies.

## Brand Voice
- Gritty, direct, no fluff. Talks to contractors like a contractor.
- Premium execution behind the gritty name (Patagonia tension).
- Microcopy examples: "Built for contractors who actually want leads.", "No templates. No fluff. Just booked jobs.", "Hand-coded. By hand."

## Anti-AI Tells (CRITICAL — applies to all copy and design)

The Dirty Hands brand promise is "hand-built, not templated." Any output that 
reads or looks like a generic AI-generated agency site directly undermines the 
brand. Avoid the following at all costs.



### Punctuation
- **NEVER use em dashes (—).** Replace with periods, commas, parentheses, or 
  rewrite the sentence. Em dashes are the #1 AI tell in 2026.
- Avoid en dashes (–) too. Use a hyphen (-) for ranges or rewrite.
- Avoid the "rule of three" comma pattern ("fast, clean, and reliable"). 
  Vary sentence structure. Sometimes use just two adjectives. Sometimes use one.
- Avoid semicolons in marketing copy. Periods are fine.
- Avoid scare quotes around normal words.

### Words and phrases to NEVER use
- "Elevate" / "elevated"
- "Empower" / "empowering"
- "Unleash" / "unlock the power of"
- "Revolutionize" / "transform" / "transformation"
- "Seamless" / "seamlessly"
- "Cutting-edge" / "state-of-the-art" / "best-in-class"
- "Robust" / "comprehensive" / "holistic"
- "Tailored solutions" / "bespoke" / "curated"
- "Synergy" / "leverage" / "ecosystem"
- "Game-changing" / "next-level" / "next-generation"
- "Drive results" / "drive growth" / "drive value"
- "Whether you're X or Y, we've got you covered"
- "In today's fast-paced world" / "in the digital age"
- "It's not just X, it's Y"
- "Imagine if..." opener
- "Let's dive in" / "let's unpack"
- "At the end of the day"
- "More than just" anything

### Sentence patterns to avoid
- The "X. Y. Z." three-fragment punch ("Fast. Clean. Reliable.") — overused. 
  Use sparingly, max once per page.
- "Not just X, but Y" constructions
- "We don't just X, we Y" constructions
- Opening sentences with gerunds ("Building websites that...")
- Heavy use of triadic structures (lists of three in everything)
- Starting paragraphs with "But" or "And" repeatedly

### How to write copy in this brand
- Short sentences. Then longer ones. Vary the rhythm.
- Use contractions (we're, you'll, don't). Formal copy reads AI.
- Be specific. Not "many businesses" — "the contractor down the road from you."
- Include numbers and concrete details. Not "fast loading" — "loads in under 1 
  second on a phone with bad service."
- Talk like a person who works with contractors, not like a copywriter.
- Acceptable to be slightly blunt. "Your site is broken" reads more human than 
  "Your site has opportunities for improvement."

### Visual AI tells to avoid
- Generic stock-photo aesthetics (smiling diverse team at laptop)
- Gradient mesh backgrounds (the Stripe/Vercel knockoff look)
- Floating glassmorphism cards
- Identical-radius rounded everything (already addressed in Radius System)
- Centered hero with three identical feature cards directly below — overused
- Logo-cloud "trusted by" rows when there's nothing real to put there
- Generic icon sets (Heroicons, Lucide) used everywhere identically
- Identical card grids repeated 5+ times on a page (already addressed in 
  Border Discipline)
- "Hero stat row" with three identical stats in the same font and weight
- Default Tailwind look (slate background, indigo accent, rounded-xl)

### Design choices that signal "made by humans"
- Mixed border weights and radii (per design system)
- Asymmetric layouts in at least one section
- One section that breaks the grid pattern entirely
- Real photos (not illustrations) wherever possible
- Microcopy with personality in unexpected places (form labels, error states, 
  empty states, footer)
- Specific numbers over vague claims
- Imperfect line breaks (a manually-broken hero headline reads more crafted 
  than an auto-wrapped one)

### When generating new copy
Before committing any new copy, scan it for:
1. Em dashes — remove them all
2. Banned words from the list above
3. The "X. Y. Z." pattern
4. Generic agency phrases that could appear on any competitor's site
5. Anything that doesn't pass the test: "Would a contractor I know actually 
   say this?"

If a sentence fails any of these checks, rewrite it. If you can't rewrite it 
without sounding worse, the original idea probably wasn't worth saying.

## Output Quality Bar

Good output should:
- Feel like it was written by someone who has actually worked with contractors
- Use concrete details (numbers, timelines, specific outcomes, real cities)
- Be slightly blunt rather than overly polished
- Avoid sounding like a generic marketing agency
- Pass the test: "Could this appear on 50 other agency sites?" If yes, rewrite it.

Bad output:
- Generic agency phrasing
- Vague claims with no specifics
- Overly polished or corporate tone
- Anything that feels templated, AI-generated, or interchangeable with a competitor's site

When uncertain whether output meets this bar, default to MORE specific, MORE direct, and LESS polished rather than the opposite.

## Design System

### Colors (Dirty Hands palette — final)
```
--bg-primary:        #0A0A0A
--bg-surface:        #141416
--bg-surface-hover:  #1C1C1F
--border-soft:       rgba(255,255,255,0.06)
--border-medium:     rgba(255,255,255,0.10)
--border-strong:     rgba(255,255,255,0.18)
--accent:            #FF5A1F
--accent-hover:      #FF7038
--accent-subtle:     rgba(255,90,31,0.08)
--accent-border:     rgba(255,90,31,0.28)
--text-primary:      #FAFAFA
--text-secondary:    #A1A1AA
--text-muted:        #52525B
```

### Typography
- Body: `'Geist', -apple-system, sans-serif`
- Mono: `'JetBrains Mono', monospace`
- Body line-height: 1.45
- Display headings: tight letter-spacing (-0.02em)
- Uppercase labels: wide letter-spacing (0.18em), mono font, accent color

### Radius System (controlled friction — mixing intentional)
- Cards: 10px
- Buttons: 6px
- Pricing card / hero accents: 12px
- Dividers, stat blocks, badge pills: 0px (sharp)
- **Rule: never mix 0px and 12px in the same component cluster**

### Border Discipline (enforce contrast)
- Sections: no border OR strong divider — never soft
- Cards: soft border
- Featured elements (pricing card, pilot block): medium border
- Don't default everything to soft — that creates the generic look
- Avoid stacking multiple border weights on nested elements. Each visual cluster (a card group, a section, a featured block) should have ONE dominant border weight. Don't put a soft-bordered card inside a medium-bordered container inside a strong-bordered section. That stacks into visual mud.

### Accent Discipline
- `--accent` (#FF5A1F) ONLY for: primary CTAs, key highlights, single-color stat values
- Everything else uses `--accent-subtle` or `--accent-border`
- Overusing primary orange drifts back into "startup SaaS" territory

### Visual Effects
- Subtle noise texture overlay on body (already implemented, keep)
- Subtle radial glow behind hero, pricing, contact sections (already implemented, keep)
- Smooth scroll-triggered fade-in animations with staggered delays
- Mobile-first responsive
- Sticky call bar on mobile

## Visual System Lock
- The design system above is FINAL unless explicitly changed by the user
- All UI must use existing CSS custom property tokens — no new colors unless approved
- No introducing gradients (beyond existing radial glows), glassmorphism, or new visual styles
- No changing font sizes, weights, or families beyond what is defined above
- If something looks "off," fix it using existing tokens, not new ones

## File Structure
```
/
├── index.html
├── work/
│   ├── case-study-concrete.html
│   └── case-study-waterproofing.html
├── services/
│   ├── web-design.html
│   ├── local-seo.html
│   └── google-business.html
├── industries/
│   ├── concrete-contractors.html
│   ├── roofing-contractors.html
│   ├── plumbing-contractors.html
│   ├── hvac-contractors.html
│   └── pressure-washing.html
├── assets/
│   ├── images/
│   │   ├── davis-headshot.jpg
│   │   ├── jason-headshot.jpg
│   │   ├── jason-jobsite.jpg
│   │   ├── davis-working.jpg
│   │   ├── screenshot-concrete.png
│   │   ├── screenshot-waterproofing.png
│   │   ├── pagespeed-concrete.png
│   │   └── pagespeed-waterproofing.png
│   └── site-audit-template.pdf
├── favicon.svg
├── logo.svg
├── sitemap.xml
├── robots.txt
└── CLAUDE.md
```

## Subpage Pattern (services + industries)
- All subpages follow the same template structure: nav (identical to index) → hero (page-specific) → 3-5 content sections → CTA section → footer (identical to index)
- Subpages use the same design tokens, fonts, fade-in animations as index.html
- Each subpage MUST have: unique <title>, meta description with target keyword, canonical URL, og:title, og:description, JSON-LD Service schema (services) or LocalBusiness schema with industry context (industries)
- Service pages target: "[service] for contractors North Carolina" keywords
- Industry pages target: "[trade] website design [city/NC]" + "[trade] SEO" keywords
- All subpages link back to home and to /#contact for primary conversion
- Footer + nav must remain byte-identical across all pages

## Placeholder Asset System (until real photos arrive)
- When real images do not yet exist at the file paths in the structure above, use the branded placeholder system: a CSS-only component with subtle gradient, dotted texture overlay, monospace label like "[ DAVIS — HEADSHOT ]" or "[ JASON — JOBSITE ]"
- Placeholders use --bg-surface background, --border-soft border, --text-muted label color
- Placeholders MUST match the dimensions of the eventual real image so swapping is a 1-line change
- When real images arrive, replace the placeholder div with an <img> tag using the exact path defined in File Structure

## Pricing (locked — graduated model)

### Standard pricing (shown publicly on site)
- Setup: **$1,000** one-time
- Monthly: **$199/mo**
- Month-to-month, no contract
- Add small text under price: *"Most clients graduate to $249/mo as we scale results."*

### Founding Contractor Program (separate section below pricing card)
- Setup: $500 + $149/mo
- 12-month commitment
- 3 spots only (decrement counter as filled, remove section when full)
- In return: testimonial + 2 referrals
- Includes everything in standard plan PLUS: priority turnaround, direct strategy access, public case study feature
- Risk reversal line: *"If we don't deliver something you're proud to show, we don't use it publicly."*
- CTA: **"Apply for a founding spot"** must:
  - Scroll smoothly to the #contact section
  - Focus the "Monthly Revenue Range" select field on arrival
  - Not open a new page, modal, or route
  - Use a standard anchor link (#contact) with JS-enhanced focus behavior
- The "X of 3 spots remaining" counter is **static text only**. Do NOT add JavaScript, dynamic logic, localStorage, API calls, or backend logic to manage this counter. It is updated manually in the HTML by the user when a spot fills.

### Full pricing ($1,500 / $249) — NOT shown on site yet
Internal only. Activates after client #7.

## Phone Number
- Real number: (980) 281-2329
- Display format: `(980) 281-2329`
- tel: link: `tel:+19802812329`
- Appears in: nav, contact section, mobile sticky bar, schema markup

## Contact Form Fields
- Name (required)
- Phone (required)
- Email (optional)
- Business Type (dropdown — existing)
- **Monthly Revenue Range (NEW — required for pilot applications):**
  - Under $250k
  - $250k-$1M
  - $1M+
- Message (optional)

## Rules for Edits
- NEVER remove IDs, classes, or JavaScript unless specifically asked
- NEVER change spacing scale, grid structure, or section widths unless specifically asked
- NEVER reorder sections unless specifically asked
- Preserve all form functionality (Formspree), mobile nav toggle, and scroll behavior
- Respect `prefers-reduced-motion` for animations
- All new pages must match the existing design system exactly
- Keep everything in single HTML files — no extraction, no frameworks
- Case study pages must use the same nav, footer, and design tokens as index.html

## Strict Prohibited Actions
- Do NOT convert HTML into frameworks (React, Astro, Vue, etc.)
- Do NOT extract CSS into separate files unless asked
- Do NOT rename existing classes or IDs
- Do NOT "modernize architecture" or refactor file structure
- Do NOT add libraries, CDNs, or packages unless asked
- Do NOT add icon packs, animation libs, or UI kits
- Do NOT add comments explaining what code does
- Do NOT make assumptions about missing content
- If something is not explicitly defined, ASK before adding it
- Do NOT "enhance UX" beyond explicitly requested changes
- All icons must be inline SVG only
- Do NOT insert placeholder content (e.g., "Lorem ipsum", fake emails like your@email.com, fake phone numbers like 555-555-5555, "Your Company Name", "Insert testimonial here")
- If real content is missing for a section, leave the section untouched or ask for clarification rather than inventing filler
- Do NOT add new sections to any page unless explicitly requested. No "helpful" additions of testimonials sections, FAQ expansions, feature blocks, social proof rows, newsletter signups, or anything else not asked for.

## Copy Lock
- All copywriting is LOCKED unless explicitly requested to change
- Do NOT rephrase, rewrite, shorten, or "improve clarity" of any text
- Do NOT adjust tone, grammar, or marketing language
- Pricing copy, offer language, and CTA text are especially locked
- Microcopy in the brand voice section is the EXCEPTION — use that voice for any newly requested copy

## Reusable Patterns
- Nav, footer, and CTA sections must remain identical across all pages
- Case studies reuse identical layout structure with different content only
- Any new section follows the existing pattern: section-label → section-title → section-subtitle → content grid
- Card components use the same border, radius, padding patterns per the design system

## Editing Behavior Rule
Treat every request as a minimal diff patch:
- Modify only what is required
- Do not refactor surrounding code for "cleanliness"
- Do not reorganize unless explicitly asked
- Do not touch files not mentioned in the request
- Prefer surgical edits over full-file rewrites

## Definition of Done
- Renders correctly on desktop (1440px+) and mobile (320px-768px)
- No broken links or missing assets
- Forms still submit via Formspree
- No layout shift in hero, pricing, or footer
- Mobile nav toggle still works
- Scroll animations still fire
- Lighthouse performance score stays above 95
- All text readable (sufficient contrast)

## Conflict Resolution
- If a requested change conflicts with system rules, prioritize stability over completion
- Ask for clarification instead of guessing
- Never silently override a locked rule

## SEO Notes
- JSON-LD LocalBusiness schema in index.html
- JSON-LD FAQ schema in index.html
- Meta descriptions target "[service] + contractor + North Carolina" keywords
- All pages need: canonical URL, og:title, og:description, meta description
- Sitemap at /sitemap.xml
- Do not modify schema markup unless explicitly asked

## Instruction Priority
1. Strict Prohibited Actions
2. Copy Lock
3. Visual System Lock
4. Rules for Edits
5. Design System tokens
6. Tech Stack constraints
7. SEO Notes
8. General guidance
