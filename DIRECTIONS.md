# Current redesign

Run `python3 -m http.server 8000` from the repository.

- `http://localhost:8000/` — the new photography-led purple-and-white homepage.
- `http://localhost:8000/news.html` — the four original news/publication references.

The primary navigation is Team, Previous Years, Contact. Sponsorship appears inside Contact; news is linked from the footer. The robot is introduced through a supplied CAD image, a short description, and a Watch Luna in action video link. At the user's request the subsystem dropdowns were removed; Luna media is unlinked and non-draggable. The homepage restores the earlier muted 15-second testing video with a still fallback and no on-page playback control, as requested. No 3D model, scroll animation, or design-variant code loads on either page.

Current presentation: `styles/redesign.css`. Navigation and legacy-link handling: `scripts/site/redesign.js`. The roster continues to use `scripts/site/sections.js` and the unchanged `scripts/lead_info.json` data. Prior rendering modules and styles remain in the repository, unused by the new pages.

## Photography

Selected derivatives are in `resources/redesign/`, with source records alongside them. The originals in Downloads and on the camera card were not changed. The hero reuses `resources/media/luna-showcase-loop.mp4` (15 seconds, approximately 2.2 MB) and its original `luna-showcase-poster.jpg`; the prior April 12 testing photograph remains available in `resources/redesign/`. Team photograph: camera-card image IMG_4558, April 26, 2026. The CAD render and logo were supplied in the Downloads asset folder.

Existing historical images retain their pixels and now carry source comments. The new WebP assets total approximately 600 KB; historical imagery is lazy-loaded.

## Verification

Chromium checks at desktop (1440px) and phone (390px): 17 roster entries, six robot seasons, four publication links, all images loading, no horizontal overflow, no runtime errors or missing resources, mobile navigation/Escape, and contact form validation. Navigation and imagery also work without JavaScript. The contact form was not submitted; its existing external destination remains unchanged.
