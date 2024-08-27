All changes included in 1.6:

## `quarto inspect`

- ([#10039](https://github.com/quarto-dev/quarto-cli/issues/10039)): `quarto inspect` properly handles `!expr` tag in metadata.
- ([#10188](https://github.com/quarto-dev/quarto-cli/issues/10188)): `quarto inspect` properly resolves includes across subdirectory boundaries.

## Lua Filters

- ([#10004](https://github.com/quarto-dev/quarto-cli/issues/10004)): Resolve callout titles, theorem names, and `code-summary` content through `quarto_ast_pipeline()` and `process_shortcodes()`.
- ([#10196](https://github.com/quarto-dev/quarto-cli/issues/10196)): Protect against nil values in `float.caption_long`.
- ([#10328](https://github.com/quarto-dev/quarto-cli/issues/10328)): Interpret subcells as subfloats when subcap
  count matches subcell count.

## `typst` Format

- ([#10168](https://github.com/quarto-dev/quarto-cli/issues/10168)): Support `csl` bibliography style.
- ([#10181](https://github.com/quarto-dev/quarto-cli/issues/10181)): Remove workaround for image dimensions which is no longer necessary and mishandled image paths with spaces.
- ([#10217](https://github.com/quarto-dev/quarto-cli/issues/10217)): Explicitly compute units for image dimensions in `typst` format when they're not given.
- ([#10212](https://github.com/quarto-dev/quarto-cli/issues/10212)): Moves Pandoc variables to the function declaration for the default template.

## `latex` and `pdf` Format

- ([#10291](https://github.com/quarto-dev/quarto-cli/issues/10291)): Several improvement regarding Quarto LaTeX engine behavior for missing hyphenation log message:
  - `latex-auto-install: false` now correctly opt out any missing hyphenation packages detection and installation. Only a warning will be thrown if any detected in the log.
  - For default behavior (`latex-auto-install: true`), detection is still happening and missing packages are installed automatically. If it fails, Quarto does not fail anymore as PDF rendering as succeeded already. Only a warning will be thrown to log the installation failure.
  - Log message about hyphenation package missing for `chinese` or `chinese-hans` languages are now ignored.

## Engines

### `julia`

- ([#10225](https://github.com/quarto-dev/quarto-cli/issues/10225)): Handle API change in `is_manifest_current` in Julia 1.11.

### `jupyter`

- ([#9134](https://github.com/quarto-dev/quarto-cli/issues/9134)): Add proper fix for `multiprocessing` in notebooks with the Python kernel.

## Other Fixes and Improvements

- ([#10162](https://github.com/quarto-dev/quarto-cli/issues/10162)): Use Edge on `macOS` as a Chromium browser when available.
- ([#10235](https://github.com/quarto-dev/quarto-cli/issues/10235)): Configure the CI schedule trigger to activate exclusively for the upstream repository.
- ([#10295](https://github.com/quarto-dev/quarto-cli/issues/10235)): Fix regression to return error status to shell when `CommandError` is thrown.
- ([#10332](https://github.com/quarto-dev/quarto-cli/issues/10332)): Use `exitWithCleanup` whenever possible instead of `Deno.exit` to clean up temporary resources.
- ([#10334](https://github.com/quarto-dev/quarto-cli/issues/10334)): Fix `author` field rendered incorrectly in dashboards when multiple authors are present.
- ([#10552](https://github.com/quarto-dev/quarto-cli/issues/10552)): Add `contents` shortcode.
