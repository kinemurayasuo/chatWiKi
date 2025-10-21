# Repository Guidelines

## Project Structure & Module Organization
NDH.html houses the entire reader interface, including layout, styling hooks, and inline copy. Keep new structural sections grouped inside clearly labeled `<section>` wrappers and annotate significant blocks with HTML comments for quick scanning. Store any supporting media under an `assets/` directory at the repository root and reference them with relative paths to preserve offline compatibility. README.md is reserved for a high-level blurb; expand contributor-facing notes in this file instead.

## Build, Test, and Development Commands
Use a lightweight static server to preview changes; PowerShell example: `python -m http.server 8000` from the repository root, then open `http://localhost:8000/NDH.html`. On Windows you can also launch the page directly with `start msedge.exe .\NDH.html` for a quick smoke check. Keep the Tailwind CDN URL pinned to the published version already referenced in the head tag to avoid unexpected design shifts.

## Coding Style & Naming Conventions
Follow the existing two-space indentation and keep inline text content wrapped for readability at ~100 characters. Compose Tailwind utility class lists from layout to appearance (`flex` -> spacing -> color) and align them across related elements to simplify diff reviews. Name any new HTML files with lowercase hyphenated slugs (e.g., `chapter-index.html`) and mirror that pattern for supporting asset folders.

## Testing Guidelines
There is no automated test suite; run manual regressions in Chromium and a secondary browser (Edge or Firefox) before pushing. Validate that story navigation, typography, and responsive breakpoints render cleanly down to 360px width. Check the developer console for network errors, especially external image hosts, and capture screenshots of critical sections for regression tracking.

## Commit & Pull Request Guidelines
Match the concise style already in history; one-line, imperative summaries are preferred (Korean or English are both acceptable). Reference related discussion IDs in the body and bullet the key visual or content updates. Pull requests should include before/after screenshots for major layout edits and list the manual verification steps you performed so reviewers can replicate.
