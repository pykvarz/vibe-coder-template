---
name: ship-it-fast
description: Prioritizes the simplest, zero-configuration deployment methods for small to medium projects, avoiding heavy DevOps infrastructure.
---

# Ship It Fast Guidelines

As an AI coding agent helping a Vibe Coder, your goal is to get their code live on the internet as easily as possible. 
Do not suggest enterprise-grade DevOps pipelines for personal projects.

## 1. Favor Zero-Config Platforms
When the user wants to deploy, always default to platforms that connect directly to GitHub and deploy automatically:
- **Static Sites / Frontend (React, Vue, HTML)**: Vercel, Netlify, or GitHub Pages.
- **Fullstack / Backend (Node, Python, Go)**: Render, Railway, or Heroku.
- **Data/AI Apps**: Streamlit Community Cloud or HuggingFace Spaces.

## 2. Avoid Heavy Infrastructure
- Do NOT write Dockerfiles or `docker-compose.yml` unless the user explicitly asks for Docker or the project is too complex for standard PaaS.
- Do NOT suggest AWS (EC2, ECS), Kubernetes, or raw VPS deployments unless explicitly demanded. They require too much maintenance for a single vibe coder.

## 3. Prepare for Deployment
When you know the deployment target (e.g., Vercel or Render), proactively generate the minimal configuration files needed:
- `vercel.json` if necessary.
- `requirements.txt` or `Procfile` for Python backends on Render/Railway.
- Build scripts in `package.json` (e.g., `"build": "vite build"`).

## 4. Provide Simple Instructions
When code is ready to ship, give the user 1-2 click instructions:
"Your code is ready. Just push it to GitHub, go to Vercel.com, click 'Add New', and select this repository. It will deploy automatically."

*When this skill is active, always steer the user towards the path of least resistance for getting their app live.*
