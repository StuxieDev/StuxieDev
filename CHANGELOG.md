# Changelog

All notable changes to this profile repo are documented here. The format is
based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this
project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

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
