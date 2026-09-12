# Minimal Personal AI Coding Template

This is a lightweight, practical template designed for a "vibe coder" — a single creator using AI coding agents (like Antigravity IDE) to build real projects without the overhead of enterprise software development processes.

## What this template is
A minimal operating system for your AI agent. It ensures the AI writes clean code, doesn't overcomplicate things, designs beautiful interfaces, and verifies its own work — all without requiring you to manage complex Jira-like workflows or write exhaustive specifications.

## What skills are included
This template orchestrates three powerful AI skills:
- **[Superpowers](https://github.com/obra/superpowers)**: The core workflow engine. Ensures the AI brainstorms when needed, plans efficiently, debugs systematically, and verifies its work.
- **[Karpathy Guidelines](.agents/skills/karpathy-guidelines/SKILL.md)**: The simplicity enforcer. Prevents the AI from adding unnecessary dependencies, premature abstractions, or overengineered architecture. Keeps changes small and surgical.
- **[Frontend Design](.agents/skills/frontend-design/SKILL.md)**: The UI expert. Activated automatically for UI tasks, ensuring your interfaces look intentional, high-quality, and distinct (no generic AI templates).
- **[Grilling](.agents/skills/grilling/SKILL.md)**: The interviewer. Run `/grill-me` or ask for an interview at the start of a complex project to rapidly extract requirements and align on the goal before coding.
- **[Defensive Coding](.agents/skills/defensive-coding/SKILL.md)**: The security guard. Prevents the AI from generating vulnerable code (like SQL injections) and ensures basic security hygiene.

*(Note: Superpowers is loaded globally from the Antigravity IDE plugin system. The other four are installed directly in `.agents/skills/` for this workspace).*

## How the AI works here
When you ask the AI to do something, it follows this lightweight process:
1. **Understand & Inspect**: It first looks at your existing code to understand the context.
2. **Plan (Only if needed)**: For simple tasks, it just does the work. For medium/large tasks, it creates a short, practical plan.
3. **Implement**: It writes the simplest code possible to solve the problem, applying good UI design if appropriate.
4. **Run & Verify**: It doesn't just guess that the code works. It builds, runs tests, or checks logs before saying it's done.

## How to use
Just talk to your AI agent normally. Examples:
- *"Build a personal finance tracker."*
- *"Add export to CSV."*
- *"Fix this bug."*

The AI will handle the process, relying on the `AGENTS.md` instructions and installed skills to deliver high-quality results quietly and efficiently.
