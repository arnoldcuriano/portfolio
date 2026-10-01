# Portfolio Agent Rules

## Authority
Follow instructions in this order:
1. Explicit user requirements
2. `docs/DESIGN.md`
3. `docs/CONTENT.md`
4. This `AGENTS.md`
5. Anti-Slop guidance
6. Ponytail guidance
7. General agent defaults

If plugin guidance conflicts with an intentional decision in the SSOT, the SSOT wins.

## Product Goal
Build Arnold Curiano's public developer portfolio: professional, technical, premium, simple, fast, accessible, and distinctly human-designed. It must not resemble a generic AI-generated SaaS/portfolio template.

## Engineering Principles
- Use the minimum implementation that satisfies the requirement.
- Prefer native Astro, HTML, CSS, and browser APIs before adding client-side frameworks or dependencies.
- React is optional and must earn its place for a genuinely interactive island.
- Avoid premature abstractions, unnecessary wrappers, providers, contexts, helpers, and state libraries.
- Extract a component when it is reused or when extraction materially improves readability.
- Keep components focused and files reasonably small; do not split code merely to satisfy arbitrary line counts.
- TypeScript should remain strict and useful. Avoid `any` unless unavoidable and documented.
- Use semantic HTML and progressive enhancement.
- Preserve excellent keyboard navigation, visible focus states, reduced-motion support, and appropriate ARIA only when native semantics are insufficient.
- Responsive behavior is designed intentionally, not achieved by simply stacking desktop UI at a breakpoint.
- Never expose secrets, private repositories, internal screenshots, confidential data, credentials, or client-sensitive information.

## Initial Technical Baseline
- Astro
- TypeScript
- Tailwind CSS 4
- Markdown/MDX for writing
- Astro Content Collections for blog content
- Vercel deployment target
- GitHub repository is public

Do not add a database, CMS, authentication, state-management library, component framework, or animation library unless a concrete requirement justifies it.

## Styling Rules
- Tailwind implements the design system; it does not invent it.
- Establish reusable design tokens for colors, typography, spacing, containers, borders/radii, and motion.
- Avoid arbitrary values when an existing token can express the intent.
- Do not use gradients.
- Do not use decorative glassmorphism, glowing effects, generic SaaS cards, oversized pills, floating blobs, fake dashboards, or fake terminal aesthetics.
- Do not generate custom icons/SVG illustrations as decoration.
- Use an established icon library only when icons are genuinely necessary. Navigation should use almost no icons except the mobile menu control if appropriate.
- Structural UI should remain sharp. Media may use a restrained radius.

## Motion Rules
- Motion must support storytelling or interaction comprehension.
- Prefer CSS and browser APIs first.
- A small animation dependency may be introduced only if the required project storytelling cannot be implemented cleanly without it.
- Respect `prefers-reduced-motion`.
- No bouncing, gratuitous parallax, flying technology logos, cursor trails, or animation everywhere.
- Custom cursor behavior, if implemented, is limited to interactive project media and must not reduce usability.

## Content Rules
- Keep copy concise, specific, and professional.
- Avoid AI-sounding hype, vague superlatives, inflated claims, and filler.
- Never invent project outcomes, metrics, responsibilities, employers, dates, clients, technologies, or case-study details.
- Confidential projects may show only an approved public landing page or one safe screenshot.
- Employment/work history belongs primarily on the resume route, not as a long homepage timeline.

## Plugin Responsibilities
### Ponytail
Use Ponytail to minimize implementation complexity and challenge unnecessary code/dependencies. Ponytail governs implementation simplicity, not visual direction.

### Anti-Slop
Use Anti-Slop to catch generic AI UI/copy patterns, weak responsive behavior, accessibility issues, and unnecessary visual conventions. Anti-Slop must not override deliberate decisions in `docs/DESIGN.md`.

## Workflow
- Read `AGENTS.md`, `docs/DESIGN.md`, and `docs/CONTENT.md` before implementation work.
- Work incrementally and keep each phase reviewable.
- Do not build the entire site in one pass.
- Before adding a dependency, state what requirement it solves and why native/current dependencies are insufficient.
- Run relevant format, type, build, and accessibility checks before declaring a phase complete.
- After each implementation phase, inspect the actual Git diff and run `npm run review`. Review the diff with Ponytail and, when available, Anti-Slop. Report legitimate findings and fix those that do not conflict with `docs/DESIGN.md` or user requirements. Never claim an automated Anti-Slop review ran when its skill or tool was unavailable.
- Preserve a clean public Git history with focused commits.
