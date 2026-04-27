# Self-Evolving Learnings Implementer

## Problem

Operational patterns and agent learnings accumulate across repos but are not
systematically implemented as improvements. Knowledge compounds in LEARNINGS.md
and AGENT_LEARNINGS.md files but decays without action.

## Users

- polyforge-orchestrator (scripts, workflows)
- cc-utils-plugin (skills, rules, hooks)
- ralph-loop-template (adapters, config)

## Value

Automatically distill recurring patterns into concrete improvements:
new skills, better prompts, bug fixes, rule promotions.

## Stories

- Scan all LEARNINGS.md files, extract actionable patterns
- Scan all AGENT_LEARNINGS.md files, extract recurring issues
- Generate PRD with stories for highest-impact improvements
- Implement via strict TDD (Red-Green-Refactor)
- Write back novel learnings to ai-agents-research

## Constraints

- Must not break existing functionality
- Changes via fork+PR workflow (never direct push)
- Max budget per weekly run: configurable via RALPH_MAX_ITERATIONS
