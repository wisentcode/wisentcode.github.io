# AGENTS

Purpose: guidance for agentic coding agents operating in this static site repo.

**Build / Serve / Test**:
- Serve locally (quick): `python3 -m http.server 8000` then open `http://localhost:8000`.
- Serve with Node: `npx http-server . -p 8000` or `npx live-server .`.
- Compile SCSS once: `npx sass scss:assets/css` (watch: `npx sass --watch scss:assets/css`).
- Lint/format (recommended): `npx prettier --check .`, `npx htmlhint .`, `npx stylelint "assets/scss/**/*.scss"`, `npx eslint "assets/js/**/*.js"`.
- Tests: no test framework configured. Example to run a single Jest test if added: `npx jest path/to/file.test.js -t "test name"`.

**Code style (short)**:
- HTML/CSS: use semantic HTML, include styles in `<head>` and scripts before `</body>`; use relative paths.
- SCSS: partials start with `_`, filenames in kebab-case, variables/mixins in `_variables`/`_mixin` files (existing pattern).
- CSS classes: prefer BEM-like names (block__element--modifier) and kebab-case for class names.
- JS: use `camelCase` for variables/functions, `PascalCase` for constructors/components, avoid globals.
- Formatting: run `prettier` (project-wide) and keep 2-space indentation for CSS/SCSS/JS.
- Types/docs: add JSDoc comments for public JS functions; consider TypeScript for larger changes.
- Error handling: always handle promise rejections, log errors with context, avoid silent failures.

Cursor/Copilot rules: no `.cursor/` rules or `.github/copilot-instructions.md` found in repo.

When modifying files keep changes minimal, run linters, and test the site locally before submitting changes.