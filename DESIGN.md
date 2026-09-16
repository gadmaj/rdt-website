---
name: NYU Robotic Design Team
description: A simple purple-and-white student engineering website grounded in real team and robot imagery.
colors:
  purple: "#57068c"
  purple-dark: "#3d0960"
  ink: "#24202a"
  muted: "#625c68"
  paper: "#fff"
  soft: "#f6f4f8"
  line: "#ded9e3"
  field-border: "#c7c0cd"
  purple-wash: "#eee5f4"
typography:
  display:
    fontFamily: "Atkinson, sans-serif"
    fontSize: "clamp(44px, 5.3vw, 80px)"
    fontWeight: 500
    lineHeight: 1.12
    letterSpacing: "-.035em"
  headline:
    fontFamily: "Atkinson, sans-serif"
    fontSize: "clamp(34px, 3.7vw, 52px)"
    fontWeight: 500
    lineHeight: 1.12
    letterSpacing: "-.03em"
  title:
    fontFamily: "Atkinson, sans-serif"
    fontSize: "25px"
    fontWeight: 500
    lineHeight: 1.12
    letterSpacing: "-.02em"
  body:
    fontFamily: "Atkinson, sans-serif"
    fontSize: "17px"
    fontWeight: 350
    lineHeight: 1.6
  label:
    fontFamily: "Atkinson, sans-serif"
    fontSize: "15px"
    fontWeight: 400
    lineHeight: 1.6
  caption:
    fontFamily: "Atkinson, sans-serif"
    fontSize: "14px"
    fontWeight: 350
    lineHeight: 1.6
rounded:
  control: "3px"
  portrait: "50%"
spacing:
  caption: "12px"
  field-gap: "20px"
  group: "32px"
  section: "clamp(64px, 7vw, 108px)"
  page-inline: "clamp(22px, 5vw, 80px)"
components:
  button-primary:
    backgroundColor: "{colors.purple}"
    textColor: "{colors.paper}"
    rounded: "{rounded.control}"
    padding: "13px 22px"
  button-primary-hover:
    backgroundColor: "{colors.purple-dark}"
  button-light:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.purple}"
    rounded: "{rounded.control}"
    padding: "13px 22px"
  button-light-hover:
    backgroundColor: "{colors.purple-wash}"
  text-field:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.ink}"
    rounded: "{rounded.control}"
    padding: "11px 13px"
    width: "100%"
  navigation-link:
    textColor: "{colors.ink}"
    padding: "12px 0"
  navigation-link-current:
    textColor: "{colors.purple}"
  text-link:
    textColor: "{colors.purple}"
    padding: "10px 0"
  project-record:
    textColor: "{colors.ink}"
    padding: "10px 0"
  news-link:
    textColor: "{colors.ink}"
    padding: "28px 0"
---

# Design System: NYU Robotic Design Team

## Overview

**Creative North Star: "Real engineering, real people"**

An approachable student engineering website whose identity comes from NYU purple, its robot, and its people. Naturally colored photography and the supplied assembled CAD rendering establish the subject; readable type and spacious groups make the team's work easy to browse.

This records the implemented system in `styles/redesign.css`, `index.html`, and `news.html`, following the user's authorized replacement of the former drawing-sheet and exploded-model direction. The chosen conventional student-team presentation takes priority over the workshop's generated form assignment. Surface sequence and reference-site research remain in the surface brief and `REDESIGN-RESEARCH.md`.

**Key Characteristics:**

- NYU purple, white, and quiet neutral surfaces.
- Real robot and team imagery with readable captions.
- One self-hosted sans-serif family and a clear type hierarchy.
- Flat sections, fine dividers, and ordinary scrolling.
- Direct, visible navigation and a simple robot introduction.

## Colors

Purple carries the university identity, while warm gray text and lightly tinted backgrounds support photographs without recoloring them.

### Primary

- **NYU Purple** (`purple`): hero ground, primary buttons, links, selected navigation, project names, and selected section headings.
- **Deep Purple** (`purple-dark`): footer ground and primary-button hover.
- **Purple Wash** (`purple-wash`): the light-button hover surface.

### Neutral

- **White Paper** (`paper`): main page, masthead, fields, and reversed text on purple.
- **Warm Ink** (`ink`): default headings and reading text.
- **Muted Gray** (`muted`): supporting prose, dates, captions, and specifications.
- **Soft Lilac Paper** (`soft`): alternating sections and photograph-caption ground.
- **Quiet Divider** (`line`): roster groups, specifications, and archive rows.
- **Field Outline** (`field-border`): input and textarea boundaries.

**The Real Color Rule.** Keep robot and team photographs naturally colored; let purple framing carry the brand.

## Typography

**Display Font:** Atkinson, served from the self-hosted Atkinson Hyperlegible Next variable font, with sans-serif fallback.

**Body Font:** The same Atkinson family. The loaded face supports weights 200–500, and font synthesis is disabled. No separate mono or display family is used by the current pages.

**Character:** Open letterforms and moderate weights give both the introduction and technical records an approachable voice. Headings use balanced wrapping; body paragraphs stay within 72 characters where available.

### Hierarchy

- **Display:** The frontmatter display role is the homepage headline. At the medium breakpoint it becomes 56px; below 760px it uses `clamp(44px, 8vw, 60px)`. The news title uses `clamp(38px, 5vw, 64px)`.
- **Headline:** The frontmatter headline role introduces major sections. The mission statement uses the smaller `clamp(30px, 3.1vw, 44px)` variant.
- **Title:** The title role introduces smaller groups. Robot names use 30px; roster group titles use 23px and become 21px on the smallest layout.
- **Body:** The body role is the default reading size. Introductory hero prose is 19px on desktop and 17px below 760px; supporting sponsorship prose is 16px.
- **Label:** The label role identifies form fields. Captions and metadata use 13–14px according to context; member names use 19px. These remain ordinary sentence-case supporting text.

**The One Family Rule.** Use the self-hosted Atkinson family throughout; express hierarchy through size, weight, spacing, and color.

## Layout

The shared content wrapper centers at a maximum width of 1440px, using the fluid page-inline spacing token. Main sections use the fluid section-spacing token. Two-column introductions pair a heading or image with copy; related records use open grids rather than boxed panels.

The homepage hero uses a 44%/56% copy-and-image split, changing to 46%/54% below 1100px and stacking below 760px. Its image remains a separate figure, with a caption beneath it. At widths above 1600px, hero text aligns to the shared maximum-width content. The sticky masthead is 96px tall, changing to 76px below 760px. Scroll padding accounts for the header plus 24px.

The layout adapts at 1100px, 760px, and 520px. Roster groups begin with a 240px label column and a three-column member grid; the member grid becomes two columns at 1100px, and group labels move above it at 760px. Project records move from three columns to two at 1100px and one at 520px. Contact and sponsorship become single-column at 760px; paired name fields stack at 520px. News dates move beneath their titles at 760px.

At 520px and below, JavaScript enhances the masthead with a Menu button. Without JavaScript the primary links remain visible. The menu closes after selecting a link or pressing Escape; Escape restores focus to the toggle.

## Elevation & Depth

The system is flat: no box shadows, glass effects, or raised card surfaces. White and soft-tinted sections, fine rules, and image scale establish separation. The sticky white header sits above scrolling content without a shadow.

**The Flat Surface Rule.** Separate content with spacing, tonal surfaces, and fine dividers; keep records and controls free of decorative elevation.

## Shapes

Photographs and section surfaces are rectangular. Buttons and fields use the small control radius; supplied member portraits may use the circular portrait radius. Dividers and input borders are one pixel. Direction icons are inline SVG with thin strokes; they do not require icon fonts or text glyph substitutions.

## Components

### Buttons

Compact, plainly labeled actions. Primary buttons use purple with white text; the light variant uses white with purple text on the hero. Both use the control radius, a minimum height of 50px, and a 28px label-to-arrow gap.

Hover changes only the background over 180ms with `cubic-bezier(.16, 1, .3, 1)`. Focus uses a two-pixel outline with a five-pixel offset, purple on light surfaces and white in the hero and footer. Reduced-motion preference removes transitions and smooth scrolling.

### Inputs / Fields

Labels sit above outlined white fields with an 8px gap. Fields are at least 48px high; the textarea is at least 140px high and resizes vertically. Required and email validation use native browser behavior. The contact form retains its existing external destination; no custom success, error, or disabled presentation is implemented.

### Navigation

A sticky white masthead pairs the existing RDT logo with simple links. Desktop links use 40px gaps, ordinary text, and purple underline on hover or current section. The Contact link is purple at rest. The university descriptor is hidden below 1100px.

The current primary destinations are Team, Previous Years, and Contact. News & publications is a footer link to a separate page; sponsorship is inside Contact. The footer uses deep purple with white links and subdued light metadata. Both pages include a keyboard-visible skip link.

### Text Links

Purple, medium-weight inline-flex links use a 12px gap when paired with an SVG. They gain an underline on hover and share the global focus outline. Links embedded in reading copy retain ordinary underlining.

### Robot Introduction

The supplied static Luna CAD image sits beside a short factual introduction and the Watch Luna in action video link. The user requested removal of the subsystem disclosures. The CAD image remains unlinked and non-draggable; the separate video link is the action.

The homepage hero restores the earlier 15-second Luna testing film at the user's suggestion, with its original still as the fallback. The muted, inline loop loads when permitted by reduced-motion/data-saving preferences. The user explicitly requested no on-page play/pause control. Playback loops continuously, without scroll-triggered pausing, as requested; browser playback policies can still prevent playback. The media itself remains unlinked and non-draggable. No overlay copy, scroll-scrubbing, or extra effects accompany the footage.

### Team and Project Records

Roster groups pair discipline headings and member counts with open member grids. Small line-art avatars are the default; a supplied photo field may render a portrait. Names, roles, and academic metadata come from the existing roster data. The 17 entries are preserved without adding personal links.

The six season records combine prominent purple robot names, definition-list specifications, relevant links, and naturally colored historical imagery. Fine horizontal rules align specification labels and values. Earlier team photographs form a separate simple grid. These records have no card background, enclosing border, or hover lift.

### News Archive

Four original publication references use full-row links separated by fine rules. Each row pairs a title and source with a date and a thin SVG arrow. Hover colors and underlines the title. The undated university profile stays undated; the archive does not imply new reporting.

## Do's and Don'ts

### Do:

- **Do** use the shared purple, neutral, typography, and spacing tokens for new surfaces.
- **Do** show actual team and robot media, retain meaningful alt text and captions, and preserve asset provenance.
- **Do** keep controls native where practical and keyboard focus clearly visible.
- **Do** preserve roster, season, publication, and contact facts when changing presentation.
- **Do** use the same simple masthead, footer, and reading rhythm across pages.

### Don't:

- **Don't** reintroduce the rejected exploded-model tour, floating leader lines, drawing-sheet decorations, or design-variant selector.
- **Don't** add moving sponsor names or make scrolling depend on a presentation sequence.
- **Don't** recolor photographs into purple artwork or cover their subject with interface text.
- **Don't** invent metrics, awards, deadlines, sponsor benefits, or form-success behavior.
- **Don't** apply decorative shadows, extra font families, or boxed treatment to the open roster and project grids.
