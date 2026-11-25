# 🤖 AI Agent Command Center

A 3D virtual software-development office where **you create three AI agents** (Backend, Frontend, Testing), your **manager sends you priority tasks**, you **give the work to your agents**, and your only job is the **final verification**.

> **Status: interactive prototype.** The agents are simulated in the browser. A real Java + Kafka orchestrator with live AI coding models is the next stage.

🔗 **Live demo:** https://merhawi7.github.io/Ai-agent-Command-center/

## ✨ Features
- 3D office (Three.js) with animated agents at their desks
- **Step 1:** create your 3 agents (name + model)
- **Step 2:** manager sends priority tasks to your inbox, you give them to your agents
- Live code panels, terminal, and the 8-step plan for every agent
- Pause / resume / stop controls and a live activity feed
- **Step 3:** agents send reports, you press **✔ VERIFIED** or request changes

## ▶️ Run it
Open `index.html` in a modern browser. No install needed (it loads Three.js from a CDN).

## 🏗️ Planned architecture
You ← Manager → Orchestrator (Java / Spring Boot) + Kafka events → Backend, Frontend and Testing agents → shared Git repo → final human verification.

## 🧰 Tech
Three.js · JavaScript · (planned) Java Spring Boot · Apache Kafka · React · PostgreSQL · Playwright · Vitest

## 🗺️ Roadmap
- [x] 3D office, agents, manager inbox, step tracking, reports, final verification
- [ ] Java orchestrator + Kafka event bus
- [ ] Real AI coding agents working in separate Git branches
- [ ] Real test runs and reports
