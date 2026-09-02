# IBM Enterprise Design Thinking — Agent Skills

An unofficial collection of [Agent Skills](https://agentskills.io) that bring [IBM Enterprise Design Thinking](https://www.ibm.com/training/enterprise-design-thinking) activities into AI agents. Each skill packages the instructions an agent needs to facilitate or synthesize a specific EDT activity — empathy maps, assumptions and questions, needs statements, and more.

> **Unofficial:** This project is not affiliated with or endorsed by IBM. IBM Enterprise Design Thinking is a trademark of IBM Corp.

---

## Skills in this collection

| Skill | What it does |
|---|---|
| [`edt-empathy-map`](skills/edt-empathy-map/SKILL.md) | Facilitate or synthesize an Empathy Map — maps what a user Says, Does, Thinks, and Feels |
| [`edt-assumptions-and-questions`](skills/edt-assumptions-and-questions/SKILL.md) | Surface team assumptions and open questions, place them on a risk grid, and build an action plan |
| [`edt-needs-statements`](skills/edt-needs-statements/SKILL.md) | Translate user research and observations into outcome-focused Needs Statements |

---

## What is an Agent Skill?

An Agent Skill is an open, standardized format for extending AI agents with specialized knowledge and workflows — defined at [agentskills.io](https://agentskills.io). At its core, a skill is a folder containing a `SKILL.md` file with YAML frontmatter (`name` and `description`) followed by Markdown instructions.

Agents load skills through **progressive disclosure**:

1. **Discovery** — at startup the agent reads only the `name` and `description` of every available skill, giving it a lightweight index of what's available
2. **Activation** — when your prompt matches a skill's description, the agent loads the full `SKILL.md` into context automatically
3. **Execution** — the agent follows the instructions, optionally running bundled scripts or loading referenced files as needed

This means you don't manually paste anything — you put the skills somewhere the agent can find them, and the agent does the rest.

---

## How to use these skills

### claude.ai

Claude has native skill support in its settings. Go to **Settings → Skills → Add → Upload skill**, zip up the skill folder you want, and upload it. Skills uploaded this way are available to you across all conversations automatically.

```
# Zip and upload each skill folder, e.g.:
zip -r edt-empathy-map.zip skills/edt-empathy-map/
# Then upload edt-empathy-map.zip via Settings → Skills → Add → Upload skill
```

Requires a Pro, Max, Team, or Enterprise plan with code execution enabled. See the [claude.ai skills help article](https://support.claude.com/en/articles/12512180-using-skills-in-claude) for details.

### Claude Code

Claude Code discovers skills from `.claude/skills/` at the project root, or from `~/.claude/skills/` for skills available in every project.

```
# Project-level (just this project)
<your-project>/
└── .claude/
    └── skills/
        ├── edt-empathy-map/
        │   └── SKILL.md
        └── edt-assumptions-and-questions/
            └── SKILL.md

# Global (all projects)
~/.claude/skills/
├── edt-empathy-map/
│   └── SKILL.md
└── ...
```

Copy the skill folders into either location. Claude Code picks them up automatically — no configuration needed. See the [Claude Code skills docs](https://code.claude.com/docs/en/skills) for details.

### Cursor

Cursor discovers skills from a `skills/` directory at the root of your project, or from `~/.cursor/skills/` for global skills.

```
# Project-level
<your-project>/
└── skills/
    ├── edt-empathy-map/
    │   └── SKILL.md
    └── edt-needs-statements/
        └── SKILL.md
```

Copy the `skills/` folder from this repo into your project root (or into `~/.cursor/skills/` for global access). Cursor will discover and activate them automatically based on your prompts. See the [Cursor skills docs](https://cursor.com/docs/context/skills) for details.

### ChatGPT / Codex (OpenAI)

ChatGPT and Codex both support native skill discovery. The location depends on how you're using them:

**ChatGPT desktop app** — open the **Skills** panel in the sidebar to browse and manage skills. Codex reads local skills from `.agents/skills/` inside your repo or from `~/.agents/skills/` for personal skills available across all repos.

**Codex CLI** — same locations apply: `.agents/skills/` (repo-scoped) or `~/.agents/skills/` (user-scoped).

```
# Repo-scoped (checked in with your project)
<your-project>/
└── .agents/
    └── skills/
        ├── edt-empathy-map/
        │   └── SKILL.md
        └── edt-assumptions-and-questions/
            └── SKILL.md

# User-scoped (available in all repos)
~/.agents/skills/
├── edt-empathy-map/
│   └── SKILL.md
└── ...
```

Copy the skill folders into either location. Codex detects skill changes automatically. See the [Codex skills docs](https://developers.openai.com/codex/build-skills) for details.

### IBM Bob

Bob discovers skills from a `.bob/skills/` directory inside your project, or from `~/.bob/skills/` for global skills.

```
# Project-level
<your-project>/
└── .bob/
    └── skills/
        ├── edt-empathy-map/
        │   └── SKILL.md
        └── edt-assumptions-and-questions/
            └── SKILL.md

# Global
~/.bob/
└── skills/
    ├── edt-empathy-map/
    │   └── SKILL.md
    └── ...
```

Copy the `skills/` folder from this repo into `.bob/skills/` (or `~/.bob/skills/`). Bob will discover and activate skills automatically based on your prompts and the trigger phrases in each skill's description.

### Other agents

The Agent Skills format is an open standard supported by a growing list of tools — see the [Client Showcase](https://agentskills.io/clients) for the full list (includes GitHub Copilot, VS Code, Gemini CLI, Goose, and many more). Check the docs for your specific agent for its exact discovery path.

---

## About IBM Enterprise Design Thinking

[IBM Enterprise Design Thinking](https://www.ibm.com/training/enterprise-design-thinking) is a framework for applying design thinking at scale across teams and organisations. It provides a set of activities — Empathy Maps, Hills, Sponsor User sessions, Playbacks, and more — that help teams stay focused on user outcomes throughout discovery and delivery.

IBM offers free online courses and certification at the link above.

---

## Contributing

Contributions are welcome. If you have built a skill for another EDT activity, open a pull request with:

- A folder under `skills/` named after the activity (e.g. `skills/edt-hills/`)
- A `SKILL.md` file inside it with valid [Agent Skills frontmatter](https://agentskills.io/specification) (`name`, `description`, and optionally `metadata`) followed by the skill instructions

Keep skill names prefixed with `edt-` so they are easy to identify in an agent's skill library.
