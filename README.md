# Mile High Sips — Website

Static site for milehighsips.com. No build step, no framework, no monthly cost.

## Files
- `index.html` — homepage (hero, about, services, full menu, schedule, FAQ, CTA)
- `booking.html` — event inquiry form
- `thanks.html` — confirmation page after form submit
- `assets/` — drop logo, photos, og-image.jpg here

## Local preview
Open `index.html` in a browser. That's it. (Tailwind, fonts load from CDN.)

## Deploy (recommended: Netlify, free)

1. Sign up at https://netlify.com (free).
2. Drag the `milehighsips` folder onto the Netlify dashboard. Site goes live in seconds at a `*.netlify.app` URL.
3. **Forms:** the booking form already has `data-netlify="true"` — Netlify will auto-detect it. Submissions show up under **Forms** in the Netlify dashboard.
4. **Email notifications:** in Netlify → Site settings → Forms → Form notifications → add email notification → send to `info@milehighsips.com`.
5. **Custom domain:** Netlify → Domain settings → Add `milehighsips.com`. Netlify gives you DNS records — point the domain there at your registrar. SSL is automatic and free.

## Alternate deploys
- **Cloudflare Pages** — also free, just as easy. Forms need a separate service (Formspree, Web3Forms).
- **GitHub Pages** — free, but no built-in form handling. Use Formspree (`<form action="https://formspree.io/f/YOUR_ID">`) instead.

## Editing the schedule
Open `index.html`, search for `id="schedule"`. Each event is a `ticket` div — copy/paste a block and edit the date + name + location. Takes ~30 seconds per event.

## Editing the menu
Open `index.html`, search for `id="menu"`. Each drink is a `menu-card` div. Same pattern — copy, paste, change name + ingredients.

## Add real photos
1. Save photos into `assets/` (use compressed JPGs, ~300KB each).
2. Replace the placeholder "Photo of the team" div in the About section with: `<img src="assets/team.jpg" class="w-full h-full object-cover rounded-[2rem]" alt="Mile High Sips team" />`
3. Add a `og-image.jpg` (1200x630) to `assets/` for social link previews.

## Future ideas
- Online ordering for public pop-ups (Square or Stripe Checkout)
- Gift cards
- Loyalty / "Frequent Flyer" punch card
- Blog or "where we've been" archive
