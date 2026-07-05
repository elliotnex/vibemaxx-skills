# VibeMaxx Skills

The public skills catalog for [VibeMaxx](https://github.com/elliotskise/vibemaxx). The desktop app's Skills panel reads this repo directly — no app update is needed to publish new skills.

Skills are focused instruction sets that make coding agents better at a specific job: building features, hunting bugs, reviewing security, and more. Installing one from the Skills panel drops it into your project's `.claude/skills/` directory, where agent CLIs pick it up automatically.

## Repo layout

```
catalog.json            The index the Skills panel lists — id, name, description, category, tags
skills/<id>/SKILL.md    The skill itself (frontmatter + instructions)
skills/<id>/...         Optional supporting files, installed alongside SKILL.md
```

## Contributing a skill

1. Create `skills/<your-skill-id>/SKILL.md` with frontmatter:

   ```markdown
   ---
   name: your-skill-id
   description: One line on what the skill does and when to use it.
   ---

   # Your Skill

   Instructions for the agent...
   ```

2. Add a matching entry to `catalog.json`. The `id` must match the directory name (lowercase letters, digits, hyphens).
3. Open a pull request.

Keep skills focused: one job per skill, concrete instructions over vibes, and no secrets or machine-specific paths.
