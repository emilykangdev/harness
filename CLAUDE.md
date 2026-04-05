# CLAUDE.md

This is the harness repo - a collection of portable prompts, slash commands, and configurations for AI-assisted software engineering.

## rules for working in this repo

- This repo contains *instructions for agents*, not product code. Treat every file as a prompt or config that will be consumed by an AI model.
- When editing slash commands, preserve the structure: context gathering -> human interaction -> output generation.
- When editing prompts, be precise. Vague instructions produce vague results. Write instructions, not aspirations.
- Every change to the harness should be logged in `meta/EVOLUTION.md` with a date and rationale.
- Test changes by actually using them on a real task before committing.

## structure

- `.claude/commands/` - slash commands for the discussion -> plan -> implement pipeline
- `prompts/` - system prompts and reusable prompt templates
- `configs/` - reusable project configurations (linting, CI, etc.)
- `meta/` - self-improvement system (evolution log, review prompts)
