# AGENTS.md

## Project overview

This repository is a small static marketing site for STEM-Park. The project is intentionally lightweight and is built around a single HTML file with embedded CSS and JavaScript.

- Primary app file: `index.html`
- No framework, bundler, or package manager is required
- Content is mostly static, but the page includes a language switcher and a Formspree contact form

## Working conventions

- Keep changes simple and in the existing style of the page
- Prefer vanilla HTML/CSS/JavaScript over introducing frameworks or build tooling
- Preserve the current section structure: home, about, projects, pricing, contact, footer
- Keep the translation structure consistent if updating text: the `translations` object in the script should stay aligned with `data-i18n` attributes in the markup
- Prefer small, targeted edits over broad rewrites

## Validation

Because this is a static page, validation is primarily visual and browser-based:

1. Start a local static server from the project root:
   `python -m http.server 8000`
2. Open `http://localhost:8000/` in a browser
3. Check the landing page layout, mobile menu behavior, language switching, and form submission flow

## Common tasks

### Updating content

- Add or edit text directly in `index.html`
- Keep wording consistent across Russian, Kazakh, and English versions when relevant
- Preserve the `data-i18n` keys used by the language switcher

### Styling updates

- Prefer updating the existing CSS variables and section styles in the `<style>` block
- Keep the dark STEM theme and gradient accent styling unless a stronger visual direction is explicitly requested

### JavaScript updates

- Keep event handlers and scripts simple and readable
- Preserve the existing `setLanguage()` behavior and the mobile navigation toggle
- If form behavior changes, keep the Formspree submission logic and user feedback messages intact

## Hard constraints

- Do not add dependencies or a frontend framework unless the user explicitly asks for it
- Do not remove the multilingual behavior without a clear requirement
- Do not restructure the page into a multi-file app unless the task explicitly requires it

## Useful references

- Main implementation: `index.html`
- Browser preview: `http://localhost:8000/`
