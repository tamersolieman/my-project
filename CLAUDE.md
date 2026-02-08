# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A bilingual (English/Arabic) personal website and portfolio for Tamer Solieman — Product Leader, Agile Coach, and Podcast Host. The site features dark mode support, RTL/LTR language toggling, and sections for About, Contact, Podcast ("Mrn Podcast"), and Blog.

## Architecture

- **`index.html`**: Main entry point — contains all HTML structure and inline JavaScript for dark mode and language toggling. Uses `localStorage` to persist user preferences.
- **`styles.css`**: All styling including CSS custom properties for theming (light/dark mode), responsive layout, and RTL support. Uses the Almarai Google Font.
- **`images/`**: SVG logo (`mrn_logo_blue.svg`) and PNG assets for the podcast section.
- **`oldindex.html`**: Previous version of the site kept for reference.
- **`.vscode/settings.json`**: VS Code editor configuration.

## Development

### Building/Running
This is a static HTML project with no build process. To view the website:
- Open `index.html` directly in a web browser, or
- Serve it using a local HTTP server (e.g., `python3 -m http.server 8000`)

### Key Patterns
- **Bilingual content**: English and Arabic text coexist in the DOM using `.en-content` and `.ar-content` classes. The `.hidden` class toggles visibility.
- **Dark mode**: Controlled via a `data-theme="dark"` attribute on the `<html>` element. CSS variables swap between light and dark palettes.
- **Brand colors**: Primary blue `#0A7BD2` from the MRN logo. All theme colors are derived from a blue spectrum defined as CSS custom properties in `:root`.

### Common Tasks
- **Edit content**: Modify `index.html` directly — update both `.en-content` and `.ar-content` spans for bilingual changes.
- **Edit styles**: Modify `styles.css` — use the existing CSS custom properties for consistency.
- **Preview**: Open `index.html` in a browser or use a local development server.

## Notes

- No build tools, package manager, or testing framework are configured.
- No `.gitignore` is present — consider adding one if build artifacts or dependencies are introduced.
