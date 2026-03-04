# Copilot Role Map

Use this folder to route requests to the right specialist.

## Agents

- Hugo Developer: `.github/agents/hugo-developer.md`
  - Use for Hugo content structure, front matter, templates, menu/taxonomy behavior, and build correctness.

- Netlify Expert: `.github/agents/netlify-expert.md`
  - Use for deploy setup, `netlify.toml`, redirects/headers, environment strategy, and preview/production parity.

- Graphic Designer: `.github/agents/graphic-designer.md`
  - Use for visual hierarchy, typography, spacing, consistency, and theme-safe design polish.

- UX Engineer: `.github/agents/ux-engineer.md`
  - Use for navigation clarity, information architecture, accessibility, and low-friction user flows.

## Instructions

- Hugo rules: `.github/instructions/hugo.instructions.md`
- Netlify rules: `.github/instructions/netlify.instructions.md`
- Graphic design rules: `.github/instructions/graphic-design.instructions.md`
- UX rules: `.github/instructions/ux.instructions.md`

## Prompts

- Hugo task prompt: `.github/prompts/hugo-developer.prompt.md`
- Netlify task prompt: `.github/prompts/netlify-expert.prompt.md`
- Graphic design prompt: `.github/prompts/graphic-designer.prompt.md`
- UX prompt: `.github/prompts/ux-engineer.prompt.md`
- Personal site strategy prompt: `.github/prompts/personal-site-strategist.prompt.md`

## Quick Routing

- "Fix build/deploy issues" → Netlify Expert
- "Add page / adjust front matter / Hugo behavior" → Hugo Developer
- "Improve visual polish" → Graphic Designer
- "Make site easier to use" → UX Engineer
- "I need direction / structure first" → Personal Site Strategist prompt

For mixed tasks, start with UX Engineer (structure), then Graphic Designer (polish), then Hugo Developer (implementation), then Netlify Expert (deploy hardening).
