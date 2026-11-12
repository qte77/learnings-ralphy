<!-- markdownlint-disable MD024 no-duplicate-heading -->

# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

**Types of changes**: `Added`, `Changed`, `Deprecated`, `Removed`, `Fixed`, `Security`

## [Unreleased]

### Fixed

- `ralphy-weekly.yaml` configures a `github-actions[bot]` git identity before the submodule commit
  (every run failed with `empty ident name`), pins the Claude Code install to `2.1.310`, records the
  template commit in the job summary, and caps the PRD-generation step at `--max-budget-usd 5` with
  `--permission-mode bypassPermissions`, logging `total_cost_usd` to the job summary; the local
  `make ralphy_generate_prd` gets the same flags (#22)
- `ralph_run` and `ralph_init_loop` now run inside the `ralph/` submodule (`make -C ralph`), since
  the included `ralph/Makefile`'s recipes use paths relative to the template's own root, and that
  root is one level deeper here (`ralph/ralph/scripts/...`) than at the superrepo root; same fix in
  `config/prd-generation-prompt.md`, which now points `generate_prd_json.py` at the double-nested
  script with `../docs/PRD.md` so it reads this repo's PRD, not the submodule's own (#22)
- `.scaffolds/contrib.sh`'s `adapter_validate` no longer ends in `|| true`: it now fails when the
  target repo's `make validate`/`make test` fails, and errors clearly when neither target exists,
  instead of silently passing. Added `.scaffolds/contrib.test.sh` (RED-GREEN, no CI wiring yet).
  The template's own `make validate` always exiting 0
  ([template#90](https://github.com/qte77/ralph-loop-cc-tdd-wt-vibe-kanban-template/issues/90)) is a
  separate upstream issue, not fixed here (#22)

### Added

- `CHANGELOG.md` in Keep a Changelog format (#23)

### Changed

- `AGENTS.md` asks for a CHANGELOG entry on non-trivial changes (#23)
- README, `AGENTS.md` and `docs/UserStory.md` retarget the repo to the ralph-loop template as its
  self-improvement offspring and state current status (#21)
- README follows the estate doc-structure canon; `AGENTS.md` marketplace reference fixed (#20)
- Agent config standardized: `AGENTS.md` as single source with `CLAUDE.md` symlink, shared rules,
  plugin marketplace, Dependabot (#16)
- `actions/checkout` bumped from v4 to v7 (#17)
- `.github/dependabot.yml` groups `github-actions` updates into
  `actions-security-updates` and `actions-version-updates` (minor/patch)

### Security

- `actions/checkout` in `ralphy-weekly.yaml` pinned to its full commit SHA; tag refs now fail at
  workflow startup under the repo's Actions allow-list policy
