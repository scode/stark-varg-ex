# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

An unofficial owner's guide for Stark Varg EX motorcycles, built with mdbook and deployed to GitHub Pages at
https://scode.github.io/stark-varg-ex/

## Commands

```bash
mdbook serve    # Local development server with hot reload
mdbook build    # Build the book to ./book/
dprint check    # Check formatting
dprint fmt      # Fix formatting
```

# Conventional Commits

All commit messages and PR titles must use Conventional Commit format: `<type>: <short summary>`

Allowed types: `feat`, `fix`, `docs`, `perf`, `refactor`, `style`, `test`, `chore`, `ci`, `revert`.

Append `!` after the type for breaking changes (e.g. `feat!: remove legacy endpoint`). Scope is optional.

Rules:

- Type reflects the user-visible effect, not the implementation activity. A bug fix that requires heavy refactoring is
  `fix`, not `refactor`. A new CLI flag is `feat`, not `chore`.
- The summary after the colon is lowercase, imperative mood, no trailing period.
- Keep the first line under 72 characters.

## Structure

- `src/` - mdbook source files (SUMMARY.md defines navigation)
- `book.toml` - mdbook configuration
- `dprint.json` - formatter config (markdown line width: 120, text wrap: always)

## CI/CD

- **CI**: Runs `dprint check` on push/PR to main
- **Deploy**: Builds and deploys to GitHub Pages on push to main
