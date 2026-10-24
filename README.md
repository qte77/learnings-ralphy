# learnings-ralphy

> Self-improvement offspring of the [ralph-loop template](https://github.com/qte77/ralph-loop-cc-tdd-wt-vibe-kanban-template): distills learnings from our own repos and agent sessions into tested improvements for the template.

[![License](https://img.shields.io/badge/license-Apache--2.0-58f4c2.svg)](LICENSE)
[![Ralphy Weekly Run](https://github.com/qte77/learnings-ralphy/actions/workflows/ralphy-weekly.yaml/badge.svg)](https://github.com/qte77/learnings-ralphy/actions/workflows/ralphy-weekly.yaml)

## Status

**Not yet working end to end.** Every scheduled weekly run has failed, and GitHub has disabled the workflow for
inactivity (last run 2026-08-27). The fixes are tracked in this repo's
[issues](https://github.com/qte77/learnings-ralphy/issues).

## What

- **Purpose:** compound *how we work*. Learnings from our own repos and projects become improvements to the
  ralph-loop template, so every project started from it starts smarter.
- **Feeds:**
  - `AGENT_LEARNINGS.md` / `LEARNINGS.md` across our repos
  - the cross-repo learnings digest in [ai-agents-research](https://github.com/qte77/ai-agents-research)
  - local Claude Code session memory and plans, via [config/compound.env](config/compound.env). These are
    local paths, so they are not available on CI runners
    ([#19](https://github.com/qte77/learnings-ralphy/issues/19)).
- **Target:** the ralph-loop template.
- **Cycle:**
  1. synthesize ([config/prd-generation-prompt.md](config/prd-generation-prompt.md))
  2. PRD
  3. ralph TDD loop
  4. pull request in this repo
- **Feedback path:** this repo never pushes to the template. Worthwhile changes are picked back into the
  template by the owner. The design is in
  [template#32](https://github.com/qte77/ralph-loop-cc-tdd-wt-vibe-kanban-template/issues/32).
- **Sibling:** [research-ralphy](https://github.com/qte77/research-ralphy) does the same for *what's new*
  (external research, papers, best practices).

## How

- **Weekly cycle:** `.github/workflows/ralphy-weekly.yaml`, Thursday 12:00 UTC plus manual dispatch (currently
  disabled, see Status).
- **Locally:** `make ralphy_evolve`, which runs PRD generation, then `ralph_init_loop`, then `ralph_run`.
- **The template is included as the `ralph` git submodule.** How improvements get from here back into the
  template (a submodule or a template copy) is still open in
  [template#32](https://github.com/qte77/ralph-loop-cc-tdd-wt-vibe-kanban-template/issues/32).
- See [AGENTS.md](AGENTS.md) for agent config and conventions.

## Why

Learnings captured in one repo rarely reach the tooling every repo starts from. This repo turns accumulated
learnings into tested changes to the ralph-loop template, so improvements compound across every project built
on it instead of staying in the repo where they were noticed.

## References

- [AGENTS.md](AGENTS.md)
- [ralph-loop template](https://github.com/qte77/ralph-loop-cc-tdd-wt-vibe-kanban-template) and its
  [self-improvement design (#32)](https://github.com/qte77/ralph-loop-cc-tdd-wt-vibe-kanban-template/issues/32)
- [research-ralphy](https://github.com/qte77/research-ralphy)
- [An Open Agentic Coding Harness](https://qte77.github.io/open-agentic-coding-harness/)
- [ai-agents-research](https://github.com/qte77/ai-agents-research)

## License

Apache-2.0 - see [LICENSE](LICENSE).
