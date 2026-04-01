---
name: system-diagnostics
description: Diagnostic tools and workflows for agentic workspace health.
---

# System Diagnostics Skill

## Overview
This skill provides a `/doctor` workflow to diagnose common project issues, check the presence and validity of `.agent` directory components, and verify environment health.

## Key Diagnostic Areas
1. **Agent Setup Check**: Check for the existence of `GEMINI.md`, `ARCHITECTURE.md`, agents, skills, and workflows in the `.agent` directory.
2. **Environment Check**: Verify Node/Bun/Python versions are compatible.
3. **Project Setup Check**: Check for necessary files like `package.json`, `tsconfig.json`, `.env.example`, etc.
4. **Tool/Script Check**: Run quick sanity checks for core validation scripts (`checklist.py`, etc.).
5. **Context Check**: Verify if `CLAUDE.md` is present and up-to-date.

## Diagnostic Workflow
1. **Check Files**: Run file system checks to see what is present and what is missing.
2. **Analyze**: Identify potential gaps or misconfigurations.
3. **Report**: Present a categorized checklist (Success, Warning, Critical) to the user.
4. **Fix Proposals**: Offer specific commands or edits to fix issues found.

## Tools to Use
- `list_dir` for directory structure.
- `view_file` for content validation.
- `run_command` for environment and version checks.

## Guidelines
- **Be Concise**: Group related checks together.
- **Actionable**: Don't just report errors; suggest fixes.
- **Progress Documentation**: If major repairs are done, update `CLAUDE.md`.
