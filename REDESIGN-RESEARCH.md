# RDT redesign research — September 16, 2026

## Brief

Replace the overdesigned presentation, particularly the exploded assembly and leader lines. Preserve the useful team grouping and previous-years breakdown. Remove News from primary navigation, preserve all four article/publication references on a separate page, and link it from the footer. Rename Sponsors to Contact and place sponsorship within that section. Purple is permitted as the main or accent color.

## References inspected

These observations combine the sites' public content with browser captures; they are design judgments, not claims of usability-test results.

| Reference | Useful lesson for RDT | What to avoid carrying over |
| --- | --- | --- |
| [CalSol](https://calsol.berkeley.edu/) | A real vehicle establishes the subject immediately. The team identity is recognizable at large and small scales. | Several navigation categories and nested routes are unnecessary for RDT's smaller content set. |
| [Michigan Solar Car](https://www.solarcar.engin.umich.edu/) | Organizes its story around people, mission, and the current challenge. | The hero was blank in the captured browser session; RDT needs a dependable image before motion loads. |
| [Olin Baja](https://www.olinbaja.org/) | Workshop imagery and plain student-centered language communicate what participation feels like. | Avoid text covering the most important part of a photo, and avoid adding more navigation than RDT needs. |
| [Olin Electric Motorsports](https://olinelectricmotorsports.com/) | Real people and a real vehicle provide credibility; sponsorship is explained through tangible ways to help. | Its navigation and long fundraising copy would make RDT's homepage too busy. |
| [Cornell Mars Rover](https://marsrover.engineering.cornell.edu/) | A relevant robotics comparison: actual rover footage, immediately legible identity, and a direct path to the team and rovers. | A video must have a useful static fallback; avoid building the whole visitor journey around playback. |
| [MIT Solar Electric Vehicle Team](https://www.mitsolar.com/) | Connects vehicle history, subteams, and the educational purpose of building together. | RDT does not need the same number of display headings, slogans, and competing content blocks. |

## Recommended design

A direct student engineering team website. White page, NYU purple as the defining brand color, readable sans-serif typography, real Luna photography, and ordinary scrolling. The website's identity comes from its robot and its people.

### Homepage

1. A small RDT mark and three primary links: **Team · Previous Years · Contact**. The logo returns home.
2. A prominent Luna photograph, paired with the actual name **NYU Robotic Design Team**, a short factual introduction, and one primary link to meet the team. Purple carries the title area; the photograph remains naturally colored. On phones, text and photo stack.
3. **Meet Luna:** a concise explanation of the Lunabotics robot and four subsystems. Recommended treatment: a real robot image and four plain-language descriptions. No scroll track, drawing-sheet readouts, progress rail, or floating leader lines. An optional 3D viewer remains a user decision.
4. **Team:** preserve the roster, discipline groupings, names, roles, and useful hierarchy. Reduce decorative numbering and repeated labels. Do not change the underlying data or invent member statistics.
5. **Previous Years:** preserve season names, specifications, proof-of-life links, and the existing historical content. Give robot names and seasons clear prominence; supporting metadata stays smaller.
6. **Contact:** lead with the existing team email and contact form. Include sponsorship interest and the four existing supporters in a quiet, static section. No moving ticker.
7. Footer: university affiliation, team social links, address, copyright, and **News & publications**.

### News page

`news.html` uses the same header and footer and an uncomplicated reading layout. Preserve all four existing references and their recorded titles/dates:

- Brooklyn Eagle — NYU Tandon Downtown Brooklyn showcase, May 2, 2023.
- NYU Tandon — Research Excellence Exhibit, May 2, 2023.
- NYU Tandon — Coney Island and Mars, July 20, 2021.
- NYU Tandon — RDT Vertically Integrated Projects profile, undated.

Link to the source publications; do not copy their articles or present an undated profile as breaking news.

## Open decisions sent to the user

- Primary homepage audience: prospective members, members and sponsors equally, or sponsors.
- Robot presentation: photo with subsystem descriptions, or optional 3D viewer.
- Build workflow: direct implementation, or a visual mockup before implementation.

The user subsequently approved proceeding with this direction and supplied additional photographs. The implementation now lives in `index.html` and `news.html`; see `DIRECTIONS.md` for the current preview and asset notes.
