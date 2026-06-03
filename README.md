# PSI Pressure Wash Co. — Website

A fast, modern, single-file site for **PSI Pressure Wash Co.** (Ennis, TX).
Open `index.html` in any browser. No build step, no server needed.

---

## 1. Add your real info (2 minutes)

Open `index.html`, scroll to the **`CONFIG`** block near the bottom (inside `<script>`),
and fill in the real details. Everything on the page reads from here:

| Field | What to put |
|-------|-------------|
| `phoneDisplay` / `phoneDial` | Your real phone number (the dial version is digits only, e.g. `+19725551234`) |
| `email` | Your business email |
| `facebookUrl` | Your Facebook page URL (already set) |
| `hours` | Your business hours |
| `areas` | Towns you actually serve |
| `gallery` | Captions + image filenames for your photos |
| `reviews` | **Real** reviews copied from your Facebook page |
| `beforeImg` / `afterImg` | A real before & after photo for the slider |

> ⚠️ The phone number, reviews, and price-related text are placeholders.
> Replace them before going live — don't publish the sample text.

---

## 2. Add your photos

Put image files in the **`images/`** folder, then reference the filenames in `CONFIG`.

- **Logo:** save as `images/logo.png` (transparent PNG works best). It auto-appears,
  replacing the built-in logo mark. Big and recognizable, as requested.
- **Gallery:** `images/work-1.jpg` … `work-6.jpg` (or any names — just match `CONFIG.gallery`).
- **Before/After slider:** set `beforeImg` and `afterImg` to real photos of the same spot.

Any missing image shows a tidy branded "Add photo" tile, so the site never looks broken.

---

## 3. How to get your photos OFF Facebook

Facebook blocks automated downloads, so grab them manually — it's quick:

**Logo / profile picture**
1. Open your page, click the profile picture → **View profile picture**.
2. Click the **⋯ menu → Download**, or right-click → **Save image as…**
3. Save it as `images/logo.png`.

**Cover photo & posted job photos**
1. Click any photo to open it full-size.
2. Right-click → **Save image as…** (or the **⋯ → Download** option).
3. Save into `images/` and add the filename to `CONFIG.gallery`.

**Get the biggest version** (sharper on screens): when a photo is open, the URL or the
Download option gives the full-resolution file — prefer that over a screenshot.

**Reviews:** Facebook reviews can't be downloaded — just **copy the text** from your
Reviews tab and paste it into the `reviews` list in `CONFIG`, with the reviewer's first
name and town.

> Use only photos you own / took for your business — that's everything on your own page.

---

## 4. Make the quote form actually send (optional)

By default the form shows a thank-you message and logs the request to the browser console.
To receive submissions by email with zero backend:

1. Make a free form at **formspree.io** (or Web3Forms / Getform).
2. In `index.html` find `const ACTION = "";` and paste your form URL between the quotes.

That's it — submissions land in your inbox.

---

## 5. Put it online

Drag-and-drop hosting that works with this single file + `images/` folder:

- **Netlify Drop** — drag the `psi_pro` folder onto app.netlify.com/drop → instant live URL.
- **Cloudflare Pages** / **GitHub Pages** — also free, great for a custom domain.
- Or any web host: upload `index.html` and the `images/` folder.

Point your domain at it and you're live.

---

### Files
- **`index.html`** — the current site. **Brand colors pulled straight from the logo**
  (navy + green + steel blue), top-nav layout, image-driven full-bleed hero.
  Four sections: Hero · Services · Results · Free Quote. **This is the one to use.**
- `index-light.html` — earlier light / left-sidebar version (reference).
- `index-dark.html` — earlier dark / industrial version (reference).

### Real assets already wired in
- `logo1.jpg` — your circular badge logo (clipped to a clean circle; shown large in the
  header & footer, and used as the favicon).
- `image1.jpg` — your truck + rig, used as the full-bleed **hero background**.
- `image2.jpg` — your driveway **before/after**, featured in the Results section.

> To swap any photo, just replace the file (keep the name) or edit the `src` in `index.html`.
> Add more before/afters and we can turn Results into a scrolling gallery again.

### What's already built in (current branded version)
- Large, recognizable circular logo (header + footer), brand-accurate palette
- Image-driven hero with staggered headline reveal + green swoosh divider (logo callback)
- Navy trust strip, services grid, real before/after showcase
- Navy contact section with quote form + click-to-call everywhere
- Sticky mobile call bar, responsive, accessible, respects "reduce motion", no dependencies
