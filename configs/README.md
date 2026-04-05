# configs/

Reusable project configurations that you want consistent across projects.

## what goes here

- Linting configs (ESLint, Prettier, etc.)
- TypeScript configs (tsconfig presets)
- CI/CD templates (GitHub Actions workflows)
- Editor configs (.editorconfig, VS Code settings)
- Git configs (.gitattributes, hooks)
- Any other config you find yourself copying between projects

## guidelines

- Each config should include a comment header explaining what it does and when to use it
- Prefer minimal configs that can be extended per-project over maximal ones
- When a config evolves, note why in `meta/EVOLUTION.md`
