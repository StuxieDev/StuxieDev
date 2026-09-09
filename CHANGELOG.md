# Changelog

All notable changes to this profile repo are documented here. The format is
based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this
project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## v1.1.6

### Fixed
- `Generate Devcards` workflow's `devcard` and `devcard-dark` jobs both committed
  to the same `devcard` branch in parallel, racing on its HEAD sha and failing
  with a 409 whichever job committed second — serialized `devcard-dark` after
  `devcard`

## v1.1.5

### Changed
- `CONTRIBUTING.md`'s general contact address changed from `contact@stuxie.dev` to `hello@stuxie.dev`, matching the convention used across other StuxieDev/Stux.Group repos

## v1.1.4

### Changed
- Footer's attribution line reformatted to match Automater's standard StuxieDev footer (icon + link) - no footer existed here before

## v1.1.3

### Changed
- Website badge color changed from dark grey (`24292F`) to purple (`6B00A2`)
- "Languages & Tools" now uses a single [skillicons.dev](https://skillicons.dev) icon strip instead of individual shields.io badges

## v1.1.2

### Fixed
- Org stats SVGs in "My Organisations" render via `<foreignObject>` with no `viewBox`, so forcing `width="400"` on the `<img>` (their native size is 480px) made Chromium-based renderers clip the card content instead of scaling it, leaving it looking left-shoved rather than centered — set to their native `width="480"` instead

## v1.1.1

### Fixed
- Org stats images in "My Organisations" weren't actually centered — `<td align="center">` isn't reliably honored by GitHub's renderer; each cell's content is now wrapped in `<div align="center">` (the pattern already proven to work elsewhere in this README) instead

## v1.1.0

### Added
- "Languages & Tools" section with badges for the languages/tools actually used across my repos (Python, PHP, JavaScript, TypeScript, Go, C#, C++, Java, Vue.js, HTML5, Bash, Git, Discord.py)

### Changed
- Website buttons now point to `stuxie.dev` instead of the `stux.ie` short link
- Website badges no longer do a live online/offline check — replaced with a static badge
- "My Organisations" table is now centered and forced to full width, matching the rest of the page

## v1.0.1

### Fixed
- LinkedIn badge missing its icon — shields.io's built-in `linkedin` logo slug
  doesn't render, so it's now embedded as a base64 SVG data URI instead

## v1.0.0

### Added
- `VERSION.md` and `CHANGELOG.md` to track releases
- `commit.sh`/`commit.bat` to commit and tag releases from `VERSION.md`
