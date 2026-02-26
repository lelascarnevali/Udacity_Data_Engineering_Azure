# GitHub Copilot — Repository Instructions

## Project Summary

`Udacity_Data_Engineer` is a hands-on learning repository for Data Engineering with Azure, Apache Spark, and NoSQL.
**Stack:** macOS · VS Code · Jupyter Notebooks · Python 3 (.venv) · Azure · Apache Spark

> **Multi-repo workspace:** This repository is one of three open simultaneously in VS Code:
> - `Udacity_Agentic_AI` — LLM reasoning, planning, agentic workflows
> - `Udacity_Generative_AI` — Foundation models, LLMs, GenAI solutions
> - `Udacity_Data_Engineer` — **(this repo)** Data Engineering with Azure, Spark, and NoSQL
>
> Skills and memory are always read from **this repo's** `.github/skills/` and `.github/agents/memory/`.

## Repository Layout

```
AGENTS.md                           ← Single source of truth for all AI agents
CLAUDE.md                           ← Claude Code tool adapter
.github/
  copilot-instructions.md           ← This file (Copilot instructions + tool adapter)
  agents/plan.agent.md              ← Custom "Plan" agent
  instructions/python-env.instructions.md  ← Python-specific rules (auto-applied)
  prompts/documentation_workflow.prompt.md ← /documentation_workflow slash command
  skills/                           ← Agent skills (agent-memory, git-commit, tech-writer, …)
  agents/memory/                    ← Persistent memory files
Azure-Data-Lake-Databricks/
Azure-Data-Warehouse-Synapse/
Data-Integration-Pipelines/
Data-Modeling-Apache-Cassandra/
Spark Lessons/
```

## Critical Rules (from AGENTS.md)

1. **Always start every task** with Step 0: read `.github/skills/README.md` and `.github/agents/memory/README.md`.
2. **Never use terminal commands** to create or edit files — use native file tools only.
3. **Language policy:** docs/ → Portuguese (pt-BR) | code/comments → English | chat → Portuguese (pt-BR).
4. **Commits** → always follow `.github/skills/git-commit/SKILL.md` or use `/commit` slash command.
5. **Python env** → `.venv/` at workspace root (`source .venv/bin/activate`).

## Workflow Architecture (quick reference)

| Want to… | Use |
|---|---|
| Apply rules to all requests | `copilot-instructions.md` |
| Apply rules to specific files | `instructions/*.instructions.md` |
| Create a `/slash-command` | `prompts/*.prompt.md` |
| Create a specialized AI persona | `agents/*.agent.md` |
| Auto-load a reusable procedure | `skills/<name>/SKILL.md` |
| Record a session learning | `agents/memory/*.md` |

> Full reference: `.github/instructions/workflow-architecture.instructions.md`

## VS Code Tool Mapping

> Full instructions are in [`AGENTS.md`](../AGENTS.md). Use the mappings below for VS Code / Copilot equivalents.

| Generic reference in AGENTS.md | VS Code / Copilot tool |
|---|---|
| Native task management tool | `manage_todo_list` |
| Native file creation tool | `create_file` |
| Native file editing tool | `replace_string_in_file` |
| Native file reading tool | `read_file` |
| Native notebook editing tool | `edit_notebook_file` |
| Native file search tool | `list_dir` / `file_search` |
| Native content search tool | `grep_search` |
| Shell / terminal commands | `run_in_terminal` |

## Skills Integration

Skills are in `.github/skills/`. See `.github/skills/README.md` for the full catalog.
