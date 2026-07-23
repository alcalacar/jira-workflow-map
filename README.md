# 🗺️ Mapa Interactivo de Workflows QA — Bunkai (Jira Cloud & Xray TMS)

> **Sistema Visual de Aprendizaje, Gobernanza y Referencia Arquitectónica para el Framework de Agentic QA Engineering.**

[![Jira Cloud](https://img.shields.io/badge/Jira_Cloud-Workflow_Scheme-0052CC?logo=jira&logoColor=white)](https://alcalacar.github.io/jira-workflow-map/)
[![Xray TMS](https://img.shields.io/badge/Xray-Test_Management-FF5630?logo=jira&logoColor=white)](https://alcalacar.github.io/jira-workflow-map/)
[![Agentic QA](https://img.shields.io/badge/Framework-Agentic_QA_Stages_0--6-38BDF8?logo=playwright&logoColor=white)](https://alcalacar.github.io/jira-workflow-map/)
[![GitHub Pages](https://img.shields.io/badge/Status-Live_Deployment-4ADE80?logo=github&logoColor=white)](https://alcalacar.github.io/jira-workflow-map/)

---

## 🌟 Descripción General

El **Mapa Interactivo de Workflows de Bunkai** es una aplicación web Single Page (SPA) desarrollada para visualizar, navegar y estudiar los **9 workflows interconectados de Jira Cloud y Xray TMS** que gobiernan la estrategia de Calidad de Software en Bunkai.

Diseñado bajo una estética **Japandi Dark Mode** basada en los principios de diseño de **Apple e IDEO**, esta herramienta actúa como un **material de referencia continua** para desarrolladores, QA Engineers y Product Owners, facilitando la adopción del framework de gobernanza **Agentic QA**.

👉 **Sitio Web en Vivo (GitHub Pages)**: [https://alcalacar.github.io/jira-workflow-map/](https://alcalacar.github.io/jira-workflow-map/)

---

## 💎 Aristas & Funcionalidades Principales

### 1. 🚇 Metro Circuit & Trazabilidad Ordinal (`#1`, `#2`, `#3`)
- Renderizado de secuencias canónicas (*Happy Path*) estructuradas verticalmente.
- Insignias ordinales (`#1`, `#2`, `#3`) que conectan directamente los pasos de la línea principal con sus acordeones de desvíos y detalles de transición.
- Paleta semántica acorde a Jira Cloud: **Inicio / To Do** (`#cbd5e1`), **En curso / In Progress** (`#60a5fa`), **Completado / Done** (`#4ade80`), **Excepciones / Rejection** (`#f43f5e`).

### 2. ⚡ Navegación Interactiva al Glosario (Spotlight Glow & Pulse)
- Detección automática de siglas metodológicas (`PR`, `QA`, `ACs`, `ATP`, `ATC`, `TC`, `ROI`, `CI/CD`, `SUT`, etc.).
- Al hacer clic sobre cualquier acrónimo en transiciones o tarjetas, la aplicación realiza un *smooth scroll* centrado hacia el glosario en el footer y activa una **animación de resplandor neón cian** (*Spotlight Glow & Pulse*) durante 4 segundos.

### 3. 🏷️ Gobernanza Alineada al Framework Agentic QA (Stages 0 a 6)
- Agrupación estandarizada de estados en las 3 Fases de Calidad:
  - **Fase 1 (Shift-Left Stage 0 & Refinement)**: Ingesta en Backlog, refinamiento de Criterios de Aceptación (ACs) y estimación de *Readiness*.
  - **Fase 2 (Sprint Construction & Testing Stages 1-3)**: Desarrollo en Sprint, Code Review / PR, despliegue a QA y exploración trifuerza (UI / API / DB).
  - **Fase 3 (TMS, Automation & CI/CD Stages 4-6)**: Documentación en Xray, scoring ROI de automatización KATA, entrega a producción y regresión CI/CD.

### 4. 🏛️ Matriz de Arquitectura en 3 Niveles
- Organización jerárquica de ubicación de cada issue type:
  - **Nivel 1 · Contenedor Épico**: Iniciativas estratégicas (*Epic*).
  - **Nivel 2 · Tablero Sprint**: Ejecución operativa (*Story*, *Bug*, *Tech Story*).
  - **Nivel 3 · Depósito Xray**: Repositorio TMS fuera del tablero (*Test*, *Test Plan*, *Test Execution*, *Test Set*, *Precondition*).

### 5. 🔄 Recorrido Integrado del Ciclo de Vida (`Story → Exec → Bug → Release`)
- Mapeo completo del flujo multi-ticket con lectura lógica de izquierda a derecha (L-to-R).
- Destacado visual en carmesí (`#f43f5e`) para el loop de triaje, corrección y *retest* de defectos.

### 6. ⌨️ Command Palette (`⌘K` / `Ctrl+K`) & Filtros de Desvíos Inteligentes
- Buscador flotante para filtrar instantáneamente por estado, skill QA o workflow.
- Barras dinámicas de filtro de desvíos que ocultan categorías vacías (*Zero Empty-States*).

---

## 🚀 Uso Local

Puedes clonar el repositorio y ejecutar la aplicación de forma local sin dependencias de servidor:

```bash
# Abrir directamente en el navegador predeterminado
open index.html
```

O servirlo localmente mediante `npx`:

```bash
npx serve .
```

---

## 🛠️ Mantenimiento Asistido por IA

Los esquemas crudos de Jira Cloud se almacenan en **[`schema/jira-workflows.json`](./schema/jira-workflows.json)**.

Cuando ocurran cambios en los workflows o en las reglas de metodología, consulte **[`UPDATE_GUIDE.md`](./UPDATE_GUIDE.md)** para ejecutar la actualización automática del código mediante un agente de IA.

---

## 🎓 Agradecimientos & Créditos

Este material de estudio y referencia fue creado por y para la comunidad de:

- 🚀 **Curso**: [**Dojo Quality Engineer**](https://www.upexgalaxy.com/cursos/dojo-quality-engineer) por [**UPEX Galaxy**](https://www.upexgalaxy.com/)
- 👨‍🏫 **Instructor & Mentor**: [**Sai (Elyer Maldonado)**](https://www.linkedin.com/in/elyermad/)
- 🧪 **Software Bajo Pruebas (SUT)**: [**Bunkai App**](https://upexbunkai.vercel.app/login) (Team UPEX)

---

## 👤 Autor

Diseñado y Creado con ❤️ por **[Carlos Alcalá (alcalacar)](https://github.com/alcalacar)**.

---
*Refleja el esquema real de Jira Cloud Workflow Scheme configurado para Bunkai QA Engineering.*
