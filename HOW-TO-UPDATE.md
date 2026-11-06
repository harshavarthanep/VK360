# VK360 website: how to update

Everything you will ever need to change lives in ONE place: the `window.SITE = { ... }`
block near the top of `index.html` (right after the `<head>` links). You never need to
touch the design code below it.

## Edit on GitHub (no software needed)
1. Open your repository on github.com and click `index.html`.
2. Click the pencil icon (Edit this file).
3. Change the text inside `window.SITE`, then click **Commit changes**.
4. The live site updates in about 1–2 minutes.

## Before going live (fill these in)
- `contact.address`: centre address. The Google Map and "Get directions" appear automatically.
- `contact.mapsLink`: optional, paste the Google Maps share link of the centre for an exact pin.
- `social.instagram`, `social.facebook`, `social.youtube`: full profile links.
- `contact.hours`: e.g. `{ days: "Monday to Saturday", time: "5:30 AM – 9:00 PM" }`
- `events` and `updates`: the current entries are SAMPLES. Replace them with real ones.

## Add an event or workshop
Copy one block inside `events: [ ... ]`, paste it, and change the values.
- Dates: `"YYYY-MM-DD"`, times in 24-hour `"HH:MM"`.
- Multi-day workshop: add `endDate`. It shows "Happening now" while it runs.
- Past events hide themselves automatically.
- Register button opens WhatsApp with the event name pre-filled
  (or set `link` to use a Google Form instead).

## Change Coach Vimal's photo
The photo is `media/coach-vimal.jpg` (hero circle + About section) and
`media/coach-vimal-avatar.jpg` (small round photo in the chat and contact card).
Upload a new file with the same name to replace it. A square photo of at least
1200 × 1200 px with the face in the upper half looks sharpest.

## Add photos and videos
1. On GitHub, open the `media` folder, click **Add file → Upload files**.
2. Use the path in `index.html`, for example:
   - Coach photo: `coachPhoto: "media/coach-vimal.jpg"`
   - Video (YouTube): `{ title: "Morning routine", youtube: "https://youtu.be/XXXX" }`
   - Video (own file): `{ title: "Healthy plate", file: "media/plate.mp4", poster: "media/plate.jpg" }`
   - Post: `{ image: "media/post-1.jpg", caption: "Hydration tip", date: "2026-11-10", link: "" }`
Sections for videos, posts and client stories stay hidden until you add something.

Tips: keep photos under 500 KB (compress at squoosh.app). GitHub allows files up to
100 MB, but YouTube is better for long videos.

## Rules that keep the file working
- Keep the quotes "..." and the commas between entries.
- Text sits inside "double quotes", so apostrophes like I'd are fine. Never type a plain " inside the text.
- If the page goes blank after an edit, a comma or quote is missing. Undo via the file's History on GitHub.

## Share preview (WhatsApp / Facebook link card)
The share image URL in `<head>` assumes the site lives at
`https://harshavarthanep.github.io/VK360/`. If your repository has a different name,
replace `VK360` in the 3 lines with `og:url`, `og:image` and `canonical`,
and in `404.html`, `robots.txt` and `sitemap.xml`.
