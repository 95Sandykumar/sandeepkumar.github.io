# WEBSITE-BRIEF.md — Sandeep Kumar portfolio (AI/Agentic reposition)

Built via `build-website` skill, 2026-07-07. Real-code branch, Tier 1 (static HTML + GSAP + Lenis), deploys to GitHub Pages `main`.

## Goal
Reposition the live portfolio from "Data & AI Engineer" to **AI / Forward Deployed Engineer with agentic + full-stack experience**. Content source = `Sandeep Kumar_AI engineer with Agentic experience_20260623.docx`. Keep the existing content structure; upgrade interactivity to real scroll animation.

## Constraints (from Boss)
- Keep the initial site's **content structure** (section order + component types).
- Make it **more interactive** using the build-website scroll-animation features (GSAP ScrollTrigger + Lenis).
- Add a **résumé download** button served from the PDF (`assets/docs/Sandeep-Kumar-AI-Engineer.pdf`).
- New visual build is fine; structure is fixed.

## Sitemap
Single page (`index.html`). `service-details.html` / `starter-page.html` are legacy, untouched.

## Section list (order preserved from live `main`)
1. Nav — brand SK, links Work/Portfolio/Toolkit/Path, LinkedIn + Get-in-touch, hamburger
2. Hero — status pill, name + accent role, lead, CTAs (See work + Download résumé) | right: `profile.json` cred card + count-up mini-stats
3. Marquee — scrolling agentic/AI tech keywords
4. 01 The short story — 3 copy paragraphs + facts sidebar
5. 02 Selected work — bento of 4 tiles (Becker's production agentic work)
6. 03 Portfolio — masonry image gallery (existing data-viz/BI shots, kept)
7. 04 Toolkit — 6 grouped skill rows
8. 05 Path — timeline of 4 roles
9. 06 Testimonials — 4 recommendation quotes (kept, role-agnostic)
10. 07 Contact — CTA + Download résumé + contact links
11. Footer

## Primary conversion path
Recruiter reads hero → scans agentic work → **Download résumé** or **Email/LinkedIn**.

## Tech tier
Tier 1: single static `index.html`, GSAP 3.12.5 + ScrollTrigger + Lenis via CDN. No build step. IntersectionObserver reveal fallback if CDNs fail; full `prefers-reduced-motion` guard.

## Design tokens
- Base: light editorial (kept). `--bg:#fafafa`, `--ink:#09090b`, Geist + Geist Mono.
- Accent shifted emerald → **indigo `#4f46e5` / `#4338ca`**, soft `#eef2ff` (signals the AI reposition; single-accent discipline kept).
- Radius 1.5rem, shadow-soft, `cubic-bezier(0.16,1,0.3,1)`.
- New texture: subtle masked dot-grid behind hero.

## Scroll/interaction layer (the interactivity upgrade)
- Lenis smooth scroll (progressive enhancement).
- GSAP ScrollTrigger: top scroll-progress bar, hero cred-card parallax, count-up mini-stats, staggered section reveals.
- Kept: magnetic buttons, bento spotlight-follow; added: subtle card tilt.
- All motion wrapped for `prefers-reduced-motion` + no-JS fallback.

## Content source of truth
Resume summary, 5 roles (Becker's, Decision Point, Volvo, Indiana University, Spirent), 5 projects, and the grouped skills list from the 6th-July AI/agentic resume. No fabricated experience.
