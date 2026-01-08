# Agent Guidelines for atduyar.com

## Build Commands
- `npm run dev` - Start dev server at localhost:4321
- `npm run build` - Build production site to ./dist/
- `npm run format` - Format code with Biome (auto-fixes)
- `npm run deploy` - Format → Build → Deploy to Cloudflare Workers

## Design Philosophy
**Dark Brutalist Minimalism with Dark Fantasy/Grimdark Elements**

**Core Principles:**
- **Typography**: Sinistre Variable font at weight 72 for headlines, Old Turkic runes for mystic elements
- **Colors**: Near-black backgrounds (#111216, #121417), bright white text, minimal blue-300, red-900 for dramatic states
- **Spacing**: Generous padding (p-16 = 4rem), horizontal dividers for rhythm
- **Identity**: Variable font as primary visual element, nothing gratuitous

**Patterns:**
- Contract-signing ritual: Contact button turns form red with bright red text
- Old Turkic BackgroundMarquee for atmospheric texture
- 60-30-10 color rule: 60% neutral, 30% white text, 10% accent colors

**Avoid:**
- Separate skills sections (integrate into experience/projects)
- Over-use of blue (keep it subtle)
- Gratuitous animations or decorations

## Code Style

**Formatting:**
- Tabs for indentation, double quotes
- TypeScript strict mode, Biome linter (auto-organizes imports)

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

- Props interface named `Props`, destructure `Astro.props`
- Slots: default `<slot/>` or named `slot="name"`
- Import with `.astro` extension

**Naming:**
- Files: PascalCase (HomeSection.astro)
- Variables: camelCase (className)
- HTML classes: kebab-case

**CSS:**
- Use only Tailwind. Raw CSS only for `@property` or similar needs.
