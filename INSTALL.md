# Installation Quick Reference

Replace `<OWNER>/<REPO>` with the GitHub repository containing this directory.

## Claude Code

```bash
claude plugin marketplace add <OWNER>/<REPO>
claude plugin install django-expert@django-expert
claude plugin list
claude plugin details django-expert
```

## GitHub Copilot CLI — marketplace

```bash
copilot plugin marketplace add <OWNER>/<REPO>
copilot plugin install django-expert@django-expert
copilot plugin list
copilot plugin details django-expert
```

## GitHub Copilot CLI — direct plugin path

```bash
copilot plugin install <OWNER>/<REPO>:plugins/django-expert
```

## GitHub Copilot CLI — local path

```bash
copilot plugin install ./plugins/django-expert
```
