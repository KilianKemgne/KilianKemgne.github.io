# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Development commands

This project is a Hugo Blox Academic CV starter site using Hugo modules and pnpm.

- **Install dependencies**
  - `pnpm install`
- **Run local dev server** (auto-rebuilds on changes)
  - `pnpm dev`
  - This runs `hugo server --disableFastRender`.
- **Build static site for production**
  - `pnpm build`
  - This runs `hugo --minify` and outputs the static site (by default to `public/`).
- **Direct Hugo usage** (if you prefer not to use package.json scripts)
  - `hugo server --disableFastRender`
  - `hugo --minify`
- **Tooling requirements**
  - Hugo **extended** must be installed locally (see the note in `README.md`).
  - Go is required for Hugo modules (see `go.mod`).
  - The repo is configured to use `pnpm` (`packageManager` in `package.json`). Prefer `pnpm` over `npm`/`yarn` unless explicitly requested.
- **Tests**
  - There is currently **no test suite or test script** defined (no `test` script in `package.json`), so there are no test commands to run.

If you add new scripts (e.g., for tests, linting, or deployment), update this section with the exact commands.

## High-level architecture

This is a content-driven static site built with **Hugo Blox Builder** (Academic CV template) on top of Hugo.

### Top-level structure

- `content/`
  - All site content is authored in Markdown.
  - The homepage and its sections are configured in `content/_index.md` using Hugo Blox "blocks" (e.g., `resume-biography-3`, `collection`, `cta-card`).
  - Subfolders (`blog/`, `courses/`, `events/`, `projects/`, `publications/`, etc.) define listing pages and individual items for those sections.
  - `content/authors/_index.md` controls how author profile pages are built (currently set to not render individual author pages).
- `assets/`
  - `assets/media/` holds image assets used across the site (e.g., author photos, icons, background images).
  - This folder is also where Tailwind/Hugo Blox assets are mounted via Hugo modules (see `config/_default/module.yaml`).
- `static/`
  - Files served as-is, such as downloads.
  - `static/uploads/` contains downloadable assets referenced from content, for example `uploads/resume.pdf` used by the "Download CV" button on the homepage.
- `config/_default/`
  - Central site configuration broken into multiple YAML files:
    - `hugo.yaml`: core Hugo settings (base URL, languages, output formats, taxonomies, etc.).
    - `params.yaml`: Hugo Blox–specific configuration (identity, theme, layout, SEO, analytics, comments, etc.).
    - `menus.yaml`: main navigation structure (labels, URLs, weights for ordering).
    - `languages.yaml`: language-related configuration (multilingual support).
    - `module.yaml`: Hugo module imports and mount points for Blox plugins and local `layouts`/`assets`.
- `layouts/`
  - Custom layout overrides and partials that extend the upstream Hugo Blox theme.
  - Currently includes `_partials/hooks/head-end/github-button.html`, which injects the GitHub buttons script into the `<head>` via Hugo's hook system.
- `go.mod`
  - Defines the Hugo module for this site and pins versions of the imported Hugo Blox modules (`blox-plugin-netlify`, `blox-tailwind`).
- `package.json`
  - Declares the JavaScript-side dependencies (Tailwind v4 CLI, typography plugin, Preact) and npm scripts (`dev`, `build`).

### How the pieces fit together

- **Content model**
  - Content in `content/` (e.g., publications, events, courses, blog posts) is written as Markdown with front matter fields understood by Hugo Blox.
  - The homepage (`content/_index.md`) aggregates and displays subsets of that content through block definitions (e.g., collections that query `publications/`, `events/`, or `blog/`).
- **Theming & configuration**
  - Visual identity and behavior (site name, theme mode, typography, layout density, SEO options, analytics, comments, etc.) are configured in `config/_default/params.yaml` under the `hugoblox:` key.
  - Global site behavior (languages, pagination, taxonomies, output formats, robots.txt, etc.) is configured in `config/_default/hugo.yaml`.
  - Navigation links in the header are defined in `config/_default/menus.yaml` and map to either top-level pages (`experience/`, `projects/`, `courses/`) or anchors on the homepage (e.g., `/#papers`, `/#talks`).
- **Hugo modules and assets**
  - `config/_default/module.yaml` imports Hugo Blox plugins and mounts their layouts and CSS into this project.
  - `go.mod` pins the module versions to specific SHAs, ensuring consistent builds across environments.
  - Tailwind CLI and related tooling are managed via `package.json` and run as part of the Hugo Blox pipeline; you generally don't run `tailwindcss` directly—Hugo Blox orchestrates it when you run `hugo`/`pnpm dev`/`pnpm build`.
- **Customization surface**
  - For **content changes** (text, structure of sections, which publications/talks appear), edit files under `content/`.
  - For **site-wide configuration** (name, branding, navigation, analytics, SEO), edit the YAML files in `config/_default/`.
  - For **layout-level overrides** (injecting custom HTML or scripts, overriding blocks), add or modify templates under `layouts/`, using Hugo's standard lookup rules and hook partials (as demonstrated by `layouts/_partials/hooks/head-end/github-button.html`).

## Guidelines for Warp when editing this repo

- Prefer using the existing `pnpm` scripts (`pnpm dev`, `pnpm build`) instead of invoking Hugo in ad-hoc ways, unless the user explicitly requests otherwise.
- When changing the site's structure or navigation, ensure consistency between:
  - `content/_index.md` block definitions (for homepage sections), and
  - `config/_default/menus.yaml` navigation entries (so menu items point to valid sections or pages).
- When editing YAML config files under `config/_default/`, preserve comments and existing structure where possible to maintain readability and alignment with Hugo Blox documentation.
- When adding new content types or pages, follow the Hugo file naming convention and structure described in `content/courses/hugo-blox/guide/project-structure.md` (e.g., use `_index.md` for section/list pages, and either `TITLE.md` or `TITLE/index.md` for regular pages).