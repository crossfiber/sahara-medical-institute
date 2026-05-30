# Borrowed code patterns

Source build read in full: **keys-chocolates** (`C:\Users\accc0\Downloads\Agency\Recycle Bin\Outdated Sites\keys-chocolates\index.html`).

Picked because Sahara Medical Institute is a multi-section local-business with multiple service categories, multiple providers, multi-payer insurance - same structural fit as Keys (multi-location retail with multiple product categories).

Borrowed for code quality, NOT visual identity. Sahara gets its own palette (coral + sage), its own fonts (Fraunces + Plus Jakarta Sans), and its own signature hero (founder portrait + bilingual badge - NOT the Keys interactive map).

## Patterns borrowed

### 1. CSS variable architecture + nav-height variable system
Source lines ~43-68. Adopting `--nav-h: 84px` desktop / `70px` mobile and the matching `html { scroll-padding-top: calc(var(--nav-h) + 16px) }` so anchor links land cleanly under the sticky nav at every breakpoint.

### 2. Mobile drawer system
Source lines ~179-254 (CSS) + ~2229-2253 (JS). Right-side `transform: translateX(100%)` drawer, `body.drawer-open` class to hide the trigger when the drawer is open, `body.style.overflow = 'hidden'` lock, safe-area-inset padding, slideInLeft link animation, drawer-footer phone pill (white background, brand-color text + icon). Adopting wholesale, restyled to sage/coral.

### 3. Trust bar overlap pattern
Source lines ~432-454. `margin-top: -56px` on a solid dark band over the hero bottom, with `position: relative; z-index: 5` so it overlaps cleanly. Replacing the Keys multi-number stat layout with a prose-rhythm trust line per the Sahara design direction.

### 4. About photo + year-badge overlap
Source lines ~503-538. Wrapping the image in `.about-photo > .about-photo-inner` so the year badge can `translate(-50%, 50%)` outside the image's `overflow: hidden` clip. Adopting for the founder/about section.

### 5. Service card CTA bottom-alignment via flex
Source lines ~568-660. `display: flex; flex-direction: column` on card body, `flex: 1` on description container, `margin-top: auto` on CTA. Solves the CTA staircase across same-row cards with variable content lengths.

### 6. Scroll-snap horizontal carousel (mobile)
Source lines ~807-837 + ~1067-1104 (reviews carousel). `scroll-snap-type: x mandatory`, `scroll-snap-align: center`, `flex: 0 0 ~78%`, hidden scrollbars, matching `scroll-padding-left/right`. Adopting for the providers carousel.

### 7. FAQ accordion single-open behavior
Source lines ~1113-1148 (CSS) + ~2254-2265 (JS). `max-height: 0` to `max-height: 500px` transition (NEVER `display: none` mix), single-open by removing `.open` from all siblings before adding to the clicked one, `aria-expanded` sync. Adopting verbatim with sage/coral palette.

### 8. Contact form + side info card stack
Source lines ~1150-1270. Form left (white card with cream input backgrounds + branded focus border), side info column right (white cards with colored border-left). Adopting.

### 9. Sticky-nav scroll-shadow without transparent-to-solid
Source lines ~2220-2227. Solid nav from load, scroll just deepens shadow on `.scrolled` class. Avoids the iOS Safari transparent-nav bug and the contrast issues that come with it.

### 10. JSON-LD multi-block pattern
Source lines ~2323-2572. Separate `Organization` + `MedicalBusiness` (in our case) + `FAQPage` blocks. Adopting the structure, populating with Sahara facts (no aggregate rating since Google is unverified).
