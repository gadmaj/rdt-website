# RDT Redesign — Design Direction (single source of truth) — REV 3

## REV 3 pivot (user directives)
ONE-PAGER. The whole site is `index.html`. Secondary pages die; their content
folds into sections after the 3D stage. Four model parts, one coherent
explosion, camera-tour focus, no transparency ghosting, anonymized people,
no photos of people, hidden scrollbars, sponsor ticker, perf instrumentation.

## The experience (index.html top to bottom)
1. STAGE (sticky scrub track, shortened ~600svh):
   a. Intro — assembled rover, title.
   b. THE EXPLOSION — on first scroll segment ALL four parts separate at once
      into one readable exploded view (this is the animation the user likes —
      keep its feel; fix the broken translations). Directions per manifest:
      locomotion stays anchored (the base), excavation lifts up-forward,
      deposition up-rear, EE box straight up. One radial gesture, no
      random angles.
   c. CAMERA TOUR — one segment per part (Locomotion, Excavation, Deposition,
      EE Box): parts STAY separated and FULLY OPAQUE; the camera translates
      smoothly (dolly/track, minimal orbit change — no angular swinging)
      to frame each part; its callouts + team panel come up.
   d. Reassembly + Mission Operations closing.
2. TEAM section — anonymized register (see People below).
3. PROJECTS section — compact robot spec tables (AMIGO/ASTRO/PIPER), no slideshows.
4. NEWS section — the featured article + short archive list.
5. SPONSORS — a scrolling ticker/marquee text box (continuous horizontal
   scroll, pausable on hover/focus, static list under prefers-reduced-motion).
6. Footer (unchanged chrome).
In-page nav: header links become anchor links (#team, #projects, #news,
#sponsors) plus HOME → top.

## People (privacy scrub — user directive)
- NO member photos, NO group/team photos anywhere. Remove headshot files and
  team-photo usage from the page.
- ALL names become placeholders cycling: John Doe, Jane Doe, Johnny Appleseed
  (+ Joanie Appleseed if a 4th variant helps). Positions/majors/competencies stay.
- NO personal links (LinkedIn/GitHub/Instagram/personal sites) — they identify
  real people. Strip them from data and UI.
- Avatar: the line-art person icon (resources/brand/placeholder-avatar.png),
  recreated as inline SVG (circle head + shoulder arc, currentColor stroke) —
  one shared symbol, used at small sizes wherever a person renders.
- lead_info.json: keep the file SHAPE (competency/position/major arrays) but
  replace name fields with the placeholder cycle and null all personal links.

## Model / motion contract
- FOUR groups from models/subsystems.json: sys_locomotion (anchor),
  sys_excavation, sys_deposition, sys_ee_box. Iterate generically.
- Explosion state is a single scalar E (0→1): group.position =
  explodeDir · E · scale. Camera tour happens at E=1. Reassembly eases E→0.
- All parts opaque at all times. Active part may keep the violet emissive tint;
  inactive parts stay fully rendered (no opacity drops).
- Perf (user reports lag): target ≤12MB / ≤60 draw calls / ≤900k tris model;
  page caps DPR at 1.5, drops to 1 when frame time >24ms sustained (log the
  switch); ?perf=1 shows a tiny mono HUD (ms/frame, draw calls, DPR, tris).
- Hidden scrollbars everywhere (html: scrollbar-width:none;
  ::-webkit-scrollbar{display:none}) — page still scrolls normally.

## Tokens
Palette (harmonize across merged sections — "fit better"):
- `--paper: #FFFFFF`, `--ink: #0A0A0A`, `--ink-60: #5A5A5A`,
  `--hairline: #DEDEDE`, `--band: #050505`, `--violet: #57068C`.
- Violet stays functional-only (links, focus, active part tint, ticker
  accent). Sections may alternate paper / very-faint gray (#FAFAFA) panels to
  give the one-pager rhythm — nothing darker than that outside the bands.
Type: unchanged — Atkinson Hyperlegible Next variable (200-500, nothing
bolder), Atkinson Hyperlegible Mono for labels. Self-hosted.

## Accessibility floor (carried + additions)
- Ticker: pausable, reduced-motion → static wrap list; never the only path to
  sponsor names.
- Hidden scrollbars don't remove keyboard/wheel scroll; phase rail remains the
  in-page navigation route.
- Body ≥16px, lh ≥1.5; focus rings violet on paper / white in bands.
- prefers-reduced-motion: explosion/tour become stepped states.
