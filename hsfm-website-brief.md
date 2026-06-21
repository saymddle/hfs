# Holy Spirit Fire Ministries — Website Brief

**Project:** Church website for Holy Spirit Fire Ministries International
**Type:** Multi-page HTML site (11 pages, shared design system)
**Style direction:** Squarespace-style editorial template — light, image-forward layout with full-bleed color blocks, generous whitespace, and a fine-art serif/sans pairing
**Folder:** `hsfm-website/` — all pages are plain HTML files that link to one another by relative filename, so the folder can be opened locally, zipped, or uploaded to any static host as-is

---

## 1. Organization Information

| Field | Detail |
|---|---|
| Name | Holy Spirit Fire Ministries (International) |
| Denomination | Pentecostal Church |
| Mission | A Pentecostal Church with a vision to save souls for the Kingdom of God |
| Address | 2730 Mountain Industrial Blvd, Ste 110, Tucker, GA 30084 |
| Website | holyspiritfireministries.org |

---

## 2. Service Schedule

| Service | Day | Time | Notes |
|---|---|---|---|
| Worship Service | Sunday | 9:00 AM | Morning worship |
| Bible Study & Prayer | Wednesday | 7:00 PM | Mid-week teaching |
| Prayer Service | Friday | 10:00 PM – 1:00 AM | Late-night prayer |

These three service times appear in three places across the site, and must stay in sync if changed:
1. **Times bar** (`index.html`, directly under the hero) — quick-glance cards with day, time, and a short label
2. **Reach Us page** (`reach-us.html`) — "Service Times" info block
3. **Footer** (every page) — "Services" link column

---

## 3. Site Map & Navigation

The site is now multi-page. The fixed nav bar appears identically on every page, with the current page highlighted (bold, darker blue):

| Nav Label | File | Purpose |
|---|---|---|
| *(logo)* | `index.html` | Home |
| About | `about.html` | Full church story, beliefs, stats |
| Ministries | `ministries.html` | Hub linking to all 5 ministry pages |
| Request | `request.html` | Prayer request form |
| Reach Us | `reach-us.html` | Address, service times, contact form |
| Give *(red pill button)* | `give.html` | Giving methods page |

Ministry detail pages are not in the main nav (to avoid crowding it) but are reachable from the Ministries hub, the homepage ministry cards, and a sticky sub-nav that appears at the top of every ministry page:

| File | Ministry |
|---|---|
| `ministry-youth.html` | Youth Ministry |
| `ministry-women.html` | Women's Ministry |
| `ministry-men.html` | Men's Ministry |
| `ministry-evangelism.html` | Evangelism & Outreach |
| `ministry-bible-study.html` | Bible Study |

---

## 4. Color Palette

The palette is intentionally light and warm — no black anywhere on the site. Four core hues, each carrying a specific role, used consistently across all 11 pages:

| Token | Hex | Role |
|---|---|---|
| `--cream` | `#F7F2E8` | Primary page background |
| `--cream-dark` | `#EDE5D4` | Section background variant (alternating blocks) |
| `--cream-mid` | `#F0EAD8` | Card hover state |
| `--blue` | `#3B6B8A` | Primary accent — buttons, links |
| `--blue-light` | `#5A8BA8` | Secondary blue accent |
| `--blue-pale` | `#D4E4EE` | Light blue backgrounds (About panel) |
| `--blue-deep` | `#264D65` | Hero/page-hero background, footer background, primary headings |
| `--green` | `#2F5F45` | Times bar background, Ministries heading, one Pillar card |
| `--green-light` | `#4A8060` | Green hover state |
| `--green-pale` | `#D4E8DC` | Reserved light green (unused, available for future cards) |
| `--red` | `#8B2A2A` | Give CTA blocks, Give page hero, one Pillar card, nav "Give" button |
| `--red-light` | `#B03C3C` | Red hover state |
| `--red-pale` | `#EDD8D8` | Reserved light red (unused) |
| `--text` | `#2A2A2A` | Body copy on cream backgrounds |
| `--text-mid` | `#555` | Secondary body copy |
| `--text-muted` | `#888` | Labels, eyebrows, captions |
| `--border` | `rgba(42,42,42,0.12)` | Hairline dividers throughout |

**Where each color shows up:**
- **Blue (deep):** Hero/page-hero banners on every page, footer, primary section headings
- **Green:** Times bar strip, Ministries section/page headings, one Pillar card
- **Red:** "Give to the Kingdom" CTA blocks, the entire Give page hero, "Give" nav button, one Pillar card
- **Cream:** Everything else — the resting state of every page

---

## 5. Typography

| Use | Font | Weight |
|---|---|---|
| Headlines, hero text, page titles, section titles | Cormorant Garamond (serif) | 500–700, italic for emphasis words |
| Body copy, labels, nav, buttons | Jost (sans-serif) | 400–600 |

Both load from Google Fonts on every page. Nothing should be set below weight 500 on Cormorant Garamond or weight 400 on Jost — this was a deliberate revision to give the type more visual weight and presence.

---

## 6. Shared Design Elements (every page)

These elements are identical across all 11 pages, generated from one shared CSS block so visual consistency is guaranteed:

- **Fixed nav bar** — frosted cream background, blurs on scroll, current page bolded
- **Page hero banner** — every sub-page (About, Ministries, ministry detail pages, Request, Reach Us, Give) opens with a deep blue (or red, for Give) banner: an eyebrow label, a large serif page title, and a one-line subtitle
- **Grain overlay** — subtle SVG fractal-noise texture (3–8% opacity, multiply blend) on every major section, giving a tactile, printed-paper feel rather than a flat digital look
- **Scroll reveal** — content blocks fade/slide in via `IntersectionObserver` as the user scrolls, on every page
- **Footer** — deep blue, three columns (brand/tagline, Navigate links, Services links), identical on every page including all 5 ministry detail pages
- **CTA band** — most pages end in a full-bleed colored band (red or blue-deep) with a headline and a single directional button, nudging the visitor to the next logical action (Reach Us, Give, etc.)

---

## 7. Page-by-Page Breakdown

### `index.html` — Home
- Hero: two-column split, deep blue left panel with the "Holy Spirit Fire Ministries" headline (image-based text assets) + two buttons ("Plan Your Visit" → Reach Us, "Our Story" → About); right panel holds the dove emblem artwork
- Times bar: Sunday 9 AM, Wednesday 7 PM, Friday 10PM–1AM, Find Us (Tucker, GA)
- About preview: mission statement, stats row (25+ Years, Int'l Reach, One Body), link to full About page
- Pillars: Worship / Word / Community, three full-color cards
- **Ministries section — now clickable cards.** Each of the 5 ministry cards is a real link (`<a>` tag, not just a styled `<div>`) to its own ministry page, with a "See Updates →" arrow that appears on hover. A 6th card, "View All Ministries," links to the Ministries hub
- Give CTA band linking to the full Give page

### `about.html` — About
- Page hero: "About Our Church"
- Expanded mission/story copy (two paragraphs instead of one), same stats row
- Same Pillars section as homepage (Worship / Word / Community)
- Closing CTA → Reach Us

### `ministries.html` — Ministries Hub
- Page hero: "Ministries & Programs"
- All 5 ministry cards in a grid (same clickable card design as the homepage, minus the "View All" 6th card since you're already here)
- Closing CTA → Reach Us

### Ministry Detail Pages (shared template, 5 pages)
Each ministry page uses **one shared layout**, just swapping the name, tagline, and event content:
- Page hero with the ministry's name and a one-line description
- **Sticky sub-navigation** — a pill-style row letting visitors jump directly between all 5 ministries without returning to the hub
- **Events feed** — this is the core of each page. Events render as flyer-style cards: a date block (day + month) on the left, and on the right the event title, a meta row (🕒 time, 📍 place), and a description
  - **`ministry-women.html`** currently has one real event: **Women's Ministry Tea Party**, Sept 14, 2:00 PM–4:00 PM, Fellowship Hall, with a description inviting all women of the church and community
  - **`ministry-youth.html`, `ministry-men.html`, `ministry-evangelism.html`, `ministry-bible-study.html`** currently show an empty state: *"No Upcoming Events — Check back soon — new events and updates for this ministry will be posted here."*
- Closing CTA → Reach Us

**To add a new event:** open the relevant ministry page's HTML, find the `event-card` block (or the `empty-state` block if there isn't one yet), and copy the Women's Ministry tea party card as a template — replace day, month, title, time, place, and description.

### `request.html` — Prayer Request
- Page hero: "Prayer Request"
- Left column: a James 5:16 scripture callout + a short note on what happens after submitting
- Right column: form collecting **First Name, Last Name, Email or Phone Number, and the prayer request text** (per your instruction — kept minimal, no privacy-choice toggle)
- A confidentiality note appears above the submit button
- Closing CTA → Reach Us (for anyone who wants to talk to someone directly)

### `reach-us.html` — Reach Us *(renamed from "Contact")*
- Page hero: "Reach Us"
- Left column: Service Times, full street address, website link
- Right column: general contact form (First/Last Name, Email, Subject, Message)
- No closing CTA band (this is already the "end of the funnel" page)

### `give.html` — Give
- Page hero in **red** (the only page hero that isn't blue), "Give to the Kingdom"
- Three giving methods, each in its own card: **Give Online** (links out to holyspiritfireministries.org), **Give In Person** (links to Reach Us for service times), **Give By Mail** (shows the church's mailing address inline)
- A 2 Corinthians 9:7 scripture callout in a soft blue panel at the bottom

---

## 8. Forms — Current Status

| Form | Page | Fields | Backend? |
|---|---|---|---|
| Prayer Request | `request.html` | First Name, Last Name, Email/Phone, Request text | No — `onsubmit="return false;"` |
| General Contact | `reach-us.html` | First/Last Name, Email, Subject, Message | No — `onsubmit="return false;"` |

Both forms are fully styled and functional in the browser (validation, focus states, etc.) but do not currently send anywhere. They'll need a form-handling service (e.g., Formspree, Netlify Forms) or a custom backend before going live.

---

## 9. Known Gaps / Open Items

- Neither form (Prayer Request or Reach Us) is wired to a backend yet — submissions currently go nowhere
- The dove emblem on the homepage is the uploaded artwork file (background removed via CSS blend mode), not a vector recreation
- 4 of the 5 ministry pages are currently showing the empty state since only the Women's Ministry tea party has been added as a real event
- No dedicated sermons archive, events calendar view (all events live on their respective ministry pages only), or embedded online giving portal — Give Online currently links out to the main church website

---

## 10. Recent Change Log

1. Initial build: bold block-style hero with dark/charcoal palette
2. Revised to Squarespace-style editorial layout, removed black, introduced blue/cream/green/red palette
3. Increased font weights across all headings and body copy for stronger visual presence
4. Replaced placeholder hero headline graphics with uploaded "HOLY / SPIRIT / FIRE / MINISTRIES" text-image assets
5. Replaced SVG emblem placeholder with uploaded dove artwork (black background removed via blend mode)
6. Corrected service times (9 AM Sunday, removed evening service), corrected location (Augusta → Tucker), removed Matthew 19:26 scripture block, removed Prayer & Intercession ministries card
7. Added full street address (2730 Mountain Industrial Blvd, Ste 110, Tucker, GA 30084) to Contact section
8. Added Friday Prayer Service (10:00 PM–1:00 AM) to times bar, Contact section, and footer
9. **Converted the site from one single-page HTML file into a full 11-page multi-page site:** Home, About, Ministries (hub), 5 individual ministry pages, Prayer Request, Reach Us (renamed from Contact), and Give — all sharing one consistent design system, nav bar, and footer
10. Turned the homepage's ministry cards into real clickable links to each ministry's own page
11. Built a shared events-feed template for ministry pages, with flyer-style event cards (date, time, place, description) and an empty-state for ministries with nothing scheduled yet
12. Added the Women's Ministry Tea Party as the first real event (Sept 14, 2:00–4:00 PM, Fellowship Hall)
13. Packaged all 11 pages into a single folder (`hsfm-website/`) for easy transfer or upload
