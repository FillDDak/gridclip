# Changelog

All notable changes to this project are documented here. The format follows
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/) and the project uses
[Semantic Versioning](https://semver.org/).

## [1.0.0] - 2026-11-11

First release.

### Added

- `parseClipboard`, `setClipboardData`, `stringifyClipboard`: read and write both clipboard flavours (TSV and HTML table), combining exact TSV values with HTML merges.
- `copyToClipboard`, `readFromClipboard`: Async Clipboard API with `execCommand` and `writeText` fallbacks.
- `parseTSV`, `stringifyTSV`: spreadsheet-compatible TSV/CSV with round-trip guarantees.
- `parseHTMLTable`, `stringifyHTMLTable`: DOM-free HTML table model with merged cells, Excel/Sheets/LibreOffice/Word quirks, CSS white-space handling and a `maxCells` guard; serialised spaces survive pasting into Excel (written as `mso-spacerun`, verified with Excel for Windows).
- `applyPaste`, `sliceGrid`: spreadsheet paste semantics (tiling, growing, clipping).
- ESM, CommonJS and IIFE (`<script>`) builds with TypeScript declarations.
- Clipboard data captured from real Excel for Windows as test fixtures, and `examples/clipboard-capture.html` to capture more.
- Browser tests run in Chromium, Firefox and WebKit (`npm run test:browser:<engine>`), and CI runs them on Linux and Windows.
