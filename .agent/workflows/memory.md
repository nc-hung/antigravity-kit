---
description: Manage project-specific knowledge via CLAUDE.md.
---

# /memory Workflow

This workflow uses the `repository-memory` skill to manage persistent project context.

## 🚀 Step 1: Check Current Memory
1. Look for `CLAUDE.md` in the project root.
2. If it exists, summarize its contents to the user.
3. If it doesn't exist, recommend initializing it.

## 📝 Step 2: Initialize or Update Memory
1. Gather core project details (tech stack, architecture, conventions).
2. Use the `repository-memory` template to create or update the file.
3. Include the "Current Status" with today's date.

## 🔄 Step 3: Extract from Conversation
1. Scan the current session for new decisions or "gotchas".
2. Append or update the `Context/Gotchas` section in `CLAUDE.md`.

---

### Executing /memory
**Command:** `AGENT_MANAGE_MEMORY`
- The `project-planner` or `orchestrator` should handle memory management.
- Use this command when wrapping up a session or after major architecture changes.
