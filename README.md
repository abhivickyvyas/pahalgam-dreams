# Hotel Pahalgam Dreams — Website

**Location:** Village Lidroo, Near Army School, Pahalgam – 192126, Jammu & Kashmir, India  
**Coordinates:** 33.9707296, 75.3191647  
**Capacity:** 28 Rooms  

---

## Room Categories

| Category        | Beds       | Key Feature         |
|----------------|------------|---------------------|
| Family Suite    | 4 Beds     | Spacious, family     |
| Super Deluxe    | Double     | Bathtub, marble      |
| Deluxe          | Double     | Private balcony      |
| Standard        | Double     | Cosy, walnut wood    |

---

## Folder Structure

```
pahalgam-dreams/
├── index.html                  ← Main homepage (single file, self-contained)
├── README.md                   ← This file
├── assets/
│   ├── images/
│   │   ├── room-valley-view.jpeg   ← Deluxe room with balcony & mountain view
│   │   ├── room-suite-wide.jpeg    ← Suite front view with heart towel art
│   │   ├── room-deluxe.jpeg        ← Super Deluxe with LED ceiling & teal accents
│   │   ├── room-suite-adobe.png    ← Premium shot with sunset Himalayan view
│   │   └── room-standard.jpeg      ← Standard double room
│   ├── css/                        ← (future: extract styles from index.html)
│   └── js/                         ← (future: extract scripts from index.html)
```

---

## How to Use

1. **Open directly:** Double-click `index.html` in any browser.
2. **Deploy:** Upload entire `pahalgam-dreams/` folder to any web hosting (Hostinger, Netlify, Vercel, etc.)
3. **Images:** All images are local — no internet required to display them.

---

## Recommended Next Steps

- **Add more photos:** Replace placeholder images as you get more hotel photos (exterior, restaurant, lobby, bathroom, etc.)
- **Separate CSS/JS:** Extract the `<style>` and `<script>` blocks into `assets/css/main.css` and `assets/js/main.js` for maintainability.
- **Create additional pages:** `rooms.html`, `contact.html`, `booking.html`, `gallery.html`, `about.html`
- **Connect booking engine:** Replace the "Check Availability" button with a link to your booking system (e.g., Booking.com widget, Goibibo integration)
- **Add Google Analytics:** Insert GA4 tracking code for visitor analytics.
- **SEO:** Add a `sitemap.xml`, `robots.txt`, and proper `<link rel="canonical">` tags.
- **WhatsApp button:** Add a floating WhatsApp chat button linked to your number.

---

## Tech Stack

- **HTML5 + CSS3 + Vanilla JS** (no build tools needed)
- **Fonts:** Cormorant Garamond (serif) + Jost (sans) via Google Fonts
- **Icons:** Font Awesome 6.5
- **Images:** Local JPEG/PNG (your actual hotel photos)

---

## Color Palette (derived from hotel interiors)

| Swatch | Variable       | Hex       | Inspired by            |
|--------|----------------|-----------|------------------------|
| 🟠      | `--gold`       | `#C9973A` | Brass light fittings   |
| 🟡      | `--gold-light` | `#E0B86A` | Warm lamp glow         |
| 🔴      | `--crimson`    | `#8B2635` | Velvet headboards      |
| 🟤      | `--dark`       | `#1C1008` | Walnut wood ceiling    |
| ⬜      | `--cream`      | `#F7F2EB` | Marble walls           |
