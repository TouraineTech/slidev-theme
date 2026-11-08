# Slidev Theme Touraine Tech

Theme officiel [Slidev](https://sli.dev) pour les presentations Touraine Tech.

## Installation

```bash
pnpm add slidev-theme-touraine-tech
```

## Usage

Dans le frontmatter de votre presentation :

```yaml
---
theme: touraine-tech
---
```

### Usage local (developpement)

```yaml
---
theme: ./path/to/themes/slidev
---
```

## Layouts

### `cover`

Page de titre de la presentation.

```yaml
---
layout: cover
variant: dark  # ou 'light'
---

# Titre de ma presentation

Nom du speaker
```

| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `variant` | `'dark'` \| `'light'` | `'dark'` | Style du fond |

### `default`

Layout standard pour le contenu.

```yaml
---
layout: default
---

# Mon titre

- Point 1
- Point 2
```

### `section`

Transition entre sections.

```yaml
---
layout: section
variant: dark  # ou 'light'
---

# Nouvelle section

Sous-titre optionnel
```

| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `variant` | `'dark'` \| `'light'` | `'dark'` | Style du fond |

### `two-cols`

Contenu sur deux colonnes.

```yaml
---
layout: two-cols
---

# Colonne gauche

Contenu a gauche

::right::

# Colonne droite

Contenu a droite
```

### `end`

Page de fin / remerciements.

```yaml
---
layout: end
variant: dark  # ou 'light'
---

# Merci !

Des questions ?
```

| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `variant` | `'dark'` \| `'light'` | `'dark'` | Style du fond |

## Composants

### `<TntLogo>`

Logo Touraine Tech reutilisable.

```vue
<TntLogo size="md" />
<TntLogo size="lg" inverted />
```

| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `size` | `'sm'` \| `'md'` \| `'lg'` \| `'xl'` | `'md'` | Taille du logo |
| `inverted` | `boolean` | `false` | Logo blanc (pour fonds sombres) |

## Couleurs

| Variable | Valeur | Usage |
|----------|--------|-------|
| `--tnt-primary` | `#222333` | Fond sombre, texte sur fond clair |
| `--tnt-secondary` | `#6ABFAD` | Accents, liens, decorations |
| `--tnt-white` | `#ffffff` | Fond clair, texte sur fond sombre |

### Classes utilitaires

```html
<div class="bg-tnt-primary">Fond sombre</div>
<div class="bg-tnt-secondary">Fond turquoise</div>
<div class="text-tnt-primary">Texte sombre</div>
<div class="text-tnt-secondary">Texte turquoise</div>
<div class="text-tnt-white">Texte blanc</div>
```

## Typographie

- **Police** : Noto Sans (Google Fonts)
- **Code** : Fira Code

## Developpement

```bash
# Cloner le repo
git clone https://github.com/tourainetech/slidev-theme

# Installer les dependances (Node.js >= 22.22)
pnpm install

# Lancer le serveur de dev
pnpm dev
```

## License

MIT
