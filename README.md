# 🛸 USS Hustle: Space Age Hustle Command Center

> *"Floating Through the Cosmos, One Ticket at a Time"*  
> **Lead Digital Agent**: Trill Astro Buzz (T.A.B.)  
> **Organization**: Oneseco Media  
> **Runtime**: React (Vite + TypeScript + Tailwind CSS)  
> **License**: Apache-2.0  

---

```text
       _         _             _   _           _   _      
 _   _| |___ ___| |_ _ _ ___ _| |_| |_ ___ ___| |_| |___  
| | | |_ -|_ -|   | | |_ -| . |   | | |_ -|_ -|   | | -_| 
|___|_|___|___|_|_|___|___|___|_|_|_|_|___|___|_|_|_|___| 
              🚀 SPACE AGE HUSTLE (Anti-Gravity v1.0)
```

---

## 🔗 Imported Sources

This project consolidates `trill-local-runtime` (automation/n8n catalog), `charhubai-stagetemp` (UI composition) and `canva-apps-sdk-starter-kit` (app starter patterns). See [docs/sources.md](docs/sources.md) for the mapping and configuration.

**Run locally:** `cp .env.example .env && bun install && bun run dev` (port 3000).

---

## 🌌 Overview

**USS Hustle** is a zero-gravity productivity RPG engine and digital agent command center built for **Oneseco Media**. It translates real engineering workflows—Jira tickets, GitHub PRs, bug fixes, test coverage, and production deployments—into in-game XP, loot drops, and dynamic AI crew unlocks.

Rewritten as a high-fidelity React application with Dark Nebula HUD aesthetics, real-time character genesis simulation, mission task broker, inventory management, canonical transmission broadcasting, and interactive Notion story matrices.

---

## 🪐 The Dynamic Crew Roster

Agents emerge dynamically from actual work patterns:

| Agent | Role | Unlocked By | Superpower |
|:---|:---|:---|:---|
| **Trill Astro Buzz** | First Officer | Game Start (Default) | **Cosmic Clutch**: +10% XP & Zero-G Motivation |
| **Nova Starwind** | Code Navigator | 5 Bugs Fixed | **Slingshot Refactor**: Architectural cleanup & +25 XP |
| **Orion Codex** | DevOps Lead | 3 Successful Deploys | **Plasma Shield**: Pre-flight CI/CD verification |
| **Vega Quantum** | QA Scientist | 10 Tests Written | **Tachyon Scan**: Uncovers hidden edge-cases |
| **Zara Nebula** | Project Wrangler | 2 Sprint Meetings | **Quantum Sync**: Auto-prioritizes Jira backlogs |
| **Atlas Comet** | Release Engineer | 3 Deploys in 1 Week | **Zero Downtime**: Multi-service release warp |

---

## 🚀 Features

- **Bridge / HUD**: Real-time Commander Dossier, Level progression, streak counter, customizable status, interactive work telemetry, and floating motivation from First Officer Trill Astro Buzz.
- **Dynamic Character Genesis**: Live simulation of unlocking agents as engineering telemetry increments.
- **Orbital Task Broker**: Jira & GitHub task queueing with runtime selection (Codex, Jules, Craft, Zapier, Local) and approval-gated state transitions.
- **Cargo Bay & Loot**: Inventory management for Quantum Coffee, Warp Accelerators, Tachyon Crystals, and Levitation Tokens with an interactive Supply Crate drop opener.
- **Dispatches & Notion Matrix**: Canonical Trill Astro Buzz transmissions log, message composer, and a 15-node interactive narrative dialogue player.
- **Ink RPG**: Interactive branching stories written in [Ink](https://www.inklestudios.com/ink/) and compiled/played in-browser with `inkjs`; story events can award XP (see `src/services/inkStoryService.ts`).
- **XP Visualization**: Recharts-based XP bar chart on the Bridge HUD.
- **Operations Gateway**: Interactive Telegram bot terminal simulator (`/task`, `/approve`, `/delegate`, `/status`, `/briefing`) and automations monitor.

---

## 🛰️ Quick Start

Requires [Bun](https://bun.sh) (a `bun.lock` is committed); npm also works.

```bash
cp .env.example .env     # fill in only the integrations you need
bun install
bun run dev              # Vite dev server on http://localhost:3000
```

| Script | Purpose |
|:---|:---|
| `bun run dev` | Start the dev server (port 3000, all interfaces) |
| `bun run build` | Production build to `dist/` |
| `bun run preview` | Serve the production build |
| `bun run lint` | Type-check with `tsc --noEmit` |

---

## 🗂️ Project Structure

```text
src/
  App.tsx, main.tsx     App shell and entry
  components/           HUD, crew roster, missions, cargo bay, dispatches, Ink RPG, gateway
  agents/, services/    Genesis engine, Ink story service, ambient audio
  data/, db/            Seed data and D1 schema (schema.sql)
skills/                 Agent skill docs (one per crew member) + n8n/catalog.json
automations/            Automation definitions (automations.json)
docs/                   Sources, Zapier setup, story nodes, design specs and plans
themes/                 Theme tokens (theme.json)
game_state.json         Sample game state
```

---

## ⚙️ Configuration

Copy `.env.example` to `.env`. No secrets are committed. Variables are grouped by integration:

- **Cloudflare**: `CLOUDFLARE_ACCOUNT_ID`, `CLOUDFLARE_API_TOKEN`
- **Telegram gateway**: `TELEGRAM_BOT_TOKEN`, `TELEGRAM_GATEWAY_TOKEN`, `TELEGRAM_WEBHOOK_SECRET`, `OPS_ADMIN_CHAT_ID`
- **Zapier / Jira**: `ZAPIER_JIRA_CREATE_WEBHOOK`, `ZAPIER_WEBHOOK_SECRET`
- **Notion / Craft**: `NOTION_API_TOKEN`, `NOTION_STORY_DB_ID`, `CRAFT_*`
- **n8n**: `N8N_BASE_URL` (default `http://localhost:5678`), `N8N_API_KEY`
- **Notifications / misc**: `NOTIFY_DEVICE_ID`, `NOTIFY_TOKEN`, `ONESECO_AVATAR_URL`

---

## 📚 Docs

- [docs/sources.md](docs/sources.md): imported repositories and how they map here
- [docs/opxero-zapier-setup.md](docs/opxero-zapier-setup.md): Zapier setup
- [docs/superpowers/specs/2026-09-12-agent-mission-broker-design.md](docs/superpowers/specs/2026-09-12-agent-mission-broker-design.md) and its [plan](docs/superpowers/plans/2026-09-12-agent-mission-broker.md): mission broker design
- [skills/](skills/): per-agent skill docs

---

## 📜 License

Apache-2.0 © Oneseco Media. **Gravity is optional. Delivery is not.** 🫡🚀🪐
