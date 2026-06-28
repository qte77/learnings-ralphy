# learnings-ralphy

> Self-evolving ralph offspring that distills cross-repo operational patterns into TDD-implemented improvements.

[![License](https://img.shields.io/badge/license-Apache--2.0-58f4c2.svg)](LICENSE)
[![Ralphy Weekly Run](https://github.com/qte77/learnings-ralphy/actions/workflows/ralphy-weekly.yaml/badge.svg)](https://github.com/qte77/learnings-ralphy/actions/workflows/ralphy-weekly.yaml)

## What

- Ingests LEARNINGS.md and AGENT_LEARNINGS.md from across the qte77 estate
- Synthesizes operational patterns into shippable TDD improvements each week
- Targets claude-code-plugins skills, polyforge scripts, and ralph adapters
- Feeds from compound.env paths, Claude Code session data, and ai-agents-research learnings
- Runs the ralph loop: synthesize -> PRD -> TDD -> writeback
- Opens a pull request per weekly run with the generated changes
- Scheduled Thursday 12:00 UTC; supports manual dispatch

## How

Ralph runs as a git submodule. The weekly cycle (synthesize -> PRD -> TDD ->
writeback) is scheduled via `.github/workflows/ralphy-weekly.yaml`. See
[AGENTS.md](AGENTS.md) for full agent config and conventions.

## Why

Manual cross-repo learning capture is lossy and ad-hoc. Patterns discovered in
one repo rarely reach others. This repo automates the distillation cycle: raw
learnings become structured improvements that ship via PR, compounding quality
across the estate without manual intervention.

## References

- [AGENTS.md](AGENTS.md)
- [ralph submodule upstream](https://github.com/qte77/ralph-loop-cc-tdd-wt-vibe-kanban-template)
- [An Open Agentic Coding Harness](https://qte77.github.io/open-agentic-coding-harness/)
- [ai-agents-research](https://github.com/qte77/ai-agents-research)

## License

Apache-2.0 - see [LICENSE](LICENSE).
