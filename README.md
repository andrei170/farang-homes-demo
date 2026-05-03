# Farang Homes — Website Demo v1

**Status:** BUILT v1 (2026-05-03)
**Live (deploy options below):** TBD until pushed
**Audit score (current site):** 22 / 50 — see `audit.md`
**Decision:** Reposition the brand. They're a creator team with 16M YouTube views, not a marketplace. The site should look like the YouTube channel does.

## What we built

A single-page cinematic site built around the actual brand promise: HD walk-throughs of Thai property, a 30-page buying guide, and a "feature your property" service for owners + developers. Eight sections, all on one self-contained HTML file:

1. **Hero** — Cinematic Thailand drone shot with Ken Burns animation. Headline "Thailand property, walked through frame by frame." Two CTAs (buying guide + watch walk-through). Live "now filming" eyebrow with pulse dot. Group-stats column anchored bottom right.
2. **The Group / Stat Band** — 6-tile band with the audience numbers (300K IG · 16M YT · 550K total · 1,000+ walk-throughs · 8 cities · 30-page guide). Source disclaimer included.
3. **Who It's For** — 3-card segmentation: International Buyers / Property Owners + Developers / Investors + Long-Stay Renters. Each card lists what they get on the site.
4. **The Walk-Through Series** — 6-card grid showcasing sample walk-throughs as a property catalog. Hover scale, gold play button overlay. Tagged by city + property type.
5. **The Buying Guide** — Email-gated lead magnet section. eBook cover mock with `Cormorant Garamond` italic title. Form captures email; PDF delivers via the deployed version.
6. **The Eight Cities** — 4×2 grid of Thai cities (Phuket, Bangkok, Koh Samui, Hua Hin, Pattaya, Chiang Mai, Krabi, Koh Phangan). Each shows walk-through count.
7. **For Owners — How We Work** — Three-step process: Brief + Capture Day → Cinematic Cut + Approval → Distribution + Buyer Inflow. Less-than-14-day delivery promise.
8. **Founder Story** — Photo-led story block, cinematic quote inside the photo, founding-year stat row. Reinforces that this is a creator team, not an agency.
9. **Final CTA** — "Three doors. Pick one." — Watch / Get Guide / Feature Property.
10. **Footer** — Brand line, four columns (Watch / Buyers / Owners / Social), bottom row with cities + social links.

## Visual language

- **Palette:** Deep ocean navy (`#0a1830`) base, teal accent (`#00bfa5` Andaman Sea), warm gold (`#d4af6c`), cream (`#fbf6ec`). Tropical luxury, not corporate-blue.
- **Typography:** Bebas Neue (display, all caps headers), Cormorant Garamond (italic accents — "walked through", "frame by frame", italic city names), Inter (body).
- **Photography:** All Unsplash, all Thailand-relevant. Real photo URLs verified before publish. Hero is a tropical pool villa drone shot.
- **Hero animation:** Ken Burns slow-zoom on the bg image (28s loop). Pulse dot on "now filming" eyebrow.
- **Demo strip:** Bottom-fixed teal bar reading "Sample build by AG1 Consulting · Faranghomes brand assets, photography, and offer slot in on Day 1." Dismissable for screenshots.

## Tech notes

- **Single self-contained `index.html`** (no external CSS, no JS framework). Pure HTML + CSS + one tiny inline JS for the demo-strip dismiss.
- **Fonts:** Google Fonts via `<link>` (Bebas Neue + Cormorant Garamond + Inter).
- **Imagery:** 12 Unsplash photos by direct URL. All have stable Unsplash IDs.
- **Mobile responsive:** breakpoints at 1080px / 980px / 880px / 580px. Tested layouts at iPad Pro / iPhone Pro widths.
- **Accessibility:** Semantic HTML5 sections, `aria-label` on hero meta, alt text on all images via background-image sections (deferred — would add `<img>` versions in v2 for SEO + screen readers).
- **No analytics in v1.** Plausible script slot reserved if FH wants telemetry on the demo URL.

## Deploy options

**Option A — Netlify Drop (fastest):** Drag the `website-demo-v1` folder into [https://app.netlify.com/drop](https://app.netlify.com/drop). Live URL in ~10 seconds. Use this for the first prospect look.

**Option B — GitHub Pages:** Push to `andrei170.github.io/farang-homes-demo` or similar repo path. Persistent URL, free. Use this for outreach.

**Option C — Just open it:** Double-click `index.html`. Loads in browser instantly. Good for screen-share without deploying.

## Pitch context

Farang Homes is a real prospect with 300K IG and 16M YouTube views. Their current site is generic Wix-template grade. The build cost vs. brand-quality gap is the largest in our pipeline this week.

**Realistic deal sizing:**
- One-shot rebuild: $5K-$8K
- Rebuild + monthly content layer (we cut their existing YouTube into 4 short-form drops + monthly buying-guide chapter blog post): $3K + $750/mo retained
- Rebuild + SEO buildout (see SEO note below): $5K + $1K/mo for 6 months

## SEO buildout — soft yes

Thailand property keywords have real volume, especially:
- "buy property in Thailand as foreigner" (high intent, high volume)
- "Thailand condo for sale" + city qualifiers (transactional)
- "freehold vs leasehold Thailand" (informational, top-funnel)
- "Thailand property [city] [year]" (intent + freshness)

The opportunity for Farang Homes specifically: their existing audience does NOT drive the SEO. They're 100% IG/YT/TikTok-driven. A 12-month SEO content layer (monthly chapter expansions of the buying guide + city-by-city deep dives) could compound into a third lead source independent of the algorithm.

**Order of operations:** Rebuild first (this demo). SEO content layer second, after the eBook funnel is converting. Don't sell SEO until they're capturing email properly — otherwise the SEO traffic lands on a leaky funnel.

## What's NOT in this v1

- Real property database / live listings (out of scope — they're not an agency)
- Booking / payment flow for property feature service (gated behind a "brief us" form, sales-call closes the deal)
- Member login / saved walk-throughs (deferred to v2 if engagement justifies)
- True video embeds — current build uses placeholder photos with play-overlay. v2 swaps in actual YouTube embeds (`youtube.com/embed/{ID}`) with lazy-load.
- TikTok / Threads embed grids — could add in v2 as a "Latest from social" strip
- Full Thai language version (the audience is international buyers, English is correct for v1)

## Outreach script (draft, for Andrei)

> @faranghomes — built you a v1 of the site that matches what your channel actually feels like.
>
> Three things I tightened:
>
> Hero leads with the cinematic walk-through promise instead of a Vimeo embed.
>
> The buying guide is the email gate (currently it's buried in /shop-1).
>
> Eight cities each get their own walk-through library — the audience finally gets a property catalog without you having to be an agency.
>
> Sample: [deploy URL]
>
> - Andrei (AG1)

Hub URL convention if added to D100 build pipeline: `https://andrei170.github.io/farang-homes-hub/` (full Hunter-shape package) — this v1 is just the demo-rebuild track, no hub package built.
