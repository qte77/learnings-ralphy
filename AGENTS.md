# learnings-ralphy

Self-evolving ralph offspring that distills operational patterns from LEARNINGS.md
and AGENT_LEARNINGS.md across all repos into TDD-implemented improvements.

Uses ralph as a git submodule. Weekly cycle: synthesize -> PRD -> TDD -> writeback.

Target: the ralph-loop template (self-improvement offspring, template#32).
Feeds, value and constraints: docs/UserStory.md.

## Conventions

- Agent config is AGENTS.md-only; CLAUDE.md is a symlink to this file.
- Claude Code plugins are configured in .claude/settings.json against the
  qte77-claude-code-plugins marketplace; shared rules live in .claude/rules/.
