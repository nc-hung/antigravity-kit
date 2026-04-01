---
name: repository-memory
description: Strategic management of project-specific knowledge using CLAUDE.md.
---

# Repository Memory Skill

## Overview
This skill focuses on maintaining a `CLAUDE.md` file at the project root to store persistent knowledge about the project, its structure, conventions, and status. This helps maintain context across different conversation sessions.

## The CLAUDE.md File
The `CLAUDE.md` file should contain:
- **Project Name & Description**: High-level overview.
- **Architecture**: Key components and their relationships.
- **Conventions**: Coding styles, naming, file structure.
- **Development Workflows**: How to build, test, and deploy.
- **Current Status**: Recent major changes or active tasks.
- **Context/Gotchas**: Known issues, specific environment requirements, or non-obvious patterns.

## Guidelines for Agents
1. **Read First**: Always check for `CLAUDE.md` at the start of a session.
2. **Update Strategically**: Update `CLAUDE.md` after significant changes or when new important patterns are established.
3. **Keep it Concise**: Focus on high-value, persistent information. Avoid logging every small change.
4. **Consistency**: Ensure the information in `CLAUDE.md` aligns with `ARCHITECTURE.md` and other documentation.

## Updating Pattern
When updating `CLAUDE.md`, follow this structure:
```markdown
# [Project Name]

## 🛠 Tech Stack
- ...

## 🏗 Architecture
- ...

## 📏 Conventions
- ...

## 🚀 Workflows
- ...

## 📝 Current Status (Last Updated: YYYY-MM-DD)
- ...
```

## When to use this skill
- At the beginning of a project to initialize memory.
- After finishing a major feature or refactor.
- When you discover a project-specific "gotcha" that should be remembered.
- When the user asks "what's the status of the project?".
