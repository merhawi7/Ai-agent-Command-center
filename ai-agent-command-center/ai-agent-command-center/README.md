# 🤖 AI Agent Command Center

A 3D virtual software-development office where **you create three AI agents** (Backend, Frontend, Testing), your **manager sends you priority tasks**, you **give the work to your agents**, and your only job is the **final verification**.

> **Status: interactive prototype.** The agents in this demo are simulated in the browser. A real orchestrator with Java + Kafka and live AI coding models is the next stage (see Roadmap).

## ✨ Features

- 3D office (Three.js) with animated human-style agents at their desks
- **Step 1 – Create agents:** name them and pick a model for each role
- **Step 2 – Manager inbox:** tasks arrive with priority (Urgent / High / Normal / Low) and you give them to your agents
- Live code panels, terminal and step-by-step progress ("what they are doing now")
- Pause / resume / stop controls for every agent
- Activity feed of everything that happens
- **Step 3 – Final verification:** agents send reports, you press **✔ VERIFIED** or request changes

## ▶️ Run the demo

No install needed. Open `docs/index.html` in a modern browser (it loads Three.js from a CDN).

Live demo (after enabling GitHub Pages): `https://<your-username>.github.io/ai-agent-command-center/`

## 🏗️ Planned architecture

```
You  ←  Manager (priority tasks)
 │
 ▼
Orchestrator (Java / Spring Boot)
 │   Kafka topics: task.assigned · step.started · test.failed · report.ready
 ├── Backend Agent ──┐
 ├── Frontend Agent ─┼── shared Git repo (separate branches)
 └── Testing Agent ──┘
 │
 ▼
Final human verification  →  merge / deploy
```

## 🧰 Tech stack

| Part | Technology |
|------|------------|
| Demo UI | HTML, JavaScript, Three.js |
| Planned frontend | React + Vite, React Three Fiber |
| Planned backend | Java (Spring Boot), Apache Kafka, WebSockets |
| Database | PostgreSQL |
| Testing | Playwright, Vitest |
| Version control | Git |

## 🗺️ Roadmap

- [x] 3D office + animated agents
- [x] Create agents, manager inbox, priority tasks
- [x] Live code viewer, step tracking, reports, final verification
- [ ] Java orchestrator + Kafka event bus
- [ ] Real AI coding agents that edit files in separate Git branches
- [ ] Real test runs (Vitest / Playwright) and real reports
- [ ] Persistent database and user accounts

## 📄 License

MIT — see `LICENSE`.
