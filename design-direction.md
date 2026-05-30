# Sahara Medical Institute - Design Direction

## Site diagnosis (Step 2)

Live site is a generic Material-Icons template that buries the offering. Specific problems:

1. The name "Sahara Medical Institute" never communicates "pediatrician" or "kids." Their own social handles (@vegaspediatrics, @vegaspeds) prove they know it.
2. Hero is three stylized PNG banner placeholders. Zero real photography of the team, clinic, or families.
3. Primary CTA is broken: the header phone number links to `#!` (a no-op). No prominent booking action. Telemedicine is a Google Forms link for one provider only.
4. Bilingual differentiator is buried as a tiny `*language*` icon in the hero row. Dr. Peraza is a Spanish-speaking pediatrician, Katelyn Heck is fluent in Spanish, and both testimonials read in a Spanish-language voice. That's a primary acquisition lever for the Vegas Hispanic family base, not a footer afterthought.
5. Stale dual-mission copy on every provider page: "twofold mission: skincare AND pediatrics." The home page is pediatrics-only. The Products section still lists Obagi, Epionce. Outdated pivot debris.
6. Hours discrepancy: home page says Mon-Fri 8:30am-5pm; provider pages say Mon/Wed 10am-6:30pm, Tue/Thu/Fri 9am-5pm. Cross confirmed provider-page hours are correct.
7. No "new patient" onboarding flow. No "what to expect at first visit," no online intake, no clear walk-in policy above the fold.
8. Insurance section is a 16-logo grid with no quick "do you take mine?" affordance.
9. Cloudflare email obfuscation breaks the office manager email for crawlers and some clients.

What to preserve: real provider bios with personality (Dr. Mendoza's Bears fandom, Katelyn's CrossFit, Dr. Peraza's vintage cars). Comprehensive insurance acceptance. The blog. The walk-in policy. Multilingual care.

## Competitive research (Step 3)

Looked at three categories: best-in-class pediatric practice sites nationally, Las Vegas pediatric competitors, and bilingual community-health practice sites in border-state cities.

Common patterns the category overuses: cool clinical blue palettes, "We Care" generic taglines, stock photos of smiling families with white doctors, big stethoscope icons in feature blocks, dashboard stat strips ("10,000+ families served"), and the same friendly-sans-serif fonts (Poppins / Open Sans / DM Sans) on every site. The whole category looks built from the same Wix template.

What works and is worth borrowing in spirit, not copy: real provider portraits over stock; "what to expect at your first visit" trust panels; bilingual toggle as a real first-class element, not a flag in the footer; multi-provider booking grids where each provider has a click-to-call/telemed button next to their name.

What to break from: the cool blue palette. Going warm.

## Design Direction Declaration

Warm, family-run, bilingual pediatric clinic that feels lived-in since 2007 - built on a coral-and-sage palette with a serif (Fraunces) headline that reads "trusted institution," not "cold medical." The signature hero element is a real photo of Dr. Peraza with a "Hablamos Español · Pediatra de Las Vegas desde 2007" badge overlapping the bottom edge - the founder, the bilingual promise, and the founding year in one frame, specific to this practice and impossible to swap to a generic competitor. Deliberately avoiding: every default in the category - cool medical blue, stock-family imagery, stethoscope icons, "We Care" headlines, dashboard stat strips, transparent-to-solid sticky nav, glassmorphism, and Poppins/Open Sans.

## Color palette (sourced)

- **Coral red `#D94F3A`** - Primary brand / CTA. Warm Latino-family warmth, kid-safe, signals action. Source: derived from the warm-clay tones common to Las Vegas Spanish-speaking community spaces; rejects the generic clinical blue the category overuses.
- **Coral deep `#A8351F`** - Hover state for CTA. Same family, deeper.
- **Sage `#7BA888`** - Supporting. Trust + pediatric "calm" without going corporate. Used for trust strip background, "verified" pills, success states.
- **Sage deep `#3D5E47`** - Dark sage for footer + dark sections. Derived from sage by darkening, not picking a generic charcoal.
- **Cream `#FBF7F0`** - Dominant neutral background. Warm, not stark white.
- **Cream warm `#F3EBDA`** - Section alternate (used sparingly).
- **Charcoal `#2A2724`** - Body text. Warm dark brown-charcoal, not pure black. Pairs with cream.
- **Charcoal soft `#5A544D`** - Secondary text.
- **Cream muted `#EFE6D2`** - Card hairlines, dividers.
- **Gold `#D9A55C`** - Used ONLY for star icons in reviews. Not a fourth brand color.

60-30-10: 60% cream backgrounds, 30% sage/charcoal panels, 10% coral reserved for CTAs and clickable phone numbers.

## Typography (verified on Google Fonts)

- **Headlines: Fraunces** - `https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600;9..144,700&display=swap`. Variable serif with warmth. Says "established institution" + "human, not corporate." Handles Spanish characters cleanly.
- **Body: Plus Jakarta Sans** - `https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap`. Friendly geometric sans, excellent legibility at 16px, holds up in long Spanish phrases.

Combined import URL (one request):
`https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600;9..144,700&family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap`

Both verified live at fonts.google.com. No fallback drift.

## Signature hero element

A real photo of Dr. Francisco Peraza with a coral pill badge overlapping the bottom edge reading "Hablamos Español · Pediatra de Las Vegas desde 2007." Founder + bilingual promise + founding year in one frame. Cannot be swapped to a competitor without recreating all three claims, all of which are this practice's specific facts.

NOT used: no canvas particles, no animated dashboard stats, no swing-diagram, no SVG ring charts, no abstract gradient mesh. The hero earns its place by being verifiably this clinic and no other.

## Section architecture (variation plan)

Consecutive structural variation enforced - no two sections share a layout pattern.

1. **Nav** - Solid coral-cream on page load (no transparent-to-solid). Spanish toggle promoted to first-class nav pill (not a tiny footer icon). Phone CTA always visible right side.
2. **Hero** - Split. H1 + lede + CTAs left, founder photo + bilingual badge right. Mobile reorders: eyebrow → H1 → CTAs → photo → lede.
3. **Trust strip overlap** - `margin-top: -56px` over hero bottom. Three facts woven as a prose-rhythm sentence ("Bilingual care · Newborns to age 21 · Same-day sick visits"), NOT a 3-col big-number stat grid. Skips the "SaaS stats bar" blacklist pattern entirely. Aggregate rating omitted (no verified Google number yet).
4. **About / Founder story** - Split, REVERSED from hero (image left, text right). Lead with a pull-quote eyebrow ("Building Vegas families' trust since 2007.") instead of the small-caps label. Year badge overlap on the photo.
5. **Services** - Three cards. Well-child visits / Sick & walk-in care / Specialty services (ADHD, sports physicals, vaccines, etc.). NOT all 9 service pages flattened into a grid - three buckets, each card visually weighted differently. CTAs bottom-aligned via flex. NO accordion on desktop.
6. **Providers** - Horizontal scroll-snap carousel (different from services card grid). Four providers, each with photo + name + credentials + "About Dr. X" tap. Mobile uses `flex: 0 0 78%` with scroll-snap-align: center. Carousel arrows below the row, not overlapping cards.
7. **Insurance** - Compact pill cloud (different from grid + carousel). 16 carriers as text pills, grouped: Major Plans / Local Plans / Union & Federal. Faster to scan than the current 16-logo soup.
8. **FAQ** - Single-column accordion with 8+ real questions sourced from likely parent objections (walk-ins, languages, telemedicine, newborns, school physicals, hours, what insurance covers, first-visit prep). Single-open behavior, max-height transition.
9. **Contact** - Split. Form left (novalidate + branded JS validation), contact card stack right (address + click-to-call + hours + map embed since they have a real walk-in address).
10. **Footer** - 4 columns (brand+social / care / visit / contact). Real colored logo, never CSS-inverted. `<address>` semantic. Mailto + tel links live.

## AI Pattern Blacklist temptations and counters

- **#3 SaaS Stats Bar** - Tempted to do "4 providers · 19 years · 16 insurance plans · 1000+ patients." Avoided. Replaced with a prose-rhythm trust line.
- **#5 Safe Font Fallback** - Tempted to default to Outfit or DM Sans. Picked Fraunces + Plus Jakarta Sans for category-correct warmth.
- **#6 Generic Hero Headline** - "Trusted Pediatric Care for Las Vegas Families" works for any clinic. Rewriting to: "Bilingual pediatric care in West Vegas, from newborns through high school - by the same family practice since 2007." Names city + clientele + differentiator (bilingual) + founding year.
- **#9 Retroactive Narrative** - Coral + sage chosen for documented Hispanic-family demographic + pediatric trust convention. Not "felt right."
- **#12 Transparent-to-solid nav** - Solid from load.
- **#13 Inverted logo** - Sahara logo stays in its real colors on the dark footer.
- **#18 Em Dash Tell** - Zero em dashes anywhere. Will grep before deploy.

## Mobile hero element order (designed independently from desktop)

1. Eyebrow chip ("Vegas Pediatrics · Pediatra Bilingüe")
2. H1 (short form: "Bilingual pediatric care in West Vegas, since 2007.")
3. Primary CTA (Call) + Secondary CTA (Telemed) side by side
4. Founder photo with bilingual badge
5. Lede paragraph

Conversion path lands above the photo. Photo + lede below the fold.

## Mobile interaction map

- Nav: hamburger → right-side drawer (designed surface, brand-typography link list, drawer footer with white phone pill + telemed CTA)
- Hero CTAs: 44×44 minimum tap targets, both reachable above the fold on 6.1"
- Services: stays 1-up on mobile because cards are content-dense (image + bullets + CTA). Each card flex-aligned with CTA at bottom.
- Providers: scroll-snap carousel, peek 22% of next card, snap-align center
- Insurance: pill cloud reflows naturally
- FAQ: tap header → max-height transition open, single-open behavior
- Contact: form fields stack 1-col, submit button full width

## Bottom-alignment + collapse strategies

- Service cards: `display: flex; flex-direction: column` on card body + `flex: 1` on description container + `margin-top: auto` on CTA.
- FAQ accordion: `max-height` transition with `cubic-bezier(0.4, 0, 0.2, 1)` 0.34s on every accordion-content. NEVER `display: none` mixed in.
- Mobile drawer: `transform: translateX(100%)` to `translateX(0)` with 0.32s ease.
- Body lock on drawer open: `document.body.style.overflow = 'hidden'`.
