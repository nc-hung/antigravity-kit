---
description: Environment and agentic workspace diagnostics.
---

# /doctor Workflow

This workflow performs a comprehensive health check on the Antigravity Kit workspace.

## 🚀 Step 1: Core Agent Components Check
1. Check for `GEMINI.md` at root.
2. Check for `ARCHITECTURE.md` in `.agent/`.
3. Check for the following key agents in `.agent/agents/`:
    - `orchestrator.md`
    - `project-planner.md`
    - `frontend-specialist.md` (if applicable)
    - `backend-specialist.md` (if applicable)

## 🛠 Step 2: Environment Health
1. Verify `node -v` (v18+ recommended).
2. Verify `python3 --version` (for master scripts).
3. Check for existence of `.env` or `.env.example`.
4. Verify `package.json` and basic project structure.

## 🧩 Step 3: Skill & Script Sanity Check
1. Check for `scripts/checklist.py` and `scripts/verify_all.py` in `.agent/`.
2. Verify at least one skill folder exists in `.agent/skills/`.
3. Check if `CLAUDE.md` metadata is present (optional but recommended).

## 📊 Step 4: Diagnostic Report
- Present findings using a table or a clear checklist.
- Highlight any **Critical** missing components.
- Suggest next steps for missing or misconfigured items.

---

### Executing /doctor
**Command:** `AGENT_RUN_DIAGNOSTICS`
- The `orchestrator` should lead this diagnostics process.
- The `project-planner` can assist if structural issues are found.

> [!TIP]
> Use `/doctor` at the beginning of a fresh clone or when agents behave unexpectedly.
