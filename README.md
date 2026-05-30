# Sahara Medical Institute - Build README

**Business:** Sahara Medical Institute / Vegas Pediatrics
**Target site:** https://www.saharamedicalinstitute.com/
**Date built:** 2026-05-30
**Owner contact:** (702) 331-1700 · 5781 W Sahara Ave #500, Las Vegas, NV 89146
**Live URL:** https://crossfiber.github.io/sahara-medical-institute/
**Repo:** https://github.com/crossfiber/sahara-medical-institute

## Stack

- Single-file `index.html` (all CSS + JS inline)
- Google Fonts: **Fraunces** (headlines) + **Plus Jakarta Sans** (body)
- Font Awesome 6.5.1 (CDN)
- No build step. Deploys directly via GitHub Pages.

## Color palette

| Token | Hex | Source |
|---|---|---|
| `--coral` | `#D94F3A` | Primary brand / CTA. Warm Latino-family palette, picked for Vegas Hispanic patient base. |
| `--coral-deep` | `#A8351F` | CTA hover. |
| `--sage` | `#7BA888` | Pediatric trust signal, supporting brand. |
| `--sage-deep` | `#3D5E47` | Dark sections, footer, headline color. |
| `--cream` | `#FBF7F0` | Page background, warm white. |
| `--cream-warm` | `#F3EBDA` | Section alternate. |
| `--charcoal` | `#2A2724` | Body text. Warm dark brown, not pure black. |

## Provider photos (downloaded from live CDN)

All in `assets/`:
- `logo-mark.png` - Logo mark from cdn1.saharamedicalinstitute.com (5.7 KB)
- `dr-peraza-portrait.png` - Hero + provider carousel
- `dr-peraza.jpg` - About / founder section
- `katelyn-heck.png`, `dr-mendoza.png`, `nichole-fernandez.jpg` - Providers carousel

## Placeholders that still need real content

- `[REAL GOOGLE RATING NEEDED]` - Verified Google rating + review count. Currently omitted from trust strip and from JSON-LD `aggregateRating`. Yelp shows 44 reviews; Google rating couldn't be auto-confirmed. The site reads cleanly without it; add once verified.
- **Hours discrepancy unresolved by client:** the live site shows two different hours sets. We picked the **provider-page version** (Mon/Wed 10am-6:30pm, Tue/Thu/Fri 9am-5pm) per Cross's instruction. Owner should confirm before going live.
- **Nichole Fernandez bio** - Stub bio since live site has no provider page for her yet. Replace with her real credentials and background when client provides.
- **og-share.jpg** - Share card not yet created. Need a 1200×630 composite (brand mark + "Bilingual Pediatrics in West Vegas" + key facts). Currently referenced in OG meta but file not present.
- **Office manager email** - Currently directs nursing-preceptorship inquiries through the contact form (the live site uses Cloudflare email obfuscation, which we don't replicate). Client should add a real `mailto:` if they want direct.
- **Spanish version** - Spanish toggle is wired and shows a friendly alert. Full Spanish translation is a phase-2 deliverable.

## Hotlinking risk

Logo and provider photos are downloaded to `assets/` (no hotlinking dependency). The Google Maps embed iframe is the only external dependency aside from fonts and Font Awesome.

## Reference build consulted

`keys-chocolates` (from `Agency/Recycle Bin/Outdated Sites/`). Borrowed: CSS variable + nav-height system, mobile drawer pattern, trust-bar overlap, about-photo year-badge overlap, service card flex bottom-align, scroll-snap carousel, FAQ accordion single-open, sticky-nav scroll shadow without transparent-to-solid, JSON-LD multi-block. Did NOT borrow: palette, fonts, headline copy, hero composition, signature visual element. See `borrowed-patterns.md` for line refs.

## To deploy

1. Cross provides GitHub PAT with `repo` scope.
2. Create public repo `crossfiber/sahara-medical-institute`.
3. Push `index.html` + `assets/` (exclude `credentials.md` via `.gitignore` or simply don't add).
4. Enable Pages on `main` branch root.
5. Live URL: `https://crossfiber.github.io/sahara-medical-institute/`.
