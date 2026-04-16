# Phase 0.01 — Project Setup, Tools, and Documentation Pipeline

## Who this guide is for

This tutorial documents a complete pipeline for building a real-world-scale open world environment and game in Unreal Engine 5, using free and low-cost tools. Every step is documented at explicit, instruction-level detail. No prior experience with GIS, Houdini, or Unreal Engine pipeline setup is assumed.

The project covers the Gold Coast LGA, Queensland, Australia at 1:1 real-world scale — 36km x 36km — and progresses from raw elevation data through to packaged game builds across six gameplay modes.

---

## A note on AI-assisted development

This project was planned and executed with AI assistance as a core part of the workflow.

| Agent | Role |
|---|---|
| ACB — Claude (Anthropic) | Master planner, spec keeper, all architecture decisions |
| ACA — Claude (Anthropic) | Lead programmer, script generation |
| GCB — Gemini AI Studio Pro | Research, documentation retrieval |
| OGA — ChatGPT-4o | Cross-reference and fallback |
| PPA — Perplexity Pro | Fast version and API lookup |

**Critical warning from our own experience:**

Do not allow any AI agent to direct pipeline decisions without independently verifying the output against official documentation or community-confirmed examples. We experienced a significant pipeline failure when an AI agent planned a heightmap tiling method incompatible with the current UE5 landscape import system. The cost was a full reprocess of 81 heightmap tiles.

The rule enforced throughout this project: AI recommends. User verifies against official docs or community examples. Then executes. This is non-negotiable and is documented here so readers can apply the same discipline to their own AI-assisted pipelines.

---

## Documentation system

### Platform architecture

This project uses a four-platform documentation architecture with a single entry point and automatic propagation to all output platforms.

**GitBook** is the primary editing surface and public-facing tutorial site. All content is written or pasted here. GitBook maintains bidirectional sync with the project GitHub repository — every save in GitBook commits to GitHub automatically, and every GitHub commit updates GitBook immediately.

**GitHub** is the single source of truth for all scripts, configuration files, and documentation. It stores every Python script, QGIS model, and documentation file produced by this project. All other platforms receive content from GitHub.

**Confluence** receives content automatically via the GitHub Markdown Sync application, which watches the GitHub repository and updates mapped Confluence pages on every commit. No manual action is required after initial setup.

**Notion** connects to GitHub via Notion's native GitHub integration, which embeds live-synced GitHub file content directly into Notion pages. The embedded view updates automatically when GitHub content changes, providing a clean readable preview of all tutorial content throughout the project with no manual sync effort. If a fully editable native Notion version is required, content can be pasted directly at any time.

### Update flow — one action, four platforms

```
Claude produces updated content
        |
        v
Paste into GitBook visual editor  <-- your one action per update
        |
        |-- auto --> GitHub repository
                          |
                          |-- auto --> GitBook published site
                          |-- auto --> Confluence (GitHub Markdown Sync)
                          |-- auto --> Notion (native GitHub embed)
```

### Alternative sync options for other users

For users who prefer not to use GitBook as the editing surface, automation platforms such as N8N (self-hosted, free) or Zapier (subscription) can watch a GitHub repository and push content to Notion or other platforms on commit. These tools require a Markdown-to-Notion block conversion step which can be fragile on complex formatting. The GitBook native sync approach used in this project is simpler, more reliable, and requires no additional tooling or cost.

---

## Project management

### Platform

Jira Software free tier is used for all task tracking with a Kanban board — no sprint planning, no velocity tracking, no ceremony. The board has four columns: To Do, In Progress, Blocked, Done. All tickets are pre-populated before execution. The user reads, verifies, edits if needed, and moves cards.

### Ticket hierarchy

```
Initiative  — Major project phase grouping
  Epic      — Deliverable within a phase
    Story   — User-facing outcome or feature
      Task  — Specific technical action
      Bug   — Confirmed failure requiring fix
```

### Custom tracking fields

Every ticket contains:
- Planned story points — set at ticket creation
- Actual time in hours — filled on ticket close
- What changed — one sentence
- Root cause — one sentence
- Future advice — one sentence
- AI agent used — dropdown

Story points use Fibonacci scale (1, 2, 3, 5, 8, 13). Initial estimates set at plan stage, updated when method changes or execution fails.

---

## Asset ownership and licensing

All Unreal Engine assets used in this project are owned by the project author, obtained through Epic Games Fab marketplace as permanent purchases or during free monthly promotions. The Third Person Shooter Kit v2.2 by Marcin Matuszczyk is the only core asset that was purchased outright. Users following this tutorial may substitute their own shooter framework or purchase the same kit.

All pipeline software (QGIS, Python, Houdini Apprentice, Blender, GIMP) is free. Where a paid alternative is used for comparison (Houdini Indie), both free and paid methods are documented in parallel with clear fork points indicating where the free method reaches its limits.

---

## Build and test methodology

Every asset follows an independent validation pipeline before integration into the main project:

```
Step 1 — New project with asset in highest compatible UE version
          Package build, test Windows executable, document result

Step 2 — If older UE version, open copy in 5.7 to upgrade
          Package build in 5.7, document result and fixes required

Step 3 — Migrate validated asset into GASP testing project
          Package build, test with GASP controller, document result

Step 4 — Migrate into City Sample project as separate level
          Package build, test in isolation, document result

Step 5 — Integrate with City Sample level
          Full integration package build, document result
```

City Sample is the core and heaviest base. All assets must pass independent validation before entering it. The GASP Animation Sample project serves as the primary testing environment — lighter than City Sample, ships with working game modes, and allows runtime testing of character and controller behaviour in a clean environment.

This process is expected to run at least twice during development to account for major asset updates. If a core asset such as City Sample receives a significant update, the process repeats from a new base project with migration attempted before committing to a full rebuild.

---

## Git structure

Single Git repository. All modes and development tracks exist within the same repository, separated by level, plugin configuration, and feature toggle. Branches are created for significant integration milestones where a stable main must be preserved — specifically when integrating the Lyra multiplayer framework (Mode 5) and when forking the UEFN-conforming version (Mode 6). All other development occurs on main or short-lived feature branches merged on validation.
