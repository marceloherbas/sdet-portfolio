# MARCELO HERBAS CESPEDES
### AI Automation Engineer | Software Engineer in Test | LLM-Powered Workflows
📍 Cochabamba, Bolivia | ✉️ marceherbasc@gmail.com | 📱 +591-77996030
🔗 [LinkedIn](https://linkedin.com) | 🐙 [GitHub](https://github.com)

---

## 📌 PORTFOLIO OVERVIEW & ARCHITECTURE CASE STUDIES

> ⚠️ **Note on Confidentiality:** The following case studies describe production-grade architectures and frameworks designed and maintained by me across corporate environments. To comply with non-disclosure agreements (NDAs), proprietary source code has been omitted, and technical implementations are described at an architectural and strategic level.

---

### 🚀 FEATURED PROJECT: Bug Triage AI Workflow (Open Source)
*Automated QA Workflow using GenAI & Low-Code Integration*

* **The Challenge:** Bug reporting pipelines often suffer from poor classification, missing data, and manual triaging delays, slowing down the development lifecycle.
* **The Solution:** Built a resilient backend workflow using **n8n** that intercepts bug reports via a webhook. Before interacting with the LLM, the payload undergoes input validation using native **JavaScript**. A **Gemini LLM** node is then utilized to classify bug priority and category dynamically. Validated results are logged into Google Sheets and trigger automated, structured email alerts via Gmail.
* **Error Handling & Testing:** Implemented a dedicated global error-handling workflow. Executed 7 rigorous test cases, validating edge cases such as prompt injection attempts, input validation failures, and LLM API downtime.
* **Tech Stack:** `n8n` | `Gemini API` | `JavaScript` | `Webhooks` | `Google Workspace API`
* **Live Repository:** 🔗 [://github.com](https://github.com/n8n-bug-triage-ai)

---

### 🛠️ CASE STUDY 1: Enterprise E2E Test Automation Framework
*Scalable Playwright & TypeScript Architecture (SDET Experience)*

* **The Challenge:** A growing microservices architecture required a fast, reliable, and maintainable end-to-end (E2E) testing suite to replace slow manual regression cycles.
* **The Solution:** Architected and deployed a highly scalable automation framework from scratch using **Playwright** and **TypeScript**. Implemented the **Page Object Model (POM)** pattern alongside custom fixtures to eliminate boilerplate code and optimize test isolation.
* **CI/CD Integration:** Integrated the test suites into **GitHub Actions** and **Jenkins** pipelines, configuring parallel execution shards that optimized machine allocation.
* **Impact:** The framework was adopted as the official engineering team standard, establishing consistent linting, reporting, and execution practices across teams.
* **Tech Stack:** `Playwright` | `TypeScript` | `Node.js` | `GitHub Actions` | `Jenkins` | `POM`

---

### 🤖 CASE STUDY 2: LLM-Powered Autonomous Testing Pipeline
*Multi-Agent System for SDET Acceleration*

* **The Challenge:** The time required to read user stories, author manual test cases, and script them into Playwright was becoming the primary bottleneck in two-week agile sprints.
* **The Solution:** Designed an innovative multi-agent orchestration layer powered by **Claude (Anthropic)**. Configured an MCP (Model Context Protocol) server connection to sync **Jira** and **GitHub**. The system uses 4 specialized agents:
  1. *Planner Agent:* Ingests Jira epics/user stories and outputs structured test conditions.
  2. *Generator Agent:* Scripts those conditions into clean Playwright/TypeScript.
  3. *Healer Agent & Checkpoint:* Executes the scripts locally, catches compilation or runtime failures, and auto-corrects the code.
  4. *Jira Bridge:* Opens GitHub Pull Requests and links them back to Jira, or creates automated defect tickets upon CI execution failures.
* **Impact:** Drastically accelerated the story-to-PR cycle from hours of manual scripting to minutes of automated generation, verified through deterministic code checking.
* **Tech Stack:** `Claude Code` | `Anthropic MCP` | `Playwright` | `TypeScript` | `Jira API` | `Git`

---

### 🌐 CASE STUDY 3: Layered API Testing Strategy
*Robust Backend Integration and Contract Verification*

* **The Challenge:** Microservices communication gaps occasionally led to breaking changes in production API response payloads.
* **The Solution:** Implemented a dual-layered testing defense. For exploratory and manual stages, designed organized collections in **Postman** leveraging global variables, pre-request scripts, and automated environment switching. For continuous integration, built a programmatic regression layer using Playwright's **APIRequestContext**, validating response contracts, status codes, and edge-case boundaries.
* **Tech Stack:** `Postman` | `Playwright API Testing` | `JavaScript` | `REST APIs`
