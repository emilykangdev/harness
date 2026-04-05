# prompts/

System prompts and reusable prompt templates for different AI models and use cases.

## organization

- `codex-system.md` - System prompt for OpenAI Codex / ChatGPT Codex
- `claude-system.md` - System prompt for Claude (CLAUDE.md format)
- Add new files as `[model-or-usecase]-[type].md`

## guidelines

- Each prompt should be self-contained and portable
- Include comments explaining *why* specific instructions exist, not just what they are
- Version your prompts - when you make significant changes, note what changed and why in `meta/EVOLUTION.md`
- Test prompts on real tasks before committing

## what makes a good system prompt

1. **Specific over general** - "Use TypeScript strict mode" beats "Write good code"
2. **Rules over suggestions** - "Never use `any` type" beats "Try to avoid `any` type"
3. **Examples over descriptions** - Show the format you want, don't just describe it
4. **Constraints over freedoms** - Tell the model what NOT to do. Models are creative by default; constraints channel that creativity.
5. **Graduated detail** - Put the most important rules first. Models pay more attention to what comes early.
