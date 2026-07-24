# 🧠 Bunkai QA Workflow Map — Memoria del Proyecto & Aprendizajes Arquitectónicos

Este documento registra los estándares arquitectónicos, principios de diseño UI/UX, convenciones metodológicas y decisiones de ingeniería establecidas para el **Mapa Interactivo de Workflows de Bunkai (Jira Cloud & Xray TMS)**.

---

## 📌 1. Principios de Diseño UI/UX (Estándares IDEO & Apple Human Interface)

### Estética Japandi Dark Mode
- **Fondo Principal**: `#090d16` (Azul/Pizarra profundo).
- **Tarjetas de Vidrio (Glassmorphism)**: `rgba(18, 26, 43, 0.85)` con `backdrop-filter: blur(16px)`.
- **Bordes Semánticos**: `var(--border-color)` (`rgba(255, 255, 255, 0.1)`).

### Paleta Semántica de Categorías Jira Cloud
- `To Do` / `Inicio` (New): `#cbd5e1` (Pizarra Claro).
- `In Progress` / `En curso` (Working): `#60a5fa` (Azul Cielo).
- `Done` / `Completado` (Done): `#4ade80` (Verde Esmeralda).
- `Exception` / `Rejection` (Salida Excepcional): `#f43f5e` (Rojo Carmesí).

### Micro-Interacciones & Componentes
- **Trazabilidad Ordinal (`#1`, `#2`, `#3`)**: Cada estación principal cuenta con una insignia numérica que coincide con los acordeones de desvíos e inspectores.
- **Pills de Botón Chevron (`.v-chevron`)**: Botones interactivos de 20x20px con efecto hover y rotación fluida a 180° al desplegar detalles.
- **Animación Spotlight (Glow & Pulse)**:
  - Al hacer clic en cualquier sigla interactiva (`.gloss` / `.acronym-link`), la aplicación abre automáticamente `<details id="glossary-section">`, realiza un *smooth scroll* centrado y aplica un pulso neón cian (`glossarySpotlightPulse`) durante 4 segundos.

---

## 🏷️ 2. Marco Metodológico Agentic QA Framework (Stages 0 a 6)

### Fase 1: Shift-Left QA (Stage 0) & Refinamiento
- *Backlog*, *Shift-Left QA*, *Estimation*.
- QA refina los Criterios de Aceptación (ACs) y elabora el borrador del Plan de Pruebas de Aceptación (ATP DRAFT) antes del inicio del desarrollo.

### Fase 2: Construcción en Sprint & Pruebas Trifuerza (Stages 1-3)
- *Ready for Dev*, *In Progress*, *In Review*, *Ready for QA*, *In Test*.
- Desarrollo construye código y somete Pull Requests (PR). QA ejecuta pruebas en el sprint usando la exploración **Trifuerza (UI / API / DB)**.
- *Story In Test* dispara de forma paralela un *Test Execution (ACTIVE)* en Xray TMS.

### Fase 3: Bifurcación de Calidad & Loop de Defectos (Stages 3-6)
- **Orden de Lectura Izquierda a Derecha (L-to-R)**:
  - **Columna Izquierda (Primera Lectura)**: *✦ Algo Falla (Salida Excepcional / Loop de Defecto)* — Triage Stage 2/3 $\rightarrow$ Fix $\rightarrow$ Code Review $\rightarrow$ Retest en QA $\rightarrow$ Closed $\rightarrow$ Desbloquea la Story. Renderizado en **Carmesí (`#f43f5e`)**.
  - **Columna Derecha (Conclusión de Éxito)**: *✓ Todo Pasa (Camino Feliz / Happy Path)* — Test Execution cerrada en verde $\rightarrow$ Stage 4 QA Approved & Scoring ROI $\rightarrow$ Release Backlog $\rightarrow$ Stage 6 Despliegue a Producción & Regresión CI/CD.

---

## 🏛️ 3. Matriz de Arquitectura en 3 Niveles (`Vista Niveles`)

- **Nivel 1 · Contenedor Épico**: Iniciativas estratégicas (*Epic*).
- **Nivel 2 · Tablero Sprint**: Ítems de trabajo en el tablero operativo (*Story*, *Bug*, *Tech Story*). Exhibe insignia superior derecha `Nivel 2`.
- **Nivel 3 · Depósito Xray**: Artefactos del repositorio TMS fuera del board (*Test*, *Test Plan*, *Test Execution*, *Test Set*, *Precondition*). Encabezado renderizado en verde Test `var(--wf-tc)` (`#00e676`).

---

## 🤖 4. Estrategia de Esquema & Mantenimiento Asistido por IA

- **Única Fuente de Verdad**: El esquema JSON crudo exportado de Jira Cloud reside en [`schema/jira-workflows.json`](../schema/jira-workflows.json).
- **Agente de Mantenimiento por IA**: Ante cambios futuros en Jira Cloud, ejecute el prompt de [`UPDATE_GUIDE.md`](../UPDATE_GUIDE.md) para sincronizar `index.html` sin romper los tokens de diseño o la estructura de Fases.

---

## 🎓 5. Créditos & Agradecimientos de la Comunidad

- **Curso**: [Dojo Quality Engineer](https://www.upexgalaxy.com/cursos/dojo-quality-engineer) por [UPEX Galaxy](https://www.upexgalaxy.com/)
- **Instructor & Mentor**: [Sai (Elyer Maldonado)](https://www.linkedin.com/in/elyermad/)
- **Software Bajo Pruebas (SUT)**: [Bunkai App](https://upexbunkai.vercel.app/login)
- **Autor & Creador**: [Carlos Alcalá (alcalacar)](https://github.com/alcalacar)
