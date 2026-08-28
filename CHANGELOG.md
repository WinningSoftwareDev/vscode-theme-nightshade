# Change Log

All notable changes to the "Nightshade" theme will be documented in this file.

Check [Keep a Changelog](http://keepachangelog.com/) for recommendations on how to structure this file.


## [0.1.4] - 2026-08-28

### Changed
- TS imported/aliased bindings (`variable.other.readwrite.alias.ts`) now use lilac (`#e1b5f8`) instead of teal (`#1ba891`), so import names no longer blend into the same-colored `{ }` brackets.

## [0.1.3] - 2026-08-28

### Changed
- Strings (`string.quoted`) now use a slightly darker tone to avoid conflicting with storage types.

## [0.1.2] - 2026-08-28

### Fixed
- Numbers (`constant.numeric`) were too dark to read against the background; lightened from `#2d54c0` to `#5b8cf0` for readable contrast.
- Constants (`constant.language`, `support.constant`, and TS/JS language constants) lightened from `#7b57ff` to `#9d86ff` for readable contrast.

### Changed
- Variables now use a soft lavender (`#d6c7e8`) instead of plain foreground white, so they read as distinct in PHP and TypeScript.
- Object properties now use a light teal (`#9fd6c9`) instead of near-white, making property access stand out from variables and method calls (applied consistently to PHP and TypeScript).
- PHP constructor-promoted properties now use the property color (`#9fd6c9`) so their declaration matches how they're colored everywhere they're used.
- Namespace segments use a solid muted teal-grey (`#6d8f89`) instead of a semi-transparent teal, keeping the receding-prefix look without the muddy transparency.
- Reworked the README to focus on activating and using the theme, with an accurate palette table.
- Added a Preview section and a `screenshots/` folder for theme screenshots.
- `.vscodeignore` now excludes packaged `.vsix` files and the `.idea/` folder so they aren't bundled into the extension.

## [0.1.1] - 2026-08-27

### Fixed
- The trailing (final) empty line number no longer renders as white/grey. Set `editorLineNumber.dimmedForeground` to match the normal line number color.

## [0.1.0] - 2026-08-27

Initial release.

### Added
- Broad, language-agnostic syntax highlighting covering keywords, storage, functions, types, strings, numbers, constants, comments, operators, and variables so JavaScript/TypeScript, Python, Go, Rust, HTML, CSS/SCSS, JSON, and Markdown get the same treatment as PHP.
- Dedicated TypeScript and Vue token rules: class/interface/type/enum names, type annotations, decorators, language constants, object keys, imported/aliased bindings, plus Vue SFC block tags, directives, and interpolation delimiters.
- Markdown styling for headings, bold, italic, links, and code.
- HTML/JSX/XML tag and attribute colors, plus CSS selector and property colors.
- Expanded workbench colors: buttons, inputs, dropdowns, lists, menus, panels, breadcrumbs, peek view, suggest/hover widgets, scrollbars, terminal ANSI palette, bracket pair colorization, selection/find highlights, and git decorations.
