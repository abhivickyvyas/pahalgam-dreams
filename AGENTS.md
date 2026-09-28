# Hotel Pahalgam Dreams — Project Knowledge

## What This Is
A single-page luxury hotel website for Hotel Pahalgam Dreams, a newly opened 28-room resort in Pahalgam, Kashmir. Built as a pure HTML/CSS/JS site with no build tools or frameworks.

## Business Details
- **Hotel name:** Hotel Pahalgam Dreams
- **Location:** Village Lidroo, Near Army School, Pahalgam – 192126, J&K, India
- **Coordinates:** 33.9707296, 75.3191647
- **Altitude:** 2,200 metres above sea level (Lidder Valley)
- **Distance from Srinagar:** 96 km
- **Phone:** +91 95552 60998
- **WhatsApp:** +919555260998
- **Email:** info@pahalgamdreams.com
- **Total rooms:** 28
- **Hours:** Open year-round, 24/7 front desk

## Room Categories
| Room Type | Beds | Capacity | Highlight |
|---|---|---|---|
| Family Suite | 4 beds | Up to 6 guests | Sitting area, most spacious |
| Super Deluxe | Double | 2–3 guests | Bathtub, peak view (honeymooners' choice) |
| Deluxe | Double | 2 guests | Private balcony, Himalayan view |
| Standard | Double | 2 guests | Walnut wood, free Wi-Fi |

## Hotel Services
- Airport & railway station transfers (Srinagar / Jammu)
- Guided treks to Betaab Valley, Aru & Baisaran
- Pony rides to Baisaran Meadows
- Amarnath Yatra facilitation & logistics
- In-house multi-cuisine restaurant (Kashmiri, Indian, Continental)
- 24/7 room service & front desk
- Complimentary high-speed Wi-Fi
- Safe private parking

## Nearby Attractions (with distances)
| Attraction | Distance |
|---|---|
| Baisaran Meadows ("Mini Switzerland") | 5 km |
| Aru Valley | 11 km |
| Betaab Valley | 14 km |
| Amarnath Yatra base camp | Pahalgam town |

## Project Structure
```
pahalgam-dreams/
├── index.html          ← Entire site: HTML + embedded CSS + embedded JS (single file)
├── README.md
├── AGENTS.md           ← This file (gitignored)
└── assets/
    └── images/
        ├── room-valley-view.jpeg    ← Deluxe room (balcony, mountain view)
        ├── room-standard.jpeg       ← Standard double room
        ├── room-suite-adobe.png     ← Super Deluxe (sunset Himalayan view) — used heavily
        ├── room-suite-wide.jpeg     ← Suite with heart towel art
        └── room-deluxe.jpeg         ← Family Suite (marble interiors, LED ceiling)
```

## Tech Stack
- **Language:** HTML5 + CSS3 + Vanilla JS only — no build tools, no npm, no frameworks
- **Fonts:** Cormorant Garamond (serif headings) + Jost (sans body) via Google Fonts CDN
- **Icons:** Font Awesome 6.5 via cdnjs CDN
- **Images:** All local JPEG/PNG files in assets/images/

## CSS Design Tokens (CSS variables in :root)
```css
--pine: #1A3D2B       /* primary dark green — headers, footer, testimonials bg */
--pine-mid: #2D5A3D   /* slightly lighter green */
--sage: #4A7C59       /* mid green — section tags, buttons, borders */
--sage-light: #6A9E77
--gold: #C9973A       /* accent gold — CTAs, icons, highlights */
--gold-light: #E0B86A /* lighter gold */
--cream: #F5F0E8      /* about section, gallery bg */
--meadow: #E8F2EC     /* services section bg */
--text: #1A2E1E
--serif: 'Cormorant Garamond'
--sans: 'Jost'
```

## Key Sections in index.html (with IDs)
| Section | ID / anchor | Notes |
|---|---|---|
| Hero slider | `#hero` | 3 slides, auto-advances every 5.5s |
| Booking bar | `#rooms` (also used as rooms anchor) | Sends inquiry via WhatsApp |
| Stats strip | — | Animated counters: 2200m, 28 rooms, 4 categories, 96km |
| About | `#about` | Grid layout, 4 feature cards |
| Rooms slider | within `#rooms` section | 4 cards, sliding carousel |
| Experience banner | — | Full-bleed image strip |
| Services | — | Two-column image + list layout |
| Gallery | `#gallery` | 5-item CSS grid with lightbox |
| Testimonials | `#testimonials` | 4 review cards, carousel |
| Attractions | `#attractions` | 4 nearby places grid |
| Newsletter | — | Email signup bar (no backend wired) |
| Footer | `#footer` | 4-column grid with embedded Google Map |

## Booking Flow
All bookings/enquiries go to WhatsApp (+919555260998). The booking bar collects check-in date, check-out date, room type, and guest count, then opens WhatsApp with a pre-filled message. No backend or booking engine is connected.

## JavaScript Features
- `sendWhatsApp()` — builds and opens WhatsApp URL from booking bar inputs
- Hero slider — `goSlide(n)`, auto-interval 5500ms, updates heading text dynamically
- Room & testimonial carousels — `slideRooms(dir)` / `slideTest(dir)`, responsive card width calculation
- Scroll reveal — IntersectionObserver on `.reveal` elements
- Counter animation — IntersectionObserver on `.stat-num[data-target]` elements
- Gallery lightbox — `openLb()`, `closeLb()`, `lbNav()`, keyboard arrow/escape support
- Header scroll state — adds `.scrolled` class after 60px scroll
- Date validation — check-in defaults to today, check-out to tomorrow, enforces logical ordering

## Responsive Breakpoints
- `≤1100px` — hamburger menu, stacked booking bar, single-column about/services
- `≤768px` — single-column rooms/testimonials, simplified gallery grid

## Deployment
Currently on Cloudflare Workers (branch `cloudflare/workers-autoconfig` exists in remotes). Can also deploy to Netlify, Vercel, Hostinger by uploading the folder.

## What's NOT Yet Done (from README)
- Real booking engine connection
- Separate CSS/JS files (currently all inline in index.html)
- Additional pages (rooms.html, contact.html, etc.)
- Google Analytics / GA4
- sitemap.xml, robots.txt
- More hotel photos (exterior, lobby, restaurant, bathroom)
