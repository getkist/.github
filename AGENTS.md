# AGENTS.md — .github (org configuration)

GitHub's special `.github` repository for the **getkist** organisation. Its
contents are consumed by GitHub itself, not by any build: `profile/README.md`
renders on [github.com/getkist](https://github.com/getkist), and community
health files placed here become the org-wide default for every repo that does
not define its own.

**No code, no build, no tests, no dependencies.** A change here changes what
visitors and contributors see across the whole organisation, so it is
higher-visibility than the file count suggests.

## What is actually in the repo

| Path | Purpose |
| --- | --- |
| `profile/README.md` | The public org profile page |
| `README.md` | Describes this repo |
| `labels.yml` | Label definitions intended to be synced across all org repos |
| `.vscode/`, `.editorconfig`, `.markdownlint.json`, `cspell.json`, `.pre-commit-config.yaml` | Editor/lint config |

## Known gaps — read before trusting the README

- **`README.md` documents files that do not exist here.** It lists
  `CODE_OF_CONDUCT.md`, `CONTRIBUTING.md`, `SECURITY.md`, `SUPPORT.md`,
  `FUNDING.yml`, `.github/ISSUE_TEMPLATE/` and
  `.github/PULL_REQUEST_TEMPLATE.md` as org defaults. None of them are in the
  repository. So the org has **no** default code of conduct, security policy,
  or issue templates — individual repos fall back to their own or to nothing.
  If asked to "check the org's security policy", the answer is that there
  isn't one, not whatever the README claims.
- For community health files to work as org-wide defaults they must sit at the
  repo root (or in a `.github/` subdirectory of this repo) — not under
  `profile/`.
- `labels.yml` is a definition file only. Nothing in this repo applies it;
  there is no workflow here. Syncing it is a manual/external step.
- Both `README.md` and `profile/README.md` point at **kist.js.org** as the
  documentation site. That domain is now only a redirect — the docs live at
  **www.getkist.com** (`www-getkist-com`). Prefer the canonical URL in new
  text.

## Conventions

- Markdown is centred-HTML-header style (logo image, `<h1 align='center'>`,
  badge row) matching every other getkist README, and ends with the
  "Made with ❤️ by Scape Press" footer.
- The logo is hotlinked from the `brand` repo's `main` branch; badges use the
  brand brown `#5e4d34`. Keep both.
- `profile/README.md` is a shop window — it should describe kist to a newcomer,
  not enumerate repos. The full repo inventory belongs in `.github-private`.

## Related repos (siblings in this workspace)

`.github-private` (internal org profile and strategy docs), `brand` (logo and
palette), `kist` (the product), `www-getkist-com` (the real docs site).
