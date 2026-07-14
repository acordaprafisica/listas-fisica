# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

A static collection of physics exercise sheets ("listas de exercícios") in standalone HTML, for **Prof. Jonas Pinheiro**'s ENEM-prep project "Acorda pra Física" (acordaprafisica.com.br). Each `.html` file is a print-ready worksheet meant to be opened directly in a browser or printed — no build step, no server, no package manager, no tests. `index.html` is the catalog page linking to every list.

## Working with this repo

There is no build/lint/test tooling. "Running" the project means opening an `.html` file (or `index.html`) in a browser. When editing a list, visually sanity-check it in a browser, including print layout (`@media print`).

## Repository layout

Worksheets live under `/listas`, organized by content area to mirror `docs/mapa_conteudos_fisica_enem_v2.md` (area `01-eletricidade`, `02-termologia`, `03-ondulatoria`, `05-optica-geometrica` — `04-mecanica` and `06-fisica-moderna` don't exist yet because no lists cover them):

```
/listas
  /01-eletricidade
    /eletrostatica     — one file per subtopic (cargas elétricas, eletrização, Lei de Coulomb)
    /revisoes           — mixed-subtopic review lists for this area
  /02-termologia
    /calorimetria
    /revisoes
  /03-ondulatoria
    /ondulatoria-geral
    /revisoes
  /05-optica-geometrica — files here each span multiple subtopics of the area (no single-subtopic split yet)
/experimentais           — non-worksheet pages (e.g. mu_muv.html), not linked from the main card grid
/docs                    — content taxonomy, generation-method prompts, and audit reports (see below)
```

A worksheet goes in a subtopic's own folder (e.g. `eletrostatica/`) when it covers exactly one mapa subtopic; it goes in that area's `revisoes/` folder when it deliberately mixes several subtopics for exam review. Don't force a mixed-topic file into a single subtopic folder just to match a template.

## Architecture

### Two page templates, don't mix them up

- **`index.html`** (repo root) — the catalog/landing page. A dark-navy header + light body with a grid of `.card` links, grouped into `<section class="category">` blocks (Eletricidade, Termologia, Ondulatória, Óptica, …), each linking into `/listas/...`. Its own self-contained `<style>` block, distinct from the worksheet template.
- **Worksheet files under `/listas`** (e.g. `listas/01-eletricidade/eletrostatica/eletro-cargas-eletricas.html`, `listas/02-termologia/revisoes/termo-revisao-calorimetria.html`) — the worksheet template: light background, `header.topo` with discipline/title/professor, an `.ident` block (Nome/Turma/Data fields for the student to fill in by hand), a `table.formulas` reference block, then a sequence of `div.exercicio` question boxes grouped under `h2.secao` blocks, and a `footer.rodape`. Every worksheet duplicates the same CSS variables (`--navy`, `--red`, `--red-soft`, `--cinza`, `--linha`, `--steel`) and structure inline — there is no shared stylesheet, so changes must be copied file-by-file.
- **`experimentais/mu_muv.html`** is an outlier: a dark-themed interactive page, not part of the standard worksheet format (no Nome/Turma/Data, no gabarito). It's linked only from the `index.html` footer, not the main card grid. Treat it as a one-off, not a pattern to copy.

File naming keeps the flat `{categoria}-{tema}.html` prefix convention (`eletro-`, `termo-`, `onda-`, `optica-`) even inside subfolders — the folder gives the subtopic grouping, the filename stays descriptive on its own. When adding a new worksheet: put it in the right `/listas/{area}/{subtopic-or-revisoes}` folder (create the folder if it's the first list for that subtopic/area) and add a corresponding `<a class="card">` entry (with the right relative path, plus updated `cat-count`/header chip counts) to `index.html`.

### Content generation rules (apply when creating or editing exercise lists)

`docs/prompt_projeto_fisica.md`, `docs/prompt_progressao_fisica.md`, and `docs/mapa_conteudos_fisica_enem_v2.md` together define the actual content spec for this project — read them before generating or editing a list:

- **`docs/prompt_projeto_fisica.md`** — the material's identity and hard formatting rules: student worksheets are always `.html` (never docx/pdf), must show "Prof. Jonas Pinheiro", must have Nome/Turma/Data fields, and **must never contain answers, resolutions, or blank space reserved for writing** (students work in a notebook). Answer keys ("gabaritos") are separate Markdown documents (`gabarito_[tema]_[turma].md`) generated only after the HTML list and validated numerically first — none currently exist in this repo. Default gravity is `g = 10 m/s²` unless told otherwise. Each subject has a themed accent color (e.g. Eletrostática = roxo `#7E22CE`, Calorimetria/Termologia = vermelho `#C0392B`) — check existing lists for the established palette before inventing a new color.
- **`docs/prompt_progressao_fisica.md`** — the pedagogical method: questions are built by isolating every possible unknown in each key formula (not just the "obvious" direct substitution), then composing multiple formulas/phenomena, ordered by difficulty tags **N0–N4** (N0 = conceptual, N1 = direct substitution, N2 = algebraic isolation, N3 = composition of two formulas, N4 = multi-body/system or conceptual trap). The same (formula, unknown) pair should not repeat within a list unless complexity genuinely increases.
- **`docs/mapa_conteudos_fisica_enem_v2.md`** — the full topic/subtopic taxonomy (Eletricidade, Termologia, Ondulatória, Mecânica, Óptica Geométrica, Física Moderna) with key formulas and the N0–N4 breakdown per subtopic. Use its section keys (e.g. "1.1 Eletrodinâmica", "5.3 Espelhos Esféricos") as the canonical categories when classifying or planning a list, and as the source of truth for where a new worksheet belongs in `/listas`.
- **`docs/relatorio_cobertura.md`** — current coverage matrix against the mapa (what's covered, partially covered, or missing) plus a backlog of subtopics with zero lists (all of Mecânica and Física Moderna, plus several Eletricidade/Termologia subtopics). Check it before proposing what to generate next.
- **Never author new exercise questions, statements, or answer keys directly in this tool** unless the user explicitly asks for it here — per the project's own workflow, question generation/validation normally happens in a separate chat flow with numeric validation before a professor approves it. If asked to do repo-organization work (inventory, dedup analysis, restructuring), `docs/prompt_auditoria_code.md` documents that workflow's ground rules: audit/report only by default, and any file move should use `git mv` to preserve history.

### Audit trail

`docs/inventario_listas.md`, `docs/relatorio_duplicatas.md`, `docs/relatorio_cobertura.md`, and `docs/proposta_estrutura_repositorio.md` are a point-in-time audit of the repository (content inventory, overlap between lists, mapa coverage, and the reorganization proposal that produced the current `/listas` layout). They describe the state of the repo as of that audit — re-derive from the live files rather than trusting them if the repo has changed significantly since.
