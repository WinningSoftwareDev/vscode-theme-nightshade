# Change Log

All notable changes to the "Nightshade" theme will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project adheres to
[Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.1.5] - 2026-09-02

### Added
- Dedicated SQL token rules so SQL no longer renders mostly as flat white. Previously nearly everything fell through to the grammar's `keyword.other.sql` catch-all (and bare `source.sql` for identifiers), which had no theme selector. SQL now maps onto the existing Nightshade palette:
  - DDL verbs and general keywords (`CREATE`, `TABLE`, `USE`, `DEFAULT`, `NOT NULL`) use lilac (`#e1b5f8`).
  - Query/DML keywords (`SELECT`, `FROM`, `WHERE`, `JOIN`, `AS`, `ORDER BY`) use blue (`#748bcf`).
  - Data types (`INT`, `VARCHAR`, `TEXT`, `DATETIME`) use cyan (`#00eaff`).
  - Constraints/modifiers (`PRIMARY KEY`, `FOREIGN KEY`, `REFERENCES`, `CONSTRAINT`) use violet (`#9d86ff`).
  - Built-in functions (`COUNT`, `NOW`, `SUBSTRING`) use teal-cyan (`#08dde4`).
  - Created entity names (e.g. the table name after `CREATE TABLE`) use teal (`#1ba891`), qualified `db.table` names use mint (`#9fd6c9`).
  - Numbers, strings, variables (`@var`/`@@global`), and operators reuse their existing language-agnostic colors.

### Note
- The built-in SQL grammar routes a large set of words through a single `keyword.other.sql` catch-all, so some keyword-like data types not in its `storage.type.sql` list may render as keywords rather than types. This is a grammar limitation.

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
