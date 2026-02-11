# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/), and this
project adheres to [Semantic Versioning](https://semver.org/).

## [1.2.0] - 2026-02-11

### Added

- **Auto-recompare** — changing options (Strip Markdown, view mode) or swapping
  texts automatically re-runs the comparison.
- **Edit inputs toggle** — inputs hide after comparing to maximize diff output
  space; click "Edit inputs" to restore them.

### Fixed

- Layout overlap when showing inputs after a comparison.

### Changed

- Pinned jsdiff CDN to exact version (7.0.0) with SRI integrity hash.
- Added `<noscript>` fallback for users with JavaScript disabled.
- Added favicon to suppress browser 404 requests.
- Added offline fallback message when jsdiff CDN is unreachable.
- Refactored `stripMarkdown` to use named regex constants for readability.
- `showMessage` now respects the active view mode (side-by-side or inline).
- Replaced mutable `hasCompared` flag with DOM-derived state.
- Used `const` instead of `let` where values are not reassigned.

## [1.1.0] - 2026-02-06

### Changed

- Replaced custom LCS diff algorithm with [jsdiff](https://github.com/kpdecker/jsdiff)
  (`Diff.diffWords`) via CDN for more accurate word-level diffs.
- Default diff view is now **side by side** — original on the left (deletions in
  red), changed on the right (additions in green).

### Added

- **Side-by-side view** — each panel shows coherent, readable text with only its
  relevant highlights.
- **View toggle** — switch between "Side by side" and "Inline" diff modes.

## [1.0.0] - 2026-02-06

### Added

- Two side-by-side text areas for pasting original and changed text.
- Word-level diff using an LCS (Longest Common Subsequence) algorithm.
- Inline diff output with color-coded highlights (red for deletions, green for additions).
- Strip Markdown option to remove formatting before comparing.
- Compare, Swap, and Clear buttons.
- Responsive layout that stacks vertically on narrow screens.
- Accessible markup with labeled inputs and semantic HTML.
