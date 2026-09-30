# Neat Laundry Website Plan

## Product outcome
A polished single-page demo website for Neat Laundry, a premium laundry and dry-cleaning service. The experience should convert visitors into pickup requests through a clear WhatsApp booking flow while communicating reliability, fabric expertise, and delivery convenience.

## Design direction
The user-selected direction is a clean, sleek, trustworthy laundry-service identity using Clean Blue `#0284c7`, Crisp White `#ffffff`, Soft Light Gray `#f8fafc`, and Dark Navy `#0f172a`. The layout uses spacious editorial sections, rounded cards, restrained shadows, large readable typography, and subtle motion. The supplied Neat logo is the primary brand asset; the hero uses a custom laundry visual and the About section uses a selected professional laundry interior image.

## Architecture
- Static HTML/CSS/JavaScript site with one public route: `/`.
- No server, database, login, or private data is needed for this demo. The form formats a WhatsApp deep link in the browser.
- Source files: `index.html`, `styles.css`, `script.js`, `assets/` for local images, plus `ideas.md` and this plan.
- Static delivery is the appropriate deployment choice: all page content is known ahead of time, first-load HTML is content-bearing for SEO, and the only dynamic behavior is client-side UI state and WhatsApp navigation.
- Browser caching: keep HTML revalidated; local assets can be served as static public files. No API routes or SPA fallback beyond `/` are needed.

## Experience
1. Sticky header with responsive nav and strong Book Pickup CTA.
2. Hero with headline, supporting copy, CTAs, trust stats, and laundry image collage.
3. About/benefits section with service promise and four benefit cards.
4. Service tabs with prices for common garments and a clear active state.
5. Booking section with validated form and WhatsApp message formatting.
6. Testimonials with Google-style rating treatment.
7. Footer with quick links, hours, location, map placeholder, and social links.

## Behavior
- Smooth-scroll all internal links.
- Mobile menu toggles open/closed with accessible `aria-expanded`.
- Service tabs update visible pricing panel and selected service in the booking form.
- Schedule A Pickup / Book Pickup scroll to the booking form and focus the first field.
- WhatsApp order button opens a prefilled WhatsApp conversation.
- Booking submission validates required fields, constructs a human-readable order summary, and opens `https://wa.me/971500000000` in a new tab; this is a clearly labeled demo business number.
- Newsletter-style micro-interactions are not needed; avoid pretending to persist data.

## Validation
- Inspect source for complete requested sections, exact copy, asset references, accessible labels, and no broken local paths.
- Run a lightweight static server on the managed Preview port and verify HTTP readiness plus HTML/CSS/JS syntax through local checks.
- Check the route manifest before first server start.
- Use the platform's managed diagnostics configuration as applicable; no screenshot or browser automation is required for ordinary validation.
