# PRD Generation Prompt

You are generating a self-improvement PRD from accumulated learnings.

## Pre-synthesis

First run these skills to gather context:

1. /cc-meta:distilling-plan-learnings --time-range 7d
2. /cc-meta:synthesizing-cc-bigpicture --time-range 7d

## Discovery

Read all LEARNINGS.md and AGENT_LEARNINGS.md files across the workspace.
Also read ai-agents-research/docs/learnings/cross-repo-digest.md for patterns.

## Selection

Extract the top 3-5 actionable patterns that are:

- Recurring (appeared in 2+ repos or sessions)
- NOT yet implemented as skills, rules, or code fixes
- High impact (saves tokens, prevents errors, or improves quality)

Cross-reference with existing cc-utils-plugin skills to avoid duplication.

## Output

Generate docs/PRD.md following the ralph PRD template at ralph/docs/templates/prd.md.template.
Each pattern becomes a story with acceptance criteria and target files.
Then run: python ralph/scripts/generate_prd_json.py
