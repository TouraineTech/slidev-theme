# Changelog

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project adheres to [Semantic Versioning](https://semver.org/).

## [Unreleased]

### Changed

- The `@tourainetech` link in the `end` layout points to x.com.
- GitHub release notes come from this changelog.

## [1.1.0] - 2026-11-08

### Changed

- Compatible with Slidev 53 (developing the theme requires Node.js >= 22.22).
- The theme forces dark mode, since every content layout has a dark background. The `variant: light` option of `cover`, `section` and `end` is still available.
- The `end` layout shows the `@tourainetech` handle, the one linked from touraine.tech.

### Fixed

- Quotes and code blocks are readable on dark backgrounds.
- `pnpm export` works (adds `playwright-chromium`).

### Added

- Automatic npm publishing, with provenance, for every new version on `main`.

## [1.0.0] - 2025-12-20

### Added

- `cover`, `default`, `section`, `two-cols` and `end` layouts, with `dark` and `light` variants for `cover`, `section` and `end`.
- `<TntLogo>` component.
- Touraine Tech colors, Noto Sans and Fira Code fonts.

[Unreleased]: https://github.com/TouraineTech/slidev-theme/compare/v1.1.0...HEAD
[1.1.0]: https://github.com/TouraineTech/slidev-theme/compare/44d15d3...v1.1.0
[1.0.0]: https://github.com/TouraineTech/slidev-theme/commit/44d15d3
