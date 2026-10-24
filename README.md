# learnings-ralphy

> Self-improvement offspring of the [ralph-loop template](https://github.com/qte77/ralph-loop-cc-tdd-wt-vibe-kanban-template): turns learnings from our own repos into tested improvements for the template.

[![License](https://img.shields.io/badge/license-Apache--2.0-58f4c2.svg)](LICENSE)
[![Ralphy Weekly Run](https://github.com/qte77/learnings-ralphy/actions/workflows/ralphy-weekly.yaml/badge.svg)](https://github.com/qte77/learnings-ralphy/actions/workflows/ralphy-weekly.yaml)

## What

> **Status:** not yet running end to end. The weekly workflow has never succeeded and is disabled; fixes are
> tracked in [issues](https://github.com/qte77/learnings-ralphy/issues).

- Compounds *how we work*: learnings and agent memories from our repos become improvements to the ralph-loop template
- Weekly cycle: synthesize → PRD → ralph TDD loop → pull request in this repo
- Never pushes to the template; good changes are picked back by the owner
- Sibling of [research-ralphy](https://github.com/qte77/research-ralphy), which does the same for external research

## How

```bash
make ralphy_evolve   # generate PRD from learnings, then run the ralph loop
```

Feeds, target and constraints: [docs/UserStory.md](docs/UserStory.md). Agent conventions: [AGENTS.md](AGENTS.md).

## Why

Learnings captured in one repo rarely reach the tooling every repo starts from. Turning them into tested template
changes lets improvements compound across every project built on the template. Design:
[template#32](https://github.com/qte77/ralph-loop-cc-tdd-wt-vibe-kanban-template/issues/32).

## Refs

- [docs/UserStory.md](docs/UserStory.md)
- [AGENTS.md](AGENTS.md)
- [ralph-loop template](https://github.com/qte77/ralph-loop-cc-tdd-wt-vibe-kanban-template)
- [template#32 — self-improvement design](https://github.com/qte77/ralph-loop-cc-tdd-wt-vibe-kanban-template/issues/32)
- [research-ralphy](https://github.com/qte77/research-ralphy)
- [ai-agents-research](https://github.com/qte77/ai-agents-research)
- [An Open Agentic Coding Harness](https://qte77.github.io/open-agentic-coding-harness/)

## License

Apache-2.0 - see [LICENSE](LICENSE).
