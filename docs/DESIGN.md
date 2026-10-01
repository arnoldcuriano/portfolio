# Portfolio Design SSOT

## Design Identity
**Monochrome Technical Editorial**

The portfolio should feel like a developer's body of work presented editorially: professional, technical, premium, quiet, and deliberate. It is not a SaaS landing page, dashboard, agency template, hacker terminal, or futuristic AI site.

Reference inspiration may include the restraint, whitespace, navigation clarity, and technical feel Arnold likes from Bryl Lim's portfolio, but this project must establish its own composition and identity rather than copy another site.

## Core Principles
1. Work is the focal point, not the portrait.
2. Typography, spacing, real project imagery, and restrained motion create the personality.
3. Keep the homepage concise despite containing meaningful information.
4. Interactions should feel intentional rather than impressive for their own sake.
5. Every layout must work naturally from small mobile screens through wide desktop screens.
6. System light/dark preference is respected.

## Typography
### Primary
Use **Inter** for headings, navigation, body copy, controls, and general interface text.

Use a restrained set of weights, likely 400/500/600 unless implementation proves another weight necessary.

### Technical Accent
Use a clean modern monospace typeface for subtle technical metadata such as:
- work section metadata
- dates
- roles
- stack metadata
- location/availability labels

The monospace face supports Inter; it must not turn the site into a terminal aesthetic. Exact monospace family remains a design implementation decision and should be evaluated visually before locking it.

## Color
### Light
- Background: pure white (`#FFFFFF`)
- Primary text: pure/near pure black (`#000000`)
- Neutral grays: only as needed for hierarchy, borders, secondary metadata, disabled states

### Dark
- Background: pure black (`#000000`)
- Primary text: white (`#FFFFFF`)
- Neutral grays: only as needed for hierarchy and borders

No brand gradient. No generated gradients. Do not introduce a decorative accent color merely because portfolios typically have one.

Use `prefers-color-scheme` as the initial theme source. A future accessible Light/Dark control should persist an explicit choice, let that choice override the OS preference, and prevent an incorrect-theme flash. Prefer native browser capabilities over React. The control is deferred beyond Phase 1.

## Width and Grid
Use a **balanced** content width:
- generous whitespace
- readable text measures
- project screenshots large enough to carry visual weight
- avoid both narrow magazine columns and edge-to-edge everything

Use a consistent container/grid system rather than per-section arbitrary widths.

## Corners and Borders
Use a mixed treatment:
- structural layout, navigation, dividers, controls: sharp or nearly sharp
- project media/screenshots: restrained subtle radius where it improves presentation

Avoid the large rounded-card language common to generated SaaS interfaces.

## Navigation
Desktop direction:

`AC.     WORK   ABOUT   WRITING   CONTACT`

Navigation is technical/editorial and compact. Resume and capabilities remain accessible without making the primary navigation visually noisy; exact placement may be determined during implementation while preserving content discoverability.

Mobile:
- `AC.` brand/mark
- minimal menu icon
- accessible menu interaction
- no cramped desktop navigation squeezed onto mobile

## Hero
Use content-driven height, not an artificial `100vh` hero.

Primary identity:
**Full-Stack Developer**

The hero should quickly communicate what Arnold does, experience level, Philippines location, and approved work preferences without excessive copy.

Structured hero metadata uses subdued labels and clear monospace values for location, experience, and work preferences. The Open to value cycles through Part-time, Contract, and Full-time; reduced-motion users see a stable presentation of all three.

No decorative 3D objects, gradients, technology-logo clouds, fake code terminals, or oversized portrait.

## Project Experience
### Desktop
Use **storytelling split** composition.

Project information and project imagery form a coordinated scroll sequence. Project context may become temporarily sticky while media moves/reveals. Motion should make the work easier to absorb, not turn the page into a demo reel.

Project content is deliberately concise:
- title
- short description
- role
- stack

Do not add invented challenge/result sections or metrics.

### Mobile
Use a natural linear story:
1. project number/title
2. description
3. role/stack metadata
4. screenshot/media
5. next project

Do not force desktop sticky split behavior onto phones.

### Screenshot Treatment
Treatment depends on project context:
- public website: natural site screenshot may stand on its own
- application/internal product: minimal frame may provide context
- confidential work: only a public landing page or one approved safe screenshot

Avoid fake browser chrome with decorative colored dots unless there is a genuine presentational reason.

## Motion
Motion direction: **combined storytelling**.

Permitted examples:
- restrained opacity/translate reveals
- temporary sticky project metadata on desktop
- subtle screenshot transitions
- small hover feedback
- restrained project-media cursor treatment

Rules:
- native CSS/browser APIs first
- preserve reading/scroll control
- no scroll hijacking
- no gratuitous parallax
- no bouncing objects
- no flying logos
- no motion-only communication
- reduced-motion mode must remain complete and polished

## Cursor
Use the normal browser cursor globally.

Navigation links may show a restrained text `|` after the active label on hover or keyboard focus. Reduced-motion users see it without blinking.

A subtle custom cursor/label may be used only over interactive project media if it adds useful affordance. It must degrade cleanly on touch devices and reduced-motion contexts.

## Imagery
Real work is preferred over decorative illustration.

Portrait may appear in About but is secondary. The portfolio's selling point is Arnold's work and capability.

## Capabilities Presentation
Group skills by capability rather than displaying a logo wall or skill percentages:
- Frontend
- Backend
- WordPress / CMS
- Cloud / DevOps
- AI Development

Typography and grouping should carry the section. Technology icons are unnecessary by default.

## Writing Presentation
Show the latest 2–3 articles near the bottom of the homepage with concise metadata and a clear route to all writing.

Blog pages should retain the same editorial system and prioritize reading quality.

## Contact Presentation
Support both:
- minimal contact form
- direct Email / LinkedIn / Book a Call actions

Use whitespace and hierarchy so the section remains calm and clean. Do not turn it into a dense card cluster.

## Responsive Principles
- Mobile is a deliberate composition, not a collapsed desktop design.
- Avoid horizontal overflow and tiny metadata.
- Maintain comfortable touch targets.
- Project storytelling becomes linear on mobile.
- Typography scales fluidly but should not use enormous display text merely for visual impact.
- Verify intermediate widths, not only phone and desktop breakpoints.

## Explicit Anti-Patterns
Do not introduce:
- gradients
- glassmorphism
- glowing neon treatments
- generic bento grids simply because they are trendy
- giant rounded cards
- excessive pill UI
- decorative blobs
- fake dashboards
- fake terminal sections
- AI-generated illustrations/icons
- skill percentage bars
- giant technology-logo walls
- gratuitous 3D
- generic "crafting digital experiences" style copy
- excessive animation
- overlong homepage copy
