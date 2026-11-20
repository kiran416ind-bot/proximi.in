# Design Spec — Proximi India Marketing Site

**Reference:** https://coming-soon-93--6ditayqu.preview.emergentagent.com (Adda coming-soon)
**Aesthetic:** Warm editorial — off-white canvas, serif display (Fraunces), warm orange accent, India-friendly.
**Date:** 2026-11-20

## 1. Brand
- **Name:** Proximi India
- **Tagline:** "Your pre-launch marketing team, in a box."
- **Voice:** Helpful, energetic, India-context (festivals, Hinglish-friendly, WhatsApp-first).
- **Logo:** Wordmark "Proximi" (Fraunces 600) + "India" (Plus Jakarta Sans 500, muted) with a warm-orange rounded-square mark containing italic "P". See `logo.svg`.

## 2. Color tokens
| Token | Hex | Use |
|---|---|---|
| --bg | #FBF9F5 | Page background (warm off-white) |
| --surface | #FFFFFF | Cards, panels |
| --surface-2 | #F4F1EA | Subtle fills, mockups |
| --text | #1c1917 | Headings, body |
| --muted | #57534e | Secondary text |
| --subtle | #78716c | Tertiary text |
| --border | #e7e5e4 | Dividers |
| --accent | #ea580c | CTAs, links emphasis, italic display words |
| --accent-dark | #9a3412 | Hover |
| --accent-soft | #fff7ed | Icon tiles, highlights |
| --secondary | #4338ca | Text links |
| --success | #16a34a | Checkmarks |

## 3. Typography
- **Display:** Fraunces (serif), weights 300–800, italic for emphasis. Sizes: H1 clamp(40,7vw,76), H2 clamp(30,4.5vw,52), H3 clamp(22,3vw,34).
- **Body:** Plus Jakarta Sans, 300–700. Base 16px, line-height 1.6. Lede 19px.
- **Mono:** JetBrains Mono, 400/500. Eyebrows, prices, codes, tags.

## 4. Spacing & layout
- 8px grid. Section padding 96px (64px on mobile). Container max 1180px, gutter 24px.
- Radius: sm 8, md 14, lg 22, pill 999.
- Shadows: sm (1px), md (8px), lg (24px) — warm, low-opacity.

## 5. Components
- **Nav:** sticky, blurred warm bg, logo + links + dual CTA (Login, Join waitlist).
- **Button:** pill, primary (orange, shadow), ghost (border), sm/lg variants.
- **Card:** white surface, 1px border, 14px radius, hover lift.
- **Feature card:** icon tile (accent-soft) + title + desc.
- **Hero:** 2-col (copy + visual mockup), big serif headline with italic accent word, email capture pill, social proof line.
- **Pricing card:** featured variant with "Most popular" badge, price in Fraunces, feature list with checkmarks.
- **Blog card:** 16:9 thumb + tag + title + excerpt + meta.
- **Auth card:** centered 420px card, social sign-in buttons.
- **Footer:** dark (text color), 4-col grid + bottom bar.

## 6. Page structure
| Page | Key sections |
|---|---|
| Home | Nav, Hero, Features (6), How it works (3 steps), Social proof, Pricing teaser, Final CTA, Footer |
| Pricing | Nav, Hero (small), 4-tier pricing grid, Comparison table, FAQ, Footer |
| About | Nav, Hero, Story, Mission/Values, Team, CTA, Footer |
| Blog | Nav, Hero, Featured post, 3-col post grid, Newsletter signup, Footer |
| Contact/Demo | Nav, Hero, Contact form + info, Map-ish block, Footer |
| Login/Signup | Centered auth card, social sign-in, email form, toggle |

## 7. Responsive
- Breakpoints: 900px (grid collapse), 760px (nav collapse), 600px (pricing single col).
- Mobile-first stacking; hero visual below copy on small screens.

## 8. Prototype files
- `styles.css` — shared design system (this spec's tokens).
- `index.html`, `pricing.html`, `about.html`, `blog.html`, `contact.html`, `login.html`.
- `logo.svg`.

## 9. Notes for implementation
- All pages share nav/footer via duplicated markup (static site; no build step).
- Forms are UI-only in prototype; wire to backend later.
- Use placeholder copy where final copy TBD; mark with `[TBD]`.
- Images: use CSS gradients/placeholders until real assets exist.
