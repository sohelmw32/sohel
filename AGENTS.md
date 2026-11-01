# Repository Guidelines

## Project Structure & Module Organization

This is a static personal website for Sohel Tamrakar’s credit advisory services. `index.html` contains page content, semantic markup, and the embedded SVG house illustration. `styles.css` defines the theme and responsive layouts. `app.js` implements tabs, mobile navigation, and the enquiry email workflow. `assets/` contains the portrait, favicon, local fonts, and `fonts.css`. See `README-HOSTING.txt` for hosting instructions. There is no backend, package manifest, or test directory.

## Build, Test, and Development Commands

- `python3 -m http.server 8000 --bind 127.0.0.1`: serve the repository locally; visit `http://127.0.0.1:8000`.
- `open -a Safari http://127.0.0.1:8000`: open the local preview on macOS.
- `node --check app.js`: check JavaScript syntax if Node.js is installed; Node.js is optional for development.
- `git diff --check`: detect whitespace errors before committing.

No build step or dependency installation is required. Deploy `index.html`, `styles.css`, `app.js`, and the complete `assets/` directory together, keeping their relative paths intact.

## Coding Style & Naming Conventions

Match surrounding formatting and avoid reformatting unrelated code. HTML uses two-space nesting; CSS and JavaScript currently use compact formatting. Use two spaces when introducing multiline blocks. JavaScript uses `const`/`let`, camelCase identifiers, and native DOM APIs. Use kebab-case for CSS classes and HTML IDs, and preserve the `data-stage` and `data-scheme` hooks used by scripts. Reuse CSS custom properties in `:root`. No formatter or linter is configured.

## Testing Guidelines

There is no automated test framework or coverage target. Check changed interactions manually at desktop and mobile widths: navigation, both tab groups, FAQ disclosures, form validation, generated email text, mailto links, and clipboard fallback. Verify keyboard navigation, focus visibility, ARIA state updates, reduced-motion behavior, asset loading, and browser console errors. The enquiry form prepares an email draft; it does not submit to a server.

## Commit & Pull Request Guidelines

History contains brief subjects such as “First website” and “Initial commit”; no formal convention is established. Use concise, descriptive imperative subjects. Pull requests should explain the change, list validation performed, link relevant issues, and include desktop/mobile screenshots for visual changes.

## Content & Hosting Precautions

Keep credentials and personal enquiry data out of the repository. Preserve financial disclosures and verify dated scheme information when changing related copy. Keep `noindex,nofollow` until search indexing is explicitly approved.
