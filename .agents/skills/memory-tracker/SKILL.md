---
name: memory-tracker
description: Maintains project context so the AI doesn't forget important decisions, architecture, and state across long conversations or multiple sessions.
---

# Memory Tracker Guidelines

As an AI coding agent, your context window is limited, and you will eventually forget decisions made early in a long project. 
To prevent this, you must act as your own memory tracker.

## 1. Create and Maintain a CONTEXT.md
If the project does not have a `CONTEXT.md` (or `MEMORY.md`) file, create one in the root directory. 

This file MUST be kept extremely short and punchy. Do not write essays. Use bullet points.
It should contain:
- **Project Goal**: 1-2 sentences explaining what the app does.
- **Tech Stack**: E.g., React, Vite, Tailwind, Supabase, Python, FastAPI.
- **Key Architecture Decisions**: E.g., "Using localstorage for state", "No database, just JSON files".
- **Current State**: E.g., "Auth is done. Working on the dashboard UI."

## 2. Update Context Automatically
- Whenever you finish a **Medium** or **Large** task, or make a significant architectural decision, silently update `CONTEXT.md` to reflect the new reality.
- Do not ask the user for permission to update the context file. Just do it as part of your "Done" routine.

## 3. Read Context First
- Whenever you start working in a repository that has a `CONTEXT.md` file, silently read it first (using your file reading tools) before you start planning or writing code.
- Treat `CONTEXT.md` as the ultimate ground truth for the project's direction.

*When this skill is active, ensure `CONTEXT.md` is always up-to-date and reflects the current state of the project.*
