# Changelog

Format inspiré de [Keep a Changelog](https://keepachangelog.com/fr/1.1.0/), versions selon [SemVer](https://semver.org/lang/fr/).

## [Non publié]

## [1.1.0] - 2026-11-08

### Modifié

- Compatible Slidev 53 (Node.js >= 22.22 pour développer le thème).
- Le thème force le mode sombre : tous les layouts de contenu ont un fond sombre. Les variantes `variant: light` de `cover`, `section` et `end` restent disponibles.
- Le layout `end` affiche le compte `@tourainetech`, celui du site touraine.tech.

### Corrigé

- Citations et blocs de code lisibles sur fond sombre.
- `pnpm export` fonctionne (ajout de `playwright-chromium`).

### Ajouté

- Publication npm automatique, avec provenance, à chaque nouvelle version sur `main`.

## [1.0.0] - 2025-12-20

### Ajouté

- Layouts `cover`, `default`, `section`, `two-cols` et `end`, avec variantes `dark` et `light` pour `cover`, `section` et `end`.
- Composant `<TntLogo>`.
- Couleurs Touraine Tech, polices Noto Sans et Fira Code.

[Non publié]: https://github.com/TouraineTech/slidev-theme/compare/v1.1.0...HEAD
[1.1.0]: https://github.com/TouraineTech/slidev-theme/compare/44d15d3...v1.1.0
[1.0.0]: https://github.com/TouraineTech/slidev-theme/commit/44d15d3
