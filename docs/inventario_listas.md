# Inventário de Listas — Acorda pra Física

Auditoria conforme `prompt_auditoria_code.md`, Etapa 1. Todos os 12 arquivos
padrão foram lidos por completo (não apenas o `<head>`). Datas via `git log`.

## Observações gerais antes da tabela

- **Nenhum gabarito (`.md`) existe no repositório.** A coluna "Gabarito" é
  "Não existe" em todas as linhas — os gabaritos nunca foram commitados aqui.
- **Nenhum arquivo contém referência a turma (9º ano, 1EM, 2EM, 3EM) nem a
  ano letivo.** Isso já foi resolvido: o commit `7cb9304` ("padroniza HTMLs:
  renomeia arquivos, atualiza identidade visual e remove referências de
  turma/ano", 2026-06-24) removeu essas referências de todos os arquivos e os
  renomeou para o padrão atual `{categoria}-{tema}.html`. Antes dessa limpeza
  havia pelo menos um arquivo com **ano fixo incorreto**: a versão anterior
  de `eletro-revisao-vetores.html` (então `index (10).html`) trazia
  "2º EM — 2º Trimestre **2025**" no cabeçalho — exatamente o bug descrito na
  observação final do prompt de auditoria. Esse arquivo específico já foi
  reescrito (não apenas renomeado) durante a padronização, então **o bug do
  ano não existe mais em nenhum arquivo atual**. Não há ação pendente aqui.
- `mu_muv.html` (adicionado em 2026-07-01, commit `ffa29f3`) **não é uma
  lista de exercícios** no formato padrão — é uma página interativa/dashboard
  de cinemática (MU vs. MUV), tema escuro, sem campos Nome/Turma/Data, sem
  gabarito e não linkada em `index.html`. Listado à parte como "não
  classificado" — decisão sobre mantê-lo no repositório cabe ao professor.
- Todos os 12 arquivos padrão foram criados/renomeados no mesmo commit
  (`7cb9304`, 2026-06-24), então a coluna de data não diferencia idade real
  de conteúdo — apenas quando cada um assumiu o formato atual.

## Tabela — Listas padrão (12)

| # | Arquivo | Tema/subtema (mapa v2) | Turma | Nº questões | Incógnitas/fórmulas principais | Nível estimado | Data (git) | Ano incorreto? |
|---|---|---|---|---|---|---|---|---|
| 1 | `eletro-cargas-eletricas.html` | 1.2 Eletrostática — fundamentos (quantização de carga; pré-requisito não listado como linha própria no mapa) | Não indicada (campo em branco) | 8 | `q = n·e`, `n = q/e`, conceito de transferência de elétrons | N0 (2), N1 (6) | 2026-06-24 | Não |
| 2 | `eletro-eletrizacao.html` | 1.2 Eletrostática — processos de eletrização (atrito, contato, indução) | Não indicada | 11 | Conservação de carga; `q_final=(q1+q2)/n` (contato); indução/polarização; `n=q/e` | N0 (5), N1–N2 (5), N3 (1, indução conceitual) | 2026-06-24 | Não |
| 3 | `eletro-lei-de-coulomb.html` | 1.2 Eletrostática — Lei de Coulomb | Não indicada | 4 | `F=k·q1·q2/d²`; variação de F com d; superposição de forças; ponto de equilíbrio; geometria triangular | N1–N2 (Q1), N3 (Q2), N4 (Q3, Q4) | 2026-06-24 | Não |
| 4 | `eletro-revisao-vetores.html` | Revisão combinada: Vetores (não mapeado no v2) + 1.2 Eletrostática completa | Não indicada | 20 | Decomposição vetorial (`Vx,Vy`); `q=n·e`; contato entre esferas; Lei de Coulomb (força e isolamento de `d`/`q`) | N1–N2 (blocos 1–2), N2 (bloco 3), N1–N3 (blocos 4–5), N3–N4 (bloco 6) | 2026-06-24 (reescrito nesse commit, substitui versão antiga com ano/turma) | Não (era o arquivo com o bug — já corrigido) |
| 5 | `onda-periodo-frequencia.html` | 3.1 Ondulatória Geral (`v=λf`, `f=1/T`) + 3.2 conceitual | Não indicada | 10 | `f=1/T`, `T=1/f`, `v=λ·f` | N0 (3), N1–N2 (7) | 2026-06-24 | Não |
| 6 | `onda-comprimento-frequencia.html` | 3.1 Ondulatória Geral (`v=λf`), aplicado/contextual | Não indicada | 10 | `v=λ·f` em contextos variados (eco, rádio AM/FM, morcego, tempestade) | N1–N2 (maioria), N3 (Q4, Q9, Q10 — múltiplos passos) | 2026-06-24 | Não |
| 7 | `onda-revisao.html` | Revisão ampla: 3.1 Ondulatória Geral + 3.3 Acústica (parcial) + tópicos fora do mapa v2 (ondas em cordas, superposição, ondas estacionárias) | Não indicada | 20 | `v=λf`, `T=1/f`, `v=√(F/μ)` (cordas), superposição `y_res=y1+y2`, `L=n·(λ/2)` (estacionárias), `c=λf` (EM) | N1–N2 (blocos 1–2), N2–N3 (blocos 3–5), N0 (bloco 6) | 2026-06-24 | Não |
| 8 | `optica-geometrica.html` | 5.1 Princípios + 5.2 Espelhos Planos + 5.3 Espelhos Esféricos + 5.4 Refração (Snell) + cores (não mapeado no v2) | Não indicada | 20 | RGB/cores; propagação retilínea (câmara escura); reflexão em espelho plano; `n=c/v`; Snell; equação de Gauss para espelhos | N0 (blocos 1–2), N1–N2 (bloco 3), N1–N2 (bloco 4), N1–N3 (bloco 5) | 2026-06-24 | Não |
| 9 | `optica-lentes-aplicada.html` | 5.5 Lentes Esféricas + 5.6 Instrumentos Ópticos + 5.4 Refração (ângulo limite/reflexão total) | Não indicada | 20 | Equação de Gauss para lentes; aumento; vergência `V=1/f`; associação de vergências; ângulo limite | N0–N1 (bloco 1, raios notáveis), N2–N3 (bloco 1, cálculo), N1–N2 (bloco 2), N0 (bloco 3), N2–N4 (bloco 4) | 2026-06-24 | Não |
| 10 | `termo-calorimetria.html` | 2.3 Calorimetria | Não indicada | 11 | `Q=m·c·ΔT` (sensível); `Q=m·L` (latente); equilíbrio de 2 corpos; curva de aquecimento multietapa | N0 (2), N1–N2 (6), N3–N4 (3) | 2026-06-24 | Não |
| 11 | `termo-equilibrio-mudanca-estado.html` | 2.3 Calorimetria — subtópico avançado: equilíbrio com mudança de fase embutida | Não indicada | 5 | `Q=m·c·ΔT` + `Q=m·L` combinados; equilíbrio de 2 corpos com mudança de fase de um deles | N4 (todas as 5 questões) | 2026-06-24 | Não |
| 12 | `termo-revisao-calorimetria.html` | 2.1 Termometria (conversão de escalas) + 2.3 Calorimetria completa | Não indicada | 10 | Conversões C↔F↔K; `Q=m·c·ΔT`; `Q=m·L`; equilíbrio (massa incógnita); multietapa | N1–N2 (bloco 1), N2 (blocos 2–3), N2–N3 (bloco 4), N4 (bloco 5) | 2026-06-24 | Não |

**Total: 12 listas, 149 questões.**

## Não classificados

| Arquivo | Motivo |
|---|---|
| `mu_muv.html` | Não segue o formato padrão de lista (sem campos Nome/Turma/Data, sem gabarito, não linkado em `index.html`); parece ser um protótipo interativo de MU/MUV, não um exercício de impressão. Necessita decisão manual do professor: manter como material complementar interativo, mover para pasta separada, ou remover. |

## Gabaritos

Nenhum arquivo `gabarito_*.md` existe no repositório atualmente. Se algum já
foi gerado em conversas anteriores no Claude.ai, ele não foi commitado aqui.
