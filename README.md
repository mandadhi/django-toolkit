# Django Expert Plugin

Production-grade Django and Django REST Framework engineering expertise for Claude Code and GitHub Copilot CLI.

This repository follows the marketplace/plugin layout used by TechWave Toolkit: a marketplace manifest at `.claude-plugin/marketplace.json`, a plugin under `plugins/django-expert/`, and the canonical skill under `plugins/django-expert/skills/django-expert/`.

## What it provides

- Full SDLC guidance: research → requirements → architecture → implementation → testing → security → performance → release → deployment → operations.
- Mandatory repository inspection before changes.
- Version-aware Django guidance.
- On-demand reference loading instead of putting the entire knowledge base into the base prompt.
- Practical BAD → GOOD → WHY → WHEN NOT TO USE guidance in the reference library.
- Django ORM, views/URLs, DRF, security, testing, performance, production deployment, and worked examples.
- Evaluation suite and scoring rubric.

## Install from GitHub

After pushing this repository to GitHub as `<OWNER>/<REPO>`:

### Claude Code

```bash
claude plugin marketplace add <OWNER>/<REPO>
claude plugin install django-expert@django-expert
```

Verify:

```bash
claude plugin list
claude plugin details django-expert
```

### GitHub Copilot CLI

```bash
copilot plugin marketplace add <OWNER>/<REPO>
copilot plugin install django-expert@django-expert
```

Verify:

```bash
copilot plugin list
copilot plugin details django-expert
```

### Direct Copilot GitHub-subdirectory install

Copilot also supports installing a plugin directly from a subdirectory in a GitHub repository:

```bash
copilot plugin install <OWNER>/<REPO>:plugins/django-expert
```

### Direct local installation

From a clone of this repository:

```bash
copilot plugin install ./plugins/django-expert
```

For Claude Code, prefer the marketplace flow above so the plugin is registered and versioned through the marketplace.

## Use the skill

The skill name is `django-expert`.

Copilot can automatically select it based on the skill description, or you can explicitly request it with `/django-expert` where supported.

Claude Code discovers the skill from the installed plugin and can invoke it as `/django-expert`.

## Repository layout

```text
.
├── .claude-plugin/
│   └── marketplace.json
├── plugins/
│   └── django-expert/
│       ├── plugin.json
│       └── skills/
│           └── django-expert/
│               ├── SKILL.md
│               ├── references/
│               └── evals/
└── README.md
```

## Updating

After publishing a new version, update the version in both:

- `.claude-plugin/marketplace.json`
- `plugins/django-expert/plugin.json`

Then refresh the marketplace and update/reinstall the plugin in the client.

## Source of truth

The canonical skill is:

`plugins/django-expert/skills/django-expert/SKILL.md`

The reference files are loaded by the skill on demand. Do not maintain separate Copilot and Claude copies of the Django knowledge unless a platform-specific adapter is genuinely required.
