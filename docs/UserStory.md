# Self-Evolving Learnings Implementer

## Problem

Operational patterns and agent learnings accumulate across repos but are not
systematically implemented as improvements. Knowledge compounds in LEARNINGS.md
and AGENT_LEARNINGS.md files but decays without action.

## Users

- ralph-loop template (the target: every project started from it benefits)

## Value

Automatically distill recurring patterns into tested improvements to the
ralph-loop template, so it compounds *how we work*. Design:
[template#32](https://github.com/qte77/ralph-loop-cc-tdd-wt-vibe-kanban-template/issues/32).

## Feeds

- AGENT_LEARNINGS.md / LEARNINGS.md across our repos
- ai-agents-research cross-repo learnings digest
- Local Claude Code session memory and plans via `config/compound.env`. These
  are local paths, not available on CI runners (#19)

## Stories

- Scan all LEARNINGS.md files, extract actionable patterns
- Scan all AGENT_LEARNINGS.md files, extract recurring issues
- Generate PRD with stories for highest-impact template improvements
- Implement via strict TDD (Red-Green-Refactor)
- Write back novel learnings to ai-agents-research

## Constraints

- Must not break existing functionality
- Uni-directional: changes land via pull request in this repo, never pushed to
  the template; the owner picks good changes back (mechanism open in #32)
- Max budget per weekly run: configurable via RALPH_MAX_ITERATIONS
