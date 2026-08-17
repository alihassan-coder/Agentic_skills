# Contributing

Thanks for stopping by — I'd genuinely love your contributions here.

This repo is a personal collection of agent skills, but the whole point of putting it in the open is that other people write better prompts than I do for things I haven't tried yet. If you have a skill that works well for you, or you spot something in mine that could be sharper, please open an issue or a pull request.

---

## Ways to contribute

**Improve an existing skill.** If a step is vague, an instruction backfires in practice, or a rule is missing, fix it. Explain in the PR *why* the change works better — that context is the valuable part.

**Add a new skill.** Anything you use repeatedly with an agent is a candidate: testing, debugging, API design, database migrations, writing documentation, refactoring.

**Fix typos and wording.** English is not my first language, so clarity fixes are always welcome and never too small.

**Open an issue.** Ideas, questions, and "this didn't work for me" reports are useful even without a patch attached.

---

## Adding a new skill

1. Create a folder under `skills/` named in kebab-case:

   ```
   skills/your-skill-name/SKILL.md
   ```

2. Start from [templates/SKILL-template.md](templates/SKILL-template.md) and keep the same section structure.

3. Fill in the frontmatter carefully:

   ```yaml
   ---
   name: your-skill-name
   description: One sentence saying WHAT the skill does and WHEN the agent should use it.
   ---
   ```

   The `description` is how an agent decides whether to load the skill, so make it specific about both the what and the when.

4. If the skill needs extra material — long checklists, code examples, reference docs — put it in a `references/` folder next to the `SKILL.md` and link to it, rather than making the main file huge.

5. Add your skill to the table in [README.md](README.md).

---

## What makes a good skill

- **Specific triggers.** "When creating a new FastAPI endpoint", not "when coding".
- **Actionable steps.** Short and numbered. The agent should be able to follow them literally.
- **Real conventions.** Encode the things an agent cannot guess: naming, file placement, patterns you actually use.
- **Negative rules too.** "Do NOT do X" is often more useful than another positive instruction.
- **Tested in practice.** Ideally you have actually run the skill with an agent and seen it improve the output.
- **Tool-agnostic.** Plain Markdown, no assumptions about a specific agent product, unless the skill is genuinely about that tool.

---

## Pull request checklist

Before opening a PR, please check:

- [ ] The skill follows the template structure
- [ ] Frontmatter has both `name` (kebab-case, matching the folder) and `description`
- [ ] Spelling and grammar are clean
- [ ] New skills are listed in the README table
- [ ] The PR description explains the problem the change solves

Keep pull requests focused — one skill or one fix per PR is much easier to review than a large mixed change.

---

## Code of conduct

Be kind and be constructive. Critique the skill, not the person who wrote it. That's the whole rule.

---

## License

By contributing, you agree that your contributions are licensed under the [MIT License](LICENSE) that covers this project.
