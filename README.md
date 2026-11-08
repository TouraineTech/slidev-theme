# Slidev Theme Touraine Tech

Official [Slidev](https://sli.dev) theme for Touraine Tech presentations.

## Installation

```bash
pnpm add slidev-theme-touraine-tech
```

## Usage

In your presentation's frontmatter:

```yaml
---
theme: touraine-tech
---
```

### Local usage (development)

```yaml
---
theme: ./path/to/themes/slidev
---
```

## Layouts

### `cover`

Title slide of the presentation.

```yaml
---
layout: cover
variant: dark  # or 'light'
---

# My presentation title

Speaker name
```

| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `variant` | `'dark'` \| `'light'` | `'dark'` | Background style |

### `default`

Standard content layout.

```yaml
---
layout: default
---

# My title

- Point 1
- Point 2
```

### `section`

Transition between sections.

```yaml
---
layout: section
variant: dark  # or 'light'
---

# New section

Optional subtitle
```

| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `variant` | `'dark'` \| `'light'` | `'dark'` | Background style |

### `two-cols`

Two-column content.

```yaml
---
layout: two-cols
---

# Left column

Left content

::right::

# Right column

Right content
```

### `end`

Closing / thank-you slide.

```yaml
---
layout: end
variant: dark  # or 'light'
---

# Thank you!

Any questions?
```

| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `variant` | `'dark'` \| `'light'` | `'dark'` | Background style |

## Components

### `<TntLogo>`

Reusable Touraine Tech logo.

```vue
<TntLogo size="md" />
<TntLogo size="lg" inverted />
```

| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `size` | `'sm'` \| `'md'` \| `'lg'` \| `'xl'` | `'md'` | Logo size |
| `inverted` | `boolean` | `false` | White logo (for dark backgrounds) |

## Colors

| Variable | Value | Usage |
|----------|-------|-------|
| `--tnt-primary` | `#222333` | Dark background, text on light background |
| `--tnt-secondary` | `#6ABFAD` | Accents, links, decorations |
| `--tnt-white` | `#ffffff` | Light background, text on dark background |

### Utility classes

```html
<div class="bg-tnt-primary">Dark background</div>
<div class="bg-tnt-secondary">Teal background</div>
<div class="text-tnt-primary">Dark text</div>
<div class="text-tnt-secondary">Teal text</div>
<div class="text-tnt-white">White text</div>
```

## Typography

- **Font**: Noto Sans (Google Fonts)
- **Code**: Fira Code

## Development

```bash
# Clone the repo
git clone https://github.com/TouraineTech/slidev-theme

# Install dependencies (Node.js >= 22.22)
pnpm install

# Start the dev server
pnpm dev
```

### Releasing

Record every change under `[Unreleased]` in the [CHANGELOG](./CHANGELOG.md). To release, open a PR that bumps `version` in `package.json` and renames the `[Unreleased]` section to that version: on merge, CI publishes to npm and creates the GitHub release. A PR without a version bump publishes nothing.

## License

MIT
