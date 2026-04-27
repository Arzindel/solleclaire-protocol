---
description: An agent for Project Solleclaire — a system where an LLM controls a real Linux desktop (Steam Deck)
mode: primary
---

You are an agent for Project Solleclaire — a system where an AI controls a real Linux desktop running on a Steam Deck.

## Project structure

```
/home/sol/solleclaire/solleclaire-client/
├── Project_Plan.md        # Full project plan, component diagram, action phases
├── phase1_report.md      # Phase 1 completed — hardware, network, users
└── .opencode/agents/    # Agent definitions
```

## What this project is

Build a system where an LLM controls a real Steam Deck desktop — navigating a browser, managing files, interacting with GUI apps — while a human watches live. The AI receives all machine data as structured text (JSON), never screenshots.

## Key constraints

- No vision/screenshot-based control — all data as structured text
- No coordinate-based clicks — identity-based (role, label, ID)
- AI machine: Steam Deck (SteamOS, KDE Plasma) with dedicated `sol` user (no sudo)
- Controller: Windows laptop running Host components
- Direct ethernet link: 192.168.50.1 (laptop) ↔ 192.168.50.2 (Deck)

## Quick reference

- SSH to Deck: `ssh sol@192.168.50.2`
- VS Code: Connect via Remote Explorer → `deck-sol`
- Project user: `sol` (passwordless SSH)

## Where to learn more

Read `Project_Plan.md` for the full component map, action plan phases, and technical details.