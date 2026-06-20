# learnings-ralphy

Self-evolving ralph offspring that distills operational patterns from LEARNINGS.md
and AGENT_LEARNINGS.md across all repos into TDD-implemented improvements.

Uses ralph as a git submodule. Weekly cycle: synthesize -> PRD -> TDD -> writeback.

Targets: cc-utils-plugin skills, polyforge scripts, ralph adapters.
Feeds: compound.env paths, CC session data, ai-agents-research learnings.

## Conventions

- Agent config is AGENTS.md-only; CLAUDE.md is a symlink to this file.
- Claude Code plugins are configured in .claude/settings.json against the
  qte77-claude-code-plugins marketplace; shared rules live in .claude/rules/.
