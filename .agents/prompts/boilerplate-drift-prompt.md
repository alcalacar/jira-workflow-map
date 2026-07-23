# Boilerplate drift — AI migration prompt

> **AUTO-GENERATED, SINGLE-USE.** Written by `bun run update` on 2026-07-22.
> Paste the prompt below into your AI session, then delete this file.
> It is regenerated (overwritten) whenever the updater detects new upstream
> changes in protected files.

```text
Migrate the project-adapted files below to the latest boilerplate capabilities, surgically.

These files are intentionally NOT synced by `bun run update` because this project
adapted them. The boilerplate versions evolved since the last sync:

   - CLAUDE.md  (canonical: https://raw.githubusercontent.com/upex-galaxy/agentic-qa-boilerplate/main/CLAUDE.md)  — protected because: per-project AI memory (identity, env URLs, custom rules)
   - config/variables.ts  (canonical: https://raw.githubusercontent.com/upex-galaxy/agentic-qa-boilerplate/main/config/variables.ts)  — protected because: environment/variable map adapted per project

For EACH file:
1. Fetch its canonical boilerplate version from the URL above
   (use your web-fetch tool, or run: curl -fsSL <url>).
2. Diff it against the local copy.
3. Port ONLY the upstream improvements: new capabilities, new config options,
   new sections, fixes. Explain each improvement you are porting.
4. PRESERVE every project adaptation verbatim — names, URLs, credentials
   references, project-specific selectors/fixtures/env vars/jobs. Never replace
   a local customization with a generic boilerplate placeholder.
5. On any genuine conflict (same block, divergent intent), surface it for my
   decision instead of silently overwriting.
6. Show me a concise before/after diff per file BEFORE writing anything.

BEFORE porting any config that depends on a pinned tool (e.g. allurerc.mjs depends on
the `allure` devDependency), check the pinned version against the latest SAME-major
(`npm view <pkg> version` vs package.json) and offer the update first — `bun run update`
appends new devDependencies but never bumps existing ones, so new config options may
not exist in the locally pinned version.

After migrating, run the project verification (tests -> types -> lint) and report results.
```
