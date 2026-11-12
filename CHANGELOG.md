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
