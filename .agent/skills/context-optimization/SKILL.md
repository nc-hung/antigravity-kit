---
name: context-optimization
description: Practical context management and conversation compression for better token efficiency.
---

# Context Optimization Skill

## Overview
This skill focuses on managing long conversations by periodically "compacting" the context. This involves summarizing the conversation so far, capturing key decisions, and resetting the detailed window to save tokens and maintain model focus.

## Key Techniques
1. **Periodic Summarization**: Summarize the goals, progress, and remaining tasks.
2. **Fact Capture**: Extract key architecture decisions, learned context, and project status.
3. **Redundant Message Pruning**: Identify and skip redundant steps or errors.
4. **Knowledge Update**: Use `CLAUDE.md` to store the distilled knowledge.

## Compacting Process
1. **Analyze History**: Review recent messages to identify the key threads.
2. **Summarize**: Create a concise summary (max 300 words) of the conversation.
3. **Capture Deltas**: Identify what has changed in the project state (files, architecture, features).
4. **Reset Context**: Inform the user that the context is being compacted.
5. **Update CLAUDE.md**: Save the new facts/decisions to the persistent memory.

## Guidelines
- **Don't Lose Detail**: Only compact when the window is nearing its limit.
- **Explain to User**: Always tell the user *why* compacting is happening.
- **Maintain Current Goal**: Ensure the *next immediately actionable* task is clear after compacting.

## When to use this skill
- When the conversation exceeds ~40-50 messages.
- When the model starts making quality errors or forgetting recent context.
- When switching between very different tasks in the same session.
- When the user explicitly asks for "compact history" or "summarize so far".
