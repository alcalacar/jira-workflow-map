# 🔄 Guía de Actualización & Prompts AI — Jira Workflow Map

> **Esta guía explica cómo mantener actualizado `index.html` cuando cambien los workflows de Jira Cloud o las fases de la metodología QA.**

---

## 📂 Archivos Fuente Utilizados

| Archivo | Ubicación | Descripción |
|---|---|---|
| **JSON de Workflows Jira** | `schema/jira-workflows.json` | JSON exportado/sincronizado desde Jira Cloud con IDs de estados, transiciones y nombres de workflows. |
| **Página Principal** | `index.html` | Aplicación estática que renderiza los mapas interactivos utilizando la variable JavaScript `WORKFLOWS`. |
| **Alias Espejo** | `jira-workflow-map.html` | Copia idéntica de `index.html` para compatibilidad de URLs. |

---

## 🤖 Prompt Recomendado para Agentes AI (Claude, Antigravity, Cursor, ChatGPT)

Cuando se modifique `schema/jira-workflows.json` o cambie la metodología QA en Jira Cloud, copiá y pegá el siguiente prompt a cualquier asistente de IA para sincronizar automáticamente el visualizador:

```text
Tengo un archivo JSON actualizado con la estructura de workflows de Jira Cloud en 'schema/jira-workflows.json'. 

Por favor realiza los siguientes pasos:
1. Revisa 'schema/jira-workflows.json' y extrae los estados, categorías (new, working, done, exception), el Camino Feliz (main) y los desvíos (sidings) para cada issue type.
2. Mapea las estaciones a las 3 Fases Metodológicas de QA según el framework Agentic QA:
   - Fase 1: Ingesta, Shift-Left QA & Refinamiento (Stage 0 / Stages 1-3).
   - Fase 2: Construcción, Desarrollo & Code Review.
   - Fase 3: Pruebas en Sprint, Regresión CI/CD & Entrega (Stage 4 / Stages 5-6).
3. Actualiza el arreglo global WORKFLOWS dentro de index.html conservando el estilo Japandi / Apple Dark Mode, las leyendas cromáticas y las insignias numéricas (#1, #2, #3).
4. Copia los cambios de index.html a jira-workflow-map.html para mantener ambos sincronizados.
5. Corre 'bun run format:fix' para formatear limpiamente.
```

---

## ⚡ Comandos Rápidos de Sincronización

```bash
# 1. Copiar index.html a jira-workflow-map.html (Alias espejo)
cp index.html jira-workflow-map.html

# 2. Formatear código
bun run format:fix

# 3. Commitear y subir a GitHub Pages
git add .
git commit -m "chore(sync): update Jira Cloud workflows schema"
git push origin main
```
