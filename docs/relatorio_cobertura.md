# Relatório de Cobertura vs. Mapa de Conteúdos (v2)

Auditoria conforme `prompt_auditoria_code.md`, Etapa 3. Cruza o inventário
(12 listas, 149 questões) com `mapa_conteudos_fisica_enem_v2.md`.

Para os subtemas em que **nenhuma questão existe**, a matriz linha-a-linha do
mapa seria só uma repetição de "Não coberto" — nesses casos, resumo em uma
linha por subtema (marcado *) em vez de expandir célula a célula, para manter
o relatório legível. Isso cobre a maior parte da área 4 (Mecânica) e da área
6 (Física Moderna), que hoje têm cobertura zero.

---

## 1. Eletricidade

### 1.1 Eletrodinâmica *(zero cobertura)*
| Nível | Incógnita | Status |
|---|---|---|
| N1–N4 (todas as linhas) | i, U, R, P, E, custo, Req misto | **Não coberto** — nenhum arquivo do repositório trata circuitos, Lei de Ohm, potência ou consumo elétrico. |

### 1.2 Eletrostática
| Nível | Incógnita | Status |
|---|---|---|
| N1 | F, d, q1 ou q2 (Coulomb) | **Coberto** — `eletro-lei-de-coulomb.html` Q1; `eletro-revisao-vetores.html` Blocos 4–5 |
| N2 | E (campo elétrico) | **Não coberto** — nenhuma questão calcula campo elétrico (`E=F/q=kQ/d²`); todo o repo trabalha só com força |
| N2 | Carga final — eletrização por contato | **Coberto** — `eletro-eletrizacao.html` Q5–7; `eletro-revisao-vetores.html` Bloco 3 |
| N3 | Conceitual + cálculo — indução | **Parcialmente coberto** — `eletro-eletrizacao.html` Q8–9 cobre a indução só conceitualmente (passo a passo, sem números); falta uma versão com cálculo |
| N3 | E resultante, duas cargas, ponto entre elas | **Não coberto** — o repo tem superposição de *força* (`eletro-lei-de-coulomb.html` Q2), não de campo elétrico |
| N4 | Posição/carga de equilíbrio, três cargas | **Coberto** — `eletro-lei-de-coulomb.html` Q3 (posição de equilíbrio entre duas cargas fixas) |

### 1.3 Magnetismo e Força Magnética *(zero cobertura)*
| Nível | Status |
|---|---|
| N0–N3 (todas as linhas) | **Não coberto** — nenhuma questão sobre ímãs, campo magnético, força magnética ou trajetória de carga em campo |

### 1.4 Indução Eletromagnética e Transformadores *(zero cobertura)*
| Nível | Status |
|---|---|
| N0–N3 (todas as linhas) | **Não coberto** — nenhuma questão sobre Lei de Lenz, fem induzida ou transformadores |

---

## 2. Termologia

### 2.1 Termometria
| Nível | Incógnita | Status |
|---|---|---|
| N1 | Conversão C↔F↔K | **Coberto** — `termo-revisao-calorimetria.html` Bloco 1 (Q1–3), único arquivo do repo com esse conteúdo |
| N2 | Temperatura de coincidência (duas escalas, mesmo valor) | **Não coberto** |

### 2.2 Dilatação Térmica *(zero cobertura)*
| Nível | Status |
|---|---|
| N1–N3 (todas as linhas) | **Não coberto** — nenhuma questão sobre dilatação linear/superficial/volumétrica |

### 2.3 Calorimetria
| Nível | Incógnita | Status |
|---|---|---|
| N1 | Q, m ou c (sensível) | **Coberto** — `termo-calorimetria.html` Q3; `termo-revisao-calorimetria.html` Q4–5 |
| N2 | ΔT, Tf ou Ti (sensível) | **Coberto** — `termo-calorimetria.html` Q4 |
| N1 | Q (latente) | **Coberto** — `termo-calorimetria.html` Q6–7; `termo-revisao-calorimetria.html` Q6 |
| N2 | L ou m (latente) | **Parcialmente coberto** — `m` é pedido (`termo-calorimetria.html` Q8), mas nenhuma questão isola `L` dado `Q` e `m` |
| N3 | Tf — equilíbrio de 2 corpos, temperaturas conhecidas | **Coberto** — `termo-calorimetria.html` Q10–11; `termo-revisao-calorimetria.html` Q8 |
| N3 | m de um corpo — equilíbrio, incógnita é massa | **Coberto** — `termo-revisao-calorimetria.html` Q9 |
| N4 | Tf — equilíbrio de 3 corpos | **Não coberto** — todo o repo só tem equilíbrio de 2 corpos |
| N4 | Tf ou m — equilíbrio com capacidade térmica do calorímetro | **Não coberto** — nenhuma questão inclui `C=mc` do próprio calorímetro na troca de calor |
| N4 | Verificação de estado final — coexistência de fases (armadilha) | **Coberto** — `termo-equilibrio-mudanca-estado.html` Q3, Q5 |
| N4 | Tf — equilíbrio com mudança de fase embutida | **Coberto** — `termo-equilibrio-mudanca-estado.html` Q1, Q2, Q4 |

### 2.4 Propagação de Calor *(zero cobertura)*
| Nível | Status |
|---|---|
| N0–N1 (todas as linhas) | **Não coberto** — nenhuma questão sobre condução (`Φ=kAΔT/L`), convecção ou irradiação |

### 2.5 Estudo dos Gases *(zero cobertura)*
| Nível | Status |
|---|---|
| N1–N3 (todas as linhas) | **Não coberto** |

### 2.6 Termodinâmica *(zero cobertura)*
| Nível | Status |
|---|---|
| N2–N4 (todas as linhas) | **Não coberto** |

---

## 3. Ondulatória

### 3.1 Ondulatória Geral
| Nível | Incógnita | Status |
|---|---|---|
| N1 | v, λ ou f | **Coberto** (bem coberto, com redundância — ver `relatorio_duplicatas.md` Grupo 2) — `onda-periodo-frequencia.html`, `onda-comprimento-frequencia.html`, `onda-revisao.html` Bloco 1 |

### 3.2 Fenômenos Ondulatórios
| Nível | Descrição | Status |
|---|---|---|
| N0 | Reflexão, refração, difração, interferência, polarização (qualitativo) | **Parcialmente coberto** — interferência/superposição está bem coberta em `onda-revisao.html` Bloco 3 (construtiva/destrutiva); difração e polarização não aparecem em nenhum arquivo. Reflexão/refração *da luz* são cobertas na área de Óptica (seção 5), não como fenômeno ondulatório geral |

### 3.3 Acústica
| Nível | Incógnita | Status |
|---|---|---|
| N0 | Conceitual — altura, timbre, intensidade | **Não coberto** — nenhuma questão trata essas três qualidades do som especificamente |
| N3 | f' — Doppler direto | **Não coberto** |
| N4 | f' com sinais — Doppler (aproximação/afastamento simultâneos) | **Não coberto** |
| N0–N2 | Ressonância | **Não coberto** |

**Conteúdo extra não mapeado:** `onda-revisao.html` cobre velocidade de onda
em corda (`v=√(F/μ)`, Bloco 2) e ondas estacionárias (`L=n·λ/2`, Bloco 5) —
material sólido e bem construído, mas sem chave correspondente no mapa v2.
Sugestão para o professor: formalizar isso como um subtema novo (ex.: "3.1b
Ondas em Cordas e Estacionárias") na próxima revisão do mapa.

---

## 4. Mecânica *(zero cobertura — nenhum arquivo do repositório aborda qualquer subtema de Mecânica)*

| Subtema | Status |
|---|---|
| 4.1 Cinemática Escalar | **Não coberto** |
| 4.2 Lançamentos e Cinemática Vetorial | **Não coberto** |
| 4.3 Dinâmica (Leis de Newton) | **Não coberto** |
| 4.4 Sistemas de Corpos | **Não coberto** |
| 4.5 Trabalho e Energia | **Não coberto** |
| 4.6 Gravitação | **Não coberto** |
| 4.7 Hidrostática | **Não coberto** |

Esta é a maior lacuna do repositório: toda a área de Mecânica — tipicamente
uma das mais cobradas no Enem — está com cobertura zero nas 12 listas atuais.

---

## 5. Óptica Geométrica

### 5.1 Princípios da Óptica Geométrica
| Nível | Descrição | Status |
|---|---|---|
| N0 | Propagação retilínea, fontes primárias/secundárias | **Coberto** — `optica-geometrica.html` Q5 (conceitual, implícito na câmara escura) |
| N0–N1 | Câmara escura de orifício (geometria/semelhança de triângulos) | **Coberto** — `optica-geometrica.html` Q5 (cálculo completo) |
| N0 | Sombra/penumbra, eclipses | **Coberto** — `optica-geometrica.html` Q6 |

### 5.2 Espelhos Planos
| Nível | Descrição | Status |
|---|---|---|
| N0 | Leis da reflexão, características da imagem | **Coberto** — `optica-geometrica.html` Q9 (distância objeto-imagem) |
| N2 | Campo visual de espelho plano (geometria) | **Não coberto** |
| N3 | Associação de espelhos planos em ângulo (nº de imagens) | **Coberto** — `optica-geometrica.html` Q10–11 |
| N3 | Translação/rotação de espelho plano (deslocamento da imagem) | **Coberto** — `optica-geometrica.html` Q12 |

### 5.3 Espelhos Esféricos
| Nível | Descrição/Incógnita | Status |
|---|---|---|
| N0 | Elementos: centro, foco, vértice, raio (`f=R/2`) | **Não coberto** — nenhuma questão pede a identificação/nomenclatura desses elementos isoladamente |
| N0 | Raios notáveis e traçado de imagem (sem conta) | **Não coberto** — nenhuma questão de construção gráfica |
| N1 | f, p ou p' — Gauss, isolando cada variável | **Parcialmente coberto** — `optica-geometrica.html` Q18–19 calculam p' a partir de R e p, mas sempre em conjunto com aumento (mistura N1+N2), nunca isolando uma variável por vez |
| N2 | A, tamanho/posição da imagem | **Coberto** — `optica-geometrica.html` Q18–19 |
| N3 | Classificação da imagem (real/virtual, direita/invertida, maior/menor) | **Coberto** — `optica-geometrica.html` Q17–19 |

### 5.4 Refração da Luz e Dioptro Plano
| Nível | Incógnita | Status |
|---|---|---|
| N0 | Conceitual — índice de refração, desvio ao mudar de meio | **Coberto** — `optica-geometrica.html` Q13 |
| N1 | n, θ ou v — Snell, cada variável | **Coberto** — `optica-geometrica.html` Q14–15 |
| N3 | Ângulo limite | **Coberto** — `optica-geometrica.html` Q16; `optica-lentes-aplicada.html` Q17–18, 20 |
| N4 | Contextual — miragem, fibra óptica, dioptro plano (deslocamento aparente) | **Parcialmente coberto** — fibra óptica coberta (`optica-lentes-aplicada.html` Q18–19); miragem e deslocamento aparente em dioptro plano **não cobertos** |

### 5.5 Lentes Esféricas
| Nível | Descrição/Incógnita | Status |
|---|---|---|
| N0 | Elementos, tipos, raios notáveis, traçado de imagem | **Coberto** — `optica-lentes-aplicada.html` Q1–3 |
| N1 | f, p ou p' — Gauss para lentes | **Coberto** — `optica-lentes-aplicada.html` Q4–7 |
| N2 | A, tamanho/posição da imagem | **Coberto** — `optica-lentes-aplicada.html` Q4–7 |
| N3 | Classificação da imagem | **Coberto** — `optica-lentes-aplicada.html` Q4–7 |
| N4 | Associação de lentes justapostas, vergência total | **Coberto** — `optica-lentes-aplicada.html` Q11 |

### 5.6 Instrumentos Ópticos
| Nível | Descrição | Status |
|---|---|---|
| N3–N4 | Olho humano e defeitos de visão (miopia/hipermetropia, lente corretiva) | **Não coberto** — nenhuma questão calcula lente corretiva |
| N3–N4 | Lupa, microscópio, luneta | **Parcialmente coberto** — lupa coberta (`optica-lentes-aplicada.html` Q13); microscópio e luneta **não cobertos**. (Câmera fotográfica, projetor e olho mágico também aparecem, mas não são as instâncias citadas pelo mapa v2 — conteúdo extra útil, ainda que fora da lista literal do mapa) |

---

## 6. Física Moderna *(zero cobertura)*

| Subtema | Status |
|---|---|
| 6.1 Efeito Fotoelétrico | **Não coberto** |
| 6.2 Relatividade | **Não coberto** |
| 6.3 Dualidade Onda-Partícula | **Não coberto** |
| 6.4 Radioatividade | **Não coberto** |

---

## Backlog de Listas a Criar

Organizado por área do mapa, do maior para o menor gap. Pronto para uso como
pauta de próximas listas (a serem geradas em conversa separada, com
validação numérica — não nesta auditoria).

### Prioridade alta — áreas com cobertura zero
- **Mecânica (4.1–4.7), todas as 7 subáreas** — maior lacuna do repositório;
  Cinemática Escalar, Lançamentos, Dinâmica, Sistemas de Corpos, Trabalho e
  Energia, Gravitação e Hidrostática não têm nenhuma lista.
- **1.1 Eletrodinâmica** — Lei de Ohm, potência, consumo, circuitos série/paralelo/misto.
- **1.3 Magnetismo e Força Magnética** — força magnética, regra da mão direita/esquerda.
- **1.4 Indução Eletromagnética e Transformadores.**
- **2.2 Dilatação Térmica.**
- **2.4 Propagação de Calor** (condução/convecção/irradiação).
- **2.5 Estudo dos Gases** e **2.6 Termodinâmica.**
- **6. Física Moderna, todas as 4 subáreas.**

### Prioridade média — subtemas parcialmente cobertos, faltam níveis específicos
- **1.2 Eletrostática:** campo elétrico (E=F/q), indução com cálculo numérico, E resultante de duas cargas em um ponto.
- **2.1 Termometria:** temperatura de coincidência entre escalas.
- **2.3 Calorimetria:** isolar `L` (calor latente específico) dado Q e m; equilíbrio de 3 corpos; equilíbrio com capacidade térmica do calorímetro.
- **3.3 Acústica:** conceitual (altura/timbre/intensidade), efeito Doppler (direto e com sinais), ressonância.
- **3.2 Fenômenos Ondulatórios:** difração e polarização (qualitativo).
- **5.3 Espelhos Esféricos:** questão conceitual de elementos/nomenclatura; traçado gráfico de raios notáveis; isolar f/p/p' individualmente (sem misturar com aumento).
- **5.4 Refração:** miragem; deslocamento aparente em dioptro plano.
- **5.6 Instrumentos Ópticos:** lente corretiva (miopia/hipermetropia); microscópio; luneta.

### Sem ação necessária (já bem cobertos)
1.2 Eletrostática (maior parte), 2.1 Termometria (conversão básica), 2.3
Calorimetria (sensível/latente/equilíbrio de 2 corpos, incluindo mudança de
fase), 3.1 Ondulatória Geral, 5.1 Princípios, 5.2 Espelhos Planos (maior
parte), 5.5 Lentes Esféricas (completo).
