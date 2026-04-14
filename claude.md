# CLAUDE.md

## Project Overview
This is the website for a web design + SEO agency (name TBD — currently using "PLACEHOLDER" throughout). We build fast, hand-coded websites and provide local SEO services for contractors and local service businesses across North Carolina.

Founded by Davis Rapp and Jason Lott. Based near Charlotte, NC.

## Tech Stack
- Pure static HTML/CSS/JS (no frameworks yet — Astro migration planned later)
- Hosted on Vercel via GitHub
- Contact form: Formspree (action URL in form tag)
- Fonts: DM Sans (body) + JetBrains Mono (mono/labels) via Google Fonts
- No build step. No npm. No dependencies.

## Design System

### Color Palette (Palette B — true black + electric orange)
- `--bg-primary: #000000`
- `--bg-secondary: #050505`
- `--bg-card: #0A0A0A`
- `--bg-card-hover: #111111`
- `--text-primary: #FFFFFF`
- `--text-secondary: #888888`
- `--text-muted: #555555`
- `--accent: #FF6B1A`
- `--accent-hover: #FF8A47`
- `--accent-glow: rgba(255, 107, 26, 0.15)`
- `--accent-subtle: rgba(255, 107, 26, 0.06)`
- `--border: rgba(255,255,255,0.08)`
- `--border-accent: rgba(255, 107, 26, 0.3)`

### Typography
- Body: `'DM Sans', -apple-system, sans-serif`
- Mono (labels, tags, stats): `'JetBrains Mono', monospace`
- Hero h1: weight 700, tight letter-spacing
- Section titles: weight 600
- Body text: weight 400, line-height 1.6
- Section labels: mono, uppercase, letter-spacing 3px, accent color

### Design Principles
- Dark, modern, sleek. Inspired by Linear/Vercel aesthetic but adapted for trades audience.
- Subtle radial glow effects behind key sections (hero, pricing, contact)
- Smooth scroll-triggered fade-in animations with staggered delays
- Card hover states use subtle box-shadow glow, not just border color
- No gradients on surfaces. Flat dark cards with thin borders.
- Noise texture overlay on body (subtle, pointer-events: none)
- Mobile-first responsive. Sticky call bar on mobile.

## Visual System Lock
- The design system above is FINAL unless explicitly changed by the user
- All UI must use existing CSS custom property tokens — no new colors unless approved
- No introducing gradients, glassmorphism, frosted glass, or new visual styles
- No changing font sizes, weights, or families beyond what is defined above
- If something looks "off," fix it using existing tokens, not new ones

## File Structure
```
/
├── index.html                      # Homepage (main landing page)
├── case-study-concrete.html        # Case study: concrete contractor
├── case-study-waterproofing.html   # Case study: waterproofing company
├── sitemap.xml
├── robots.txt
├── CLAUDE.md                       # This file
```

## Current Pricing (display on site)
- Website build (one-time): $300
- SEO + maintenance (monthly): $99 - $199/mo
- Free site audit as lead magnet

## Key Business Rules
- Target audience: contractors first, open to other local service businesses
- Service area: all of North Carolina
- Contact: phone (980) 281-2329 + Formspree contact form
- No contracts — month-to-month positioning
- Brand name is TBD. "PLACEHOLDER" is used everywhere. When we have a name, find-and-replace globally.

## Phone Number
- Real number: (980) 281-2329
- Must always be formatted exactly as: (980) 281-2329
- tel: link must always be: tel:+19802812329
- Do not reformat, abbreviate, or hyperlink it inconsistently
- Appears in: nav, contact section, mobile sticky bar, schema markup

## Rules for Edits
- NEVER remove IDs, classes, or JavaScript unless specifically asked
- NEVER change spacing scale, grid structure, or section widths unless specifically asked
- NEVER reorder sections unless specifically asked
- Preserve all form functionality (Formspree), mobile nav toggle, and scroll behavior
- Respect `prefers-reduced-motion` for animations
- All new pages must match the existing design system (colors, fonts, spacing, card styles)
- Keep everything in single HTML files until Astro migration happens
- Case study pages must use the same nav, footer, and design tokens as index.html

## Strict Prohibited Actions
- Do NOT convert HTML into frameworks (React, Astro, Vue, etc.)
- Do NOT extract CSS into separate files unless asked
- Do NOT rename existing classes or IDs
- Do NOT "modernize architecture" or refactor file structure
- Do NOT add libraries, CDNs, or packages unless asked
- Do NOT change copywriting unless explicitly requested
- Do NOT introduce new animation libraries or frameworks
- Do NOT add comments explaining what code does (keep files clean)
- Do NOT make assumptions about missing content, features, or sections
- If something is not explicitly defined, ask before adding it
- Do NOT "enhance UX" beyond explicitly requested changes
- No external libraries via CDN (including icon packs, animation libs, UI kits)
- All icons must be inline SVG or existing assets only
- Do NOT add new meta tags, scripts, preload links, or head elements unless explicitly requested

## Copy Lock
- All copywriting is LOCKED unless explicitly requested to change
- Do NOT rephrase, rewrite, shorten, or "improve clarity" of any text
- Do NOT adjust tone, grammar, or marketing language
- Do NOT change headings, subheadings, button labels, or placeholder text
- Pricing copy, offer language, and CTA text are especially locked

## Reusable Patterns
When editing or adding sections:
- Keep structure consistent across all pages
- Nav, footer, and CTA sections must remain identical across all pages
- Case studies must reuse identical layout structure with different content only
- Any new section should follow the existing pattern: section-label → section-title → section-subtitle → content grid
- Card components use the same border, radius, padding, and hover pattern everywhere

## Editing Behavior Rule
Treat every request as a minimal diff patch:
- Modify only what is required to fulfill the request
- Do not refactor surrounding code for "cleanliness"
- Do not reorganize code structure unless explicitly asked
- Do not touch files that are not mentioned in the request
- Prefer surgical edits over full-file rewrites

## Definition of Done
Before considering any task complete:
- Page renders correctly on desktop (1440px+) and mobile (320px-768px)
- No broken links or missing assets
- Forms still submit via Formspree
- No layout shift in hero, pricing, or footer
- Mobile nav toggle still works
- Scroll animations still fire
- Lighthouse performance score stays above 95
- No unnecessary JS or CSS was added
- All text is readable (sufficient contrast against backgrounds)

## Conflict Resolution
- If a requested change conflicts with system rules, prioritize stability over completion
- Ask for clarification instead of guessing
- Never silently override a locked rule to complete a task

## Iteration Workflow
- Make small, incremental changes per request
- Prefer editing existing code over rewriting entire files
- Return only modified sections when possible
- Avoid full-file rewrites unless explicitly requested
- When in doubt about intent, ask before changing

## Instruction Priority
If any instruction conflicts with another, follow this order:
1. Strict Prohibited Actions (highest priority)
2. Copy Lock
3. Rules for Edits
4. Visual System Lock
5. Design System tokens
6. Tech Stack constraints
7. SEO Notes
8. General guidance (lowest priority)

## SEO Notes
- JSON-LD LocalBusiness schema in index.html
- JSON-LD FAQ schema in index.html
- Meta descriptions target "[service] + contractor + North Carolina" keywords
- All pages need: canonical URL, og:title, og:description, meta description
- Sitemap at /sitemap.xml
- Do not remove or modify schema markup unless explicitly asked
- SEO rules apply to index.html and case study pages unless otherwise specified