# Agent Guidelines for atduyar.com

## Build Commands
- `npm run dev` - Start dev server at localhost:4321
- `npm run build` - Build production site to ./dist/
- `npm run format` - Format code with Biome (auto-fixes)
- `npm run deploy` - Format → Build → Deploy to Cloudflare Workers

## Design Philosophy & Aesthetic

**Style: Dark Brutalist Minimalism with Dark Fantasy/Grimdark Elements**

This portfolio channels neo-brutalist sensibilities mixed with mystic, occult undertones:
- **Aggressive typography**: Sinistre Variable font at weight 72 creates bold, commanding headlines
- **Runic/Mystic elements**: Old Turkic text (runes) adds mysterious, ancient quality
- **High contrast**: Near-black backgrounds (#111216, #121417) with bright white text
- **Sparse color usage**: Blue-300 for subtle interactions, red-900 for dramatic states, #90c5ff14 for structural lines
- **Raw, unpolished feel**: Minimal decorations, exposed structure

**Key Design Patterns:**
- **Contract-signing ritual**: Contact form "Sign" button turns form red, makes text bright red - creates feeling of signing a real contract
- **Atmospheric texture**: Old Turkic BackgroundMarquee creates mystic ambiance without adding content noise
- **Break rhythm**: Horizontal dividers create cinematic pacing between sections
- **Generous whitespace**: Large padding (p-16 = 4rem) gives content breathing room
- **Variable font as identity**: Sinistre's weight variations used as primary visual element, not just for readability

**Design Goals:**
- Express identity through restraint and technical mastery
- Honor cultural heritage (Turkish roots through Old Turkic aesthetics)
- Create mystic/dark fantasy atmosphere through typography and subtle effects
- Demonstrate sophistication through advanced CSS techniques (variable fonts, custom properties, mix-blend modes)
- Maintain minimalist ethos - every pixel intentional, nothing gratuitous

## Code Style

**Formatting:**
- Indentation: Tabs
- Quotes: Double quotes
- TypeScript: Strict mode enabled
- Linter: Biome (auto-organizes imports)

**Astro Components:**
```astro
---
interface Props {
  title: string;
  className?: string;
}
const { title, className } = Astro.props;
---
<div class={...}>{title}</div>
```

- Props interface named `Props`
- Destructure `Astro.props`
- Use slots: default `<slot/>` and named `slot="name"`
- Import with `.astro` extension

**Naming:**
- Files: PascalCase (HomeSection.astro)
- Variables: camelCase (className)
- HTML classes: kebab-case

**CSS:**
- Use `@import "tailwindcss"` in global.css
- Define custom fonts/animations in `@theme` block
- Prefer Tailwind utilities over custom CSS
- Use `@property` for CSS custom properties that animate (e.g., --x)
- Leverage mix-blend modes for layered effects
- Use font-variation-settings for variable font control

**Interactive Patterns:**
- Hover states should be subtle but responsive (blue-300 shifts, -translate-y movements)
- Dramatic states reserved for specific moments (contract signing, major interactions)
- Use group-has-[...] selectors for parent-child interactions
- Radial gradients with custom properties for reveal effects
- Maintain mystic atmosphere - avoid playful/bouncy animations
