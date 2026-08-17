# Agentic Skills

A small, growing collection of **agent skills** that I build and use in my daily work.

A skill is just a Markdown file that tells an AI coding agent *how I want a certain kind of task done* — my checklist, my conventions, my workflow. Instead of re-explaining the same rules in every chat, the agent reads the skill and follows it. The goal is simple: get the maximum result out of the agent, consistently.

---

## Available skills

| Skill | What it does |
|---|---|
| [agent-design](skills/agent-design/SKILL.md) | Plan an AI agent before writing code — goal, tools, state, control flow, and failure handling. |
| [code-review](skills/code-review/SKILL.md) | Review code changes against my personal checklist for correctness, security, and style. |
| [ui-design](skills/ui-design/SKILL.md) | A strict design-first frontend workflow — understand, research, design system, one page, approval, then scale. |

---

## Repository layout

```
.
├── skills/                  # one folder per skill
│   ├── agent-design/
│   │   └── SKILL.md
│   ├── code-review/
│   │   └── SKILL.md
│   └── ui-design/
│       └── SKILL.md
├── templates/
│   └── SKILL-template.md    # starting point for a new skill
├── CONTRIBUTING.md
├── LICENSE
└── README.md
```

Each skill lives in its own folder with a `SKILL.md` file. If a skill needs extra material (checklists, examples, longer docs), it goes in a `references/` folder next to the `SKILL.md`.

---

## How to use these skills

Clone the repo and copy the skills you want into your agent's skills directory:

```bash
git clone https://github.com/alihassan-coder/Agentic-Skills.git
cd Agentic-Skills

# example: use it with Claude Code
mkdir -p ~/.claude/skills
cp -r skills/code-review ~/.claude/skills/
```

You can also just open a `SKILL.md`, copy the content, and paste it into whatever agent or prompt system you use. Nothing here is tool-specific — it is plain Markdown.

---

## Anatomy of a skill

Every skill follows the same shape (see [templates/SKILL-template.md](templates/SKILL-template.md)):

```markdown
---
name: skill-name-in-kebab-case
description: One clear sentence saying WHAT this skill does and WHEN to use it.
---

# Skill Title

## When to use
## Instructions
## Conventions / Rules
## Examples (optional)
## References (optional)
```

The `description` line matters most — it is how the agent decides whether to pick the skill at all, so it should be specific about both the *what* and the *when*.

---

## Writing a good skill

A few rules I try to follow:

- **Be specific, not general.** "When creating a new FastAPI endpoint" beats "when coding".
- **Write instructions, not essays.** Short, numbered, actionable steps.
- **Encode the conventions the agent can't guess** — naming, file placement, patterns you actually use.
- **Say what NOT to do.** Negative rules are often more useful than positive ones.
- **Keep it short enough to stay in context.** If a skill grows large, split the detail into `references/`.

---

## Roadmap

- [ ] Add a design-doc template under `skills/agent-design/references/`
- [ ] Add stack-specific review checks (Next.js, FastAPI, LangGraph)
- [ ] Add more skills: testing, debugging, API design, documentation
- [ ] Improve the existing skills as I learn what actually breaks in practice

---

## Contributing

I'd love to get your thoughts and your improvement ideas. Issues, corrections, and new skills are all welcome — see [CONTRIBUTING.md](CONTRIBUTING.md) for how to get started.

---

## License

Released under the [MIT License](LICENSE). Use these skills freely, change them to fit your own workflow.
