# Relatório de Duplicatas e Oportunidades de Reaproveitamento

Auditoria conforme `prompt_auditoria_code.md`, Etapa 2. Agrupamento por
tema/subtema do mapa v2, independente de turma (nenhum arquivo atual indica
turma, então esse eixo não se aplica mais — ver `inventario_listas.md`).

**Nenhum arquivo foi movido, mesclado ou apagado nesta etapa.** As sugestões
abaixo aguardam aprovação do professor.

---

## Grupo 1 — Eletrostática (4 arquivos)

`eletro-cargas-eletricas.html`, `eletro-eletrizacao.html`,
`eletro-lei-de-coulomb.html`, `eletro-revisao-vetores.html`

| Arquivo | Cobre |
|---|---|
| `eletro-cargas-eletricas.html` | `q=n·e` isolado, `n=q/e` isolado (8 questões dedicadas) |
| `eletro-eletrizacao.html` | Atrito, contato (com cálculo), indução — mais profundo que a revisão em cada processo (11 questões) |
| `eletro-lei-de-coulomb.html` | Coulomb: isolar carga, superposição de 3 cargas, ponto de equilíbrio, geometria triangular — só 4 questões, mas os 2 últimos são N4 que não aparecem em nenhum outro arquivo |
| `eletro-revisao-vetores.html` | Um pouco de cada um dos três acima **+ vetores** (não coberto em nenhum outro arquivo), só que com menos questões por subtópico |

**O que é repetido:** o Bloco 2 da revisão (`q=n·e`, 3 questões) repete o
mesmo par (fórmula, incógnita) do Bloco 2/3 de `eletro-cargas-eletricas.html`.
O Bloco 3 da revisão (contato, 3 questões) repete o padrão de
`eletro-eletrizacao.html` Bloco 2. Os Blocos 4–5 da revisão (Coulomb, 7
questões) cobrem o mesmo terreno de `eletro-lei-de-coulomb.html` Q1–Q2, mas
sem chegar aos casos N4 (ponto de equilíbrio, geometria triangular) que só
existem no arquivo dedicado.

**O que é complementar:** a revisão é a única fonte de questões de
decomposição vetorial — conteúdo que não existe em mais nenhum lugar do
repositório, apesar de vetores serem citado como categoria de cor própria em
`prompt_projeto_fisica.md`.

**Sugestão (não decidida):** os 3 arquivos temáticos (`cargas-eletricas`,
`eletrizacao`, `lei-de-coulomb`) parecem ser as listas "de aprofundamento",
uma por subtema, seguindo a progressão N0→N4 completa cada uma. A "revisão"
parece ser uma lista de fechamento/mistura para revisão pré-prova, cobrindo
tudo em doses menores + vetores. **Recomendo manter as 4 como estão** — não
são de fato redundantes, são camadas diferentes (aprofundamento por
subtema vs. revisão mista pré-avaliação) — mas vale renomear mentalmente a
categoria da "revisão" para deixar claro que ela é um apanhado geral, não
uma 4ª lista de aprofundamento igual às outras. Se o professor preferir
reduzir volume, o candidato a cortar seria o Bloco 2 da revisão (mais
redundante com `cargas-eletricas`), mantendo vetores e Coulomb.

---

## Grupo 2 — Ondulatória Geral (3 arquivos: overlap direto em `v=λf`/`T=1/f`)

`onda-periodo-frequencia.html`, `onda-comprimento-frequencia.html`,
`onda-revisao.html`

| Arquivo | Cobre |
|---|---|
| `onda-periodo-frequencia.html` | Conceitual (cristas/vales/amplitude, onda mecânica vs. eletromagnética), `f=1/T`/`T=1/f` isolado, `v=λf` isolado — progressão didática limpa, contextos simples |
| `onda-comprimento-frequencia.html` | Só `v=λf`, mas em 10 contextos aplicados diferentes (eco, rádio AM/FM, morcego, tempestade, diapasão) — funciona como "banco de problemas contextualizados" da mesma fórmula |
| `onda-revisao.html` | Bloco 1 repete `v=λf`/`T=1/f` (5 questões) — **mesmo par fórmula/incógnita dos dois arquivos acima**, contextos parecidos (boia, som em barra metálica, diapasão). Blocos 2–6 introduzem conteúdo que **não existe em nenhum outro arquivo do repositório e não está no mapa v2**: velocidade de onda em corda (`v=√(F/μ)`), superposição de pulsos, ondas estacionárias (`L=n·λ/2`), aplicação a ondas eletromagnéticas (micro-ondas, luz visível) |

**O que é repetido:** o Bloco 1 de `onda-revisao.html` é, em essência, uma
reamostragem de `onda-periodo-frequencia.html` + `onda-comprimento-frequencia.html`
— mesma fórmula, mesma incógnita, contextos só levemente diferentes (ex.:
Q02 do Bloco 1 é literalmente "som muda de meio, frequência não muda" — o
mesmo conceito da Questão 3 de `onda-comprimento-frequencia.html`).

**O que é complementar:** os Blocos 2–5 de `onda-revisao.html` (corda,
superposição, ondas estacionárias) são conteúdo genuinamente novo — e como o
`mapa_conteudos_fisica_enem_v2.md` **não tem uma chave própria para isso**,
vale considerar adicionar "3.1b Ondas em Cordas e Superposição" (ou similar)
ao mapa como um subtema formal, já que há material de sobra para justificar.

**Sugestão (não decidida):** os dois primeiros arquivos (`periodo-frequencia`
e `comprimento-frequencia`) têm sobreposição forte entre si também — ambos
são essencialmente listas de `v=λf` com roupagens diferentes (uma mais
didática/progressiva, outra mais contextual/aplicada). Poderiam ser
consolidados em uma única lista "Ondulatória — Equação Fundamental" que
aproveite o melhor de cada (a progressão conceitual do primeiro + os
contextos mais ricos do segundo), liberando o nome "comprimento-frequencia"
para outro uso. Já `onda-revisao.html`, por trazer conteúdo próprio
(cordas/estacionárias), provavelmente deveria ser **desmembrado**: o Bloco 1
(redundante) poderia ser cortado ou reduzido, e os Blocos 2–5 promovidos a
uma lista própria de "Ondas em Cordas e Superposição". Nenhuma dessas ações
foi executada — apenas sugerida para aprovação.

---

## Grupo 3 — Calorimetria / Termologia (3 arquivos)

`termo-calorimetria.html`, `termo-equilibrio-mudanca-estado.html`,
`termo-revisao-calorimetria.html`

| Arquivo | Cobre |
|---|---|
| `termo-calorimetria.html` | Conceitual, `Q=mcΔT`, `Q=mL`, curva de aquecimento (1 corpo, multietapa) e equilíbrio de 2 corpos (Q10 sem mudança de fase, Q11 com um corpo metálico) — 11 questões, progressão N0→N4 completa dentro do próprio arquivo |
| `termo-equilibrio-mudanca-estado.html` | Só equilíbrio térmico, mas **todas as 5 questões são N4** com mudança de fase embutida (gelo derretendo, vapor condensando) — é o subconjunto mais avançado do mapa v2 ("Verificação de estado final — coexistência de fases", "Tf com mudança de fase embutida") |
| `termo-revisao-calorimetria.html` | Termometria (conversão C/F/K — **único lugar do repositório que cobre isso**) + repete sensível/latente/equilíbrio em versão reduzida (1–2 questões por subtópico) + 1 questão multietapa |

**O que é repetido:** `termo-equilibrio-mudanca-estado.html` é, na prática,
uma versão expandida e mais difícil do que já aparece implicitamente nas
Q9–Q11 de `termo-calorimetria.html` (curva de aquecimento e equilíbrio com
mudança de fase) — o padrão "gelo aquece até 0°C, funde, depois esquenta
como água" se repete em ambos. `termo-revisao-calorimetria.html` Blocos 2–4
repetem `Q=mcΔT`, `Q=mL` e equilíbrio simples já vistos em
`termo-calorimetria.html`, com números diferentes mas mesma estrutura.

**O que é complementar:** só `termo-revisao-calorimetria.html` cobre
termometria (2.1) — nenhum outro arquivo do repositório aborda conversão de
escalas de temperatura, embora o mapa v2 trate isso como subtema próprio.

**Sugestão (não decidida):** os 3 arquivos formam uma progressão pedagógica
razoável (base → avançado → revisão mista) e não é óbvio que devam virar um
arquivo só — mas o professor pode considerar (a) mover o Bloco 1 de
`termo-revisao-calorimetria.html` (termometria) para um arquivo próprio
`termo-termometria.html`, já que é o único conteúdo do repo sobre esse
subtema e fica "escondido" dentro de uma lista de revisão de calorimetria; e
(b) avaliar se `termo-equilibrio-mudanca-estado.html` deveria absorver
as questões de equilíbrio com mudança de fase que já aparecem em
`termo-calorimetria.html` (Q9) e `termo-revisao-calorimetria.html`
(Bloco 5), centralizando esse padrão de questão em um único lugar.

---

## Grupo 4 — Óptica (2 arquivos — overlap leve, não é duplicata real)

`optica-geometrica.html`, `optica-lentes-aplicada.html`

Esses dois já foram desenhados como um par complementar (o segundo arquivo
tem um botão explícito "← Lista 1 (Óptica Geométrica)" apontando para o
primeiro). A divisão de conteúdo é limpa: o primeiro cobre cores, princípios,
espelhos planos/esféricos e Snell; o segundo cobre lentes, vergência,
instrumentos e reflexão total/fibra óptica. **Não há repetição de
(fórmula, incógnita)** entre eles — a única sobreposição é conceitual (ambos
tocam "ângulo limite/reflexão total" — `optica-geometrica.html` Q16 pede o
ângulo limite de um material de índice √2, e `optica-lentes-aplicada.html`
Q17–Q20 aprofunda o mesmo cálculo em 4 questões, incluindo fibra óptica e o
diamante). **Sugestão:** nenhuma ação necessária — o par já funciona bem
como está; no máximo vale uma nota no gabarito de `optica-geometrica.html`
avisando que o ângulo limite será retomado com mais profundidade na próxima
lista.

---

## Resumo dos grupos

| Grupo | Arquivos | Sobreposição real (mesma fórmula+incógnita) | Conteúdo exclusivo relevante |
|---|---|---|---|
| 1. Eletrostática | 4 | Moderada (revisão duplica os 3 temáticos em menor escala) | Vetores (só na revisão) |
| 2. Ondulatória Geral | 3 | Alta entre os 2 primeiros; moderada no Bloco 1 da revisão | Cordas/superposição/estacionárias (só na revisão, fora do mapa v2) |
| 3. Calorimetria | 3 | Moderada (padrão gelo+água se repete em 2 arquivos) | Termometria (só na revisão) |
| 4. Óptica | 2 | Baixa/nenhuma (par já é complementar por design) | — |

Nenhuma consolidação foi executada. Todas as sugestões acima requerem
aprovação explícita do professor antes de qualquer `git mv`, fusão ou
exclusão de arquivo, conforme regra do prompt de auditoria.
