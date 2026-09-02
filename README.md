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

### Claude Code

Claude Code discovers skills from a `skills/` directory at the root of your project, or from `~/.claude/skills/` for skills you want available in every project.

```
# Project-level (just this project)
<your-project>/
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

Clone or copy the `skills/` folder from this repo into either location. Claude Code will pick up the skills automatically — no configuration needed. See the [Claude Code skills docs](https://code.claude.com/docs/en/skills) for details.

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

Codex discovers skills from a `skills/` directory at the root of your project, or from `~/.codex/skills/` for global skills.

```
# Project-level
<your-project>/
└── skills/
    ├── edt-empathy-map/
    │   └── SKILL.md
    └── ...

# Global
~/.codex/skills/
├── edt-empathy-map/
│   └── SKILL.md
└── ...
```

Copy the skills you want into either location and Codex will pick them up automatically. See the [Codex skills docs](https://developers.openai.com/codex/skills/) for details.

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

The Agent Skills format is an open standard supported by a growing list of tools — see the [Client Showcase](https://agentskills.io/clients) for the full list (includes GitHub Copilot, VS Code, Gemini CLI, Goose, and many more). Each client typically looks for a `skills/` directory at the project root or a global `~.<client>/skills/` directory. Check the docs for your specific agent.

### No coding agent? (claude.ai or chatgpt.com)

If you're using a web chat interface without automatic skill discovery, you can still use these skills manually:

1. Open the `SKILL.md` file for the activity you want to run
2. Copy its full contents
3. Paste it into the conversation before your first prompt (or into a Project's system instructions for Claude, or a custom GPT's instructions field for ChatGPT)

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
