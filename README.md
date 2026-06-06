# Forensic Transcript Analyst Skill

This repository contains the `forensic-transcript-analyst` skill for the Antigravity/Gemini coding assistant, along with its template folder structure.

## Structure
- `skills/forensic-transcript-analyst/SKILL.md`: The main instruction file with YAML frontmatter, doel, kernprincipes, and the required analysis template.
- `skills/forensic-transcript-analyst/scripts/`: Place helper scripts and utilities here.
- `skills/forensic-transcript-analyst/examples/`: Place reference implementations or example transcript analyses here.
- `skills/forensic-transcript-analyst/resources/`: Place templates, schemas, assets, or configuration files here.
- `skills/forensic-transcript-analyst/references/`: Place additional documentation, guidelines, or research papers here.
- `docker-compose.yml`: Local Docker environment configuration for SearxNG and Crawl4AI.
- `infrastructure/README.md`: Detailed startup and management guide for the Docker services.

## How to use
1. Copy the skill configuration folder to your local or global `.gemini/config/skills/` directory (or `.agent/skills/`). The assistant will automatically pick up the triggers defined in the frontmatter of `SKILL.md`.
2. Deploy the local search and crawling infrastructure by running `docker compose up -d` in the root of the project. See [infrastructure/README.md](file:///c:/Users/gewoo/New%20folder%20%2888%29/infrastructure/README.md) for more details.

