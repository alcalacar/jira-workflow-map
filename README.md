# 🗺️ Bunkai Jira & Xray Workflow Map

> **Interactive Visualization System for Bunkai QA Engineering Workflows & Governance Schemes.**

![Workflows Map Showcase](https://img.shields.io/badge/Jira_Cloud-Workflow_Scheme-0052CC?logo=jira&logoColor=white)
![Xray TMS](https://img.shields.io/badge/Xray-Test_Management-FF5630?logo=jira&logoColor=white)
![Agentic QA](https://img.shields.io/badge/Framework-Agentic_QA_Stages_0--6-38BDF8?logo=playwright&logoColor=white)

---

## 🌟 Overview

The **Bunkai Jira Workflow Map** is an interactive, web-based visualizer designed to document, navigate, and explore the **9 interconnected Jira & Xray workflows** governing Bunkai QA Engineering.

Built with a Japandi / Apple Enterprise dark aesthetic, it offers team members, product owners, and QA engineers a complete structural view of issue lifecycles, happy paths, sidings, defect loops, and stage-by-stage governance rules.

---

## ✨ Core Features

- 🚇 **Metro Circuit Happy Paths**: Vertical timeline rendering of canonical issue lifecycles with clear step numbering and status category guides (`To Do`, `In Progress`, `Done`).
- 🔀 **Smart Sidings & Category Filters**: Interactive inspection of alternative transitions and exception loops, auto-grouped and filterable by Jira category.
- 📋 **Zero-Redundancy Station Inspection**: Accordion drawers displaying incoming/outgoing transitions and QA methodology guidelines (`/shift-left-testing`, `/sprint-testing`, `/test-documentation`, `/test-automation`, `/regression-testing`).
- 🏷️ **Agentic QA Stage Alignment (Stages 0–6)**: Phase headers explicitly mapping workflows to canonical QA framework stages (*Stage 0 Shift-Left*, *Stages 1-3 In-Sprint*, *Stage 4 TMS*, *Stage 5 Automation*, *Stage 6 CI/CD Regression*).
- ⌨️ **Command Palette (`⌘K` / `Ctrl+K`)**: Instant search overlay to filter statuses, skills, or workflows.
- 📖 **Interactive Glossary in Footer**: Clickable acronym links (`ACs`, `ATP`, `ATC`, `ROI`, etc.) with smooth scrolling to the footer glossary.
- 🔄 **Life-Cycle Journey View**: Multi-ticket integration flow mapping `Story → Test Execution → Bug → Story`.

---

## 🚀 Getting Started

Simply open `index.html` or `jira-workflow-map.html` in any web browser:

```bash
open index.html
```

Or serve locally:

```bash
npx serve .
```

---

## 🛠️ Built With

- **HTML5 & Vanilla CSS**: Dynamic flexbox/grid layout, CSS variables, glassmorphism, and responsive media queries.
- **Vanilla JavaScript**: Pure ES5/ES6 event delegation, search indexing, and rendering state machine.
- **Prettier**: Clean code formatting (`bun run format:fix`).

---

## 👤 Author

Crafted with ❤️ by **[Carlos Alcalá (alcalacar)](https://github.com/alcalacar)**.

---
*Reflects the actual Jira Cloud Workflow Scheme defined in `.agents/jira-workflows.json` & `project.yaml`.*
