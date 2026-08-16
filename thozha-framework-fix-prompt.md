# Prompt: Fix Broken Images + Rename to THOZHA FRAMEWORK

Copy-paste this into your AI coding tool (the same one used to build the site).

---

I built this website in HTML/CSS/JavaScript and deployed it to Vercel. All images are currently returning 404 (broken images) on the live site.

**TASK 1 — Fix broken images (root cause, not just paths)**

The images are referenced correctly as `/images/filename.png` (this is the right format for a `public/images/` folder on Vercel), but they return 404 on the deployed site. This means the images most likely never made it into the GitHub repo / build output. Do the following:

1. List every file actually present inside the `public/images/` (or equivalent) folder in the project right now.
2. Compare that list against every image reference in HTML, CSS (`background-image: url()`), and JavaScript (`.src =`, `data-src=`) across the whole project.
3. For every reference with no matching file: tell me the exact missing filename — do NOT replace it with a random/stock/Unsplash image.
4. For every file that exists but doesn't match due to case sensitivity or extension mismatch (e.g. `LED-Lamp.jpg` vs `led-lamp.jpg`), fix the HTML/CSS/JS reference to exactly match the real filename.
5. Confirm the images folder is actually committed to git (not in `.gitignore`) and included in the Vercel build/output — this is the most likely reason for the 404s.
6. Do not use `/public/images/...` — Vercel serves the `public` folder at root, so it must be `/images/...`.

**TASK 2 — Business name correction**

Replace every instance of the business name with exactly: **THOZHA FRAMEWORK**

Do NOT use: Thonza Frame Work / Thozha Frame Work / Thozha Frameworks — check header, nav, hero, footer, page title, meta tags, alt text, and copyright line.

**DO NOT CHANGE:**
Layout, colours, fonts, animations, sections, product list, buttons, WhatsApp links, contact info, or any other content/design.

**FINAL OUTPUT — give me only:**
- Root cause of the broken images
- Files changed
- List of images fixed
- Any images that are genuinely missing (with exact filename)
- Confirmation the project is Vercel-ready after redeploy
