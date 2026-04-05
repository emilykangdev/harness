# harness

A personal AI development harness - portable prompts, slash commands, and configs for AI-assisted software engineering.

Inspired by the [software factory](https://runpane.com/blog/building-a-software-factory) philosophy: agents do the building, you do the thinking. This repo is the scaffolding that makes that work.

## philosophy

**Harness engineering** is the time you spend setting up and maintaining the scaffolding that makes AI-assisted development work. Your slash commands, system prompts, project configs, and workflow rules. You're not writing product code - you're building the harness that agents use to write product code.

This repo is meant to be:
- **Portable** - drop into any project
- **Iterative** - improve continuously based on what works
- **Model-aware** - adapt as AI capabilities evolve
- **Personal** - tuned to how *you* think and work

## structure

```
harness/
├── .claude/commands/       # slash commands for Claude Code
│   ├── discussion.md       # collaborative problem exploration
│   ├── plan.md             # structured implementation planning
│   └── implement.md        # execution and verification
├── prompts/                # system prompts and reusable prompt templates
│   ├── codex-system.md     # OpenAI Codex system prompt
│   └── claude-system.md    # Claude system prompt
├── configs/                # reusable project configurations
├── meta/                   # self-improvement system
│   ├── EVOLUTION.md        # changelog of harness iterations
│   └── harness-review.md   # meta-prompt for reviewing the harness
└── CLAUDE.md               # project-level Claude instructions
```

## the pipeline

Every feature follows three phases:

1. **`/discussion`** - have a real conversation about the problem. explore the codebase, ask questions, build shared understanding. no code yet.
2. **`/plan`** - generate a structured implementation plan with pseudocode, file refs, and task ordering. includes a built-in review loop.
3. **`/implement`** - execute the plan. parallelize where possible, verify the build, prep the result.

## usage

1. Copy `.claude/commands/` into your project's `.claude/commands/` directory
2. Copy relevant prompts from `prompts/` and adapt to your project
3. Drop `CLAUDE.md` into your project root (or merge with existing)
4. Use `/discussion`, `/plan`, `/implement` in Claude Code

## improving the harness

The meta-system in `meta/` is designed for periodic self-review. Run the `harness-review.md` prompt against your recent work to identify what's working, what's not, and what should change. Log changes in `EVOLUTION.md` with rationale.

The workflow for improving the workflow is the workflow itself.
