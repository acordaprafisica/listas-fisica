# Mapa de Conteúdos v2 — Divisão Granular por Tema (Prioridade Enem)

Esta é uma revisão do `mapa_conteudos_fisica_enem.md`. A mudança principal:
**cada chave agora representa um conteúdo conceitualmente isolado**, mesmo que
dois conteúdos apareçam juntos em listas de "assuntos mais cobrados" (como
Gravitação e Hidrostática, que não têm nenhuma dependência conceitual entre si).

Também foi adicionado o nível **N0 — Conceitual/Fundamento**, para tópicos que
têm uma etapa puramente qualitativa antes de qualquer fórmula (isso é
especialmente relevante em Óptica e em Eletromagnetismo).

Continua valendo: uma lista não precisa esgotar um subtema inteiro sozinha —
o professor escolhe o recorte (ex.: "lista só de espelhos esféricos" ou
"lista de óptica geométrica completa, dos princípios até lentes").

---

## 1. Eletricidade

### 1.1 Eletrodinâmica
*(inalterado — Ohm, potência, consumo, circuitos série/paralelo/misto)*

**Fórmulas-chave:** `U = R·i` · `P = U·i = R·i² = U²/R` · `E = P·t` ·
`Custo = E(kWh) × tarifa` · série: `Req = R1+R2+...` · paralelo: `1/Req = 1/R1+1/R2+...`

| Nível | Incógnita | Descrição |
|---|---|---|
| N1 | `i`, `U` ou `R` | Lei de Ohm, cada variável |
| N2 | `P` | Qualquer uma das 3 formas de potência |
| N2 | `E` (kWh) | Conversão de unidades |
| N2 | Custo (R$) | Consumo mensal — clássico Enem |
| N3 | `Req`, `i`, `U` | Circuito série ou paralelo simples |
| N4 | Circuito misto | Série-paralelo combinado |
| N4 | Comparação de consumo | Uso racional de energia, contextual |

---

### 1.2 Eletrostática
*(inalterado)*

**Fórmulas-chave:** `F = k·q1·q2/d²` · `E = F/q = k·Q/d²` · conservação de carga.

| Nível | Incógnita | Descrição |
|---|---|---|
| N1 | `F`, `d`, `q1` ou `q2` | Coulomb, cada variável |
| N2 | `E` | Campo elétrico |
| N2 | Carga final | Eletrização por contato |
| N3 | Conceitual + cálculo | Eletrização por indução |
| N3 | `E` resultante | Duas cargas, ponto entre elas |
| N4 | Posição/carga de equilíbrio | Três cargas em equilíbrio |

---

### 1.3 Magnetismo e Força Magnética
*(separado de "eletromagnetismo" — não depende de indução para ser entendido)*

**Fórmulas-chave:** `F = B·i·L·senθ` (condutor) · `F = q·v·B·senθ` (carga).

| Nível | Incógnita | Descrição |
|---|---|---|
| N0 | Conceitual | Ímãs, campo magnético, regra da mão direita/esquerda |
| N1 | `F` | Força magnética, condutor perpendicular ao campo |
| N2 | `F` com ângulo | Uso do seno |
| N2 | `B`, `i`, `L`, `q` ou `v` | Isolando cada variável |
| N3 | Trajetória | Força sobre carga em movimento circular no campo (raio da trajetória) |

**Nota pedagógica:** confundir a regra da mão direita para campo gerado por
corrente com a regra para força sobre corrente em um campo externo.

---

### 1.4 Indução Eletromagnética e Transformadores
*(separado — fenômeno distinto de força magnética, mesmo que use o mesmo campo)*

**Fórmulas-chave:** Lei de Faraday (fem induzida, conceitual + `ε = -ΔΦ/Δt`) ·
transformadores: `Up/Us = Np/Ns = Is/Ip`.

| Nível | Incógnita | Descrição |
|---|---|---|
| N0 | Conceitual | Lei de Lenz, o que gera fem induzida |
| N2 | `ε` | Cálculo direto de fem induzida, variação de fluxo simples |
| N3 | Tensão/corrente/espiras | Transformadores — regra de três direta e inversa |

**Nota pedagógica:** esquecer que transformador ideal não altera potência
(só distribui entre U e i).

---

## 2. Termologia

### 2.1 Termometria (Escalas de Temperatura)
*(separado da dilatação térmica)*

**Fórmulas-chave:** `(C)/5 = (F-32)/9 = (K-273)/5`.

| Nível | Incógnita | Descrição |
|---|---|---|
| N1 | Conversão C↔F↔K | Cada direção |
| N2 | Temperatura de coincidência | Onde duas escalas marcam o mesmo valor |

---

### 2.2 Dilatação Térmica
*(separado da termometria — é outro fenômeno, embora use unidade de temperatura)*

**Fórmulas-chave:** linear: `ΔL = L0·α·ΔT` · superficial: `ΔA = A0·β·ΔT` (β=2α) ·
volumétrica: `ΔV = V0·γ·ΔT` (γ=3α).

| Nível | Incógnita | Descrição |
|---|---|---|
| N1 | `ΔL`, `L0`, `α` ou `ΔT` | Dilatação linear, cada variável |
| N2 | `ΔA` ou `ΔV` | Dilatação superficial/volumétrica, usando relação com α |
| N3 | Aplicação contextual | Juntas de dilatação, dilatação de líquidos em recipiente |

---

### 2.3 Calorimetria
*(mantido como um bloco coeso — calor sensível, latente e equilíbrio térmico
são etapas progressivas do mesmo fenômeno, não conteúdos independentes)*

**Fórmulas-chave:** `Q = m·c·ΔT` (sensível) · `Q = m·L` (latente) ·
equilíbrio térmico: soma das trocas de calor = 0 · `C = m·c`.

| Nível | Incógnita | Descrição |
|---|---|---|
| N1 | `Q`, `m` ou `c` (sensível) | Obtenção direta |
| N2 | `ΔT`, `Tf` ou `Ti` (sensível) | Obtenção de temperatura |
| N1 | `Q` (latente) | Obtenção de calor latente total |
| N2 | `L` ou `m` (latente) | Obtenção de calor latente específico ou massa |
| N3 | `Tf` | Equilíbrio de 2 corpos, temperaturas iniciais conhecidas |
| N3 | `m` de um corpo | Equilíbrio de 2 corpos, incógnita é massa |
| N4 | `Tf` | Equilíbrio de 3 corpos |
| N4 | `Tf` ou `m` | Equilíbrio com capacidade térmica do calorímetro |
| N4 | Verificação de estado final | Coexistência de fases (armadilha conceitual) |
| N4 | `Tf` | Equilíbrio com mudança de fase embutida |

---

### 2.4 Propagação de Calor
*(inalterado)*

**Fórmulas-chave:** condução: `Φ = (k·A·ΔT)/L`.

| Nível | Incógnita | Descrição |
|---|---|---|
| N1 | `Φ`, `k`, `A`, `ΔT` ou `L` | Condução, cada variável |
| N0 | Conceitual | Convecção e irradiação — garrafa térmica, aquecedor solar |

---

### 2.5 Estudo dos Gases
*(separado da termodinâmica — é pré-requisito conceitual, não a mesma etapa)*

**Fórmulas-chave:** `P·V = n·R·T` (equação geral) · Boyle (`T` cte): `P1V1=P2V2` ·
Charles (`P` cte): `V1/T1=V2/T2` · Gay-Lussac (`V` cte): `P1/T1=P2/T2`.

| Nível | Incógnita | Descrição |
|---|---|---|
| N1 | `P`, `V`, `n` ou `T` | Equação geral dos gases |
| N2 | Variável restante | Transformações particulares (isotérmica, isobárica, isocórica) |
| N3 | Combinação | Duas transformações em sequência (estado 1 → 2 → 3) |

---

### 2.6 Termodinâmica
*(separado do estudo dos gases — aqui entra energia, trabalho e ciclos)*

**Fórmulas-chave:** `W = P·ΔV` (isobárico) · 1ª lei: `ΔU = Q - W` ·
rendimento: `η = W/Qq = 1 - Qf/Qq`.

| Nível | Incógnita | Descrição |
|---|---|---|
| N2 | `W` | Trabalho em transformação isobárica; W=0 na isocórica |
| N3 | `ΔU`, `Q` ou `W` | 1ª lei da termodinâmica |
| N4 | `η`, `Qq`, `Qf` ou `W` | Rendimento de máquina térmica / ciclo completo |

**Nota pedagógica:** sinal de `W` (sistema realiza vs. recebe trabalho).

---

## 3. Ondulatória

### 3.1 Ondulatória Geral
**Fórmulas-chave:** `v = λ·f`.

| Nível | Incógnita | Descrição |
|---|---|---|
| N1 | `v`, `λ` ou `f` | Equação fundamental, cada variável |

### 3.2 Fenômenos Ondulatórios
*(puramente conceitual — sem fórmula de cálculo relevante no Enem)*

| Nível | Descrição |
|---|---|
| N0 | Reflexão, refração, difração, interferência, polarização — qualitativo |

### 3.3 Acústica
**Fórmulas-chave:** Doppler: `f' = f·(v±vo)/(v±vf)`.

| Nível | Incógnita | Descrição |
|---|---|---|
| N0 | Conceitual | Altura, timbre, intensidade |
| N3 | `f'` | Doppler direto (fonte ou observador se movendo) |
| N4 | `f'` com sinais | Doppler — aproximação e afastamento simultâneos |
| N0-N2 | Conceitual/aplicação | Ressonância |

---

## 4. Mecânica

### 4.1 Cinemática Escalar
*(separado dos lançamentos — aqui o movimento é 1D)*

**Fórmulas-chave:** MU: `v = ΔS/Δt` · MRUV: `v=v0+at`, `ΔS=v0t+at²/2`, `v²=v0²+2·a·ΔS`.

| Nível | Incógnita | Descrição |
|---|---|---|
| N1 | `v`, `ΔS` ou `Δt` | MU direto |
| N2 | `v`, `v0`, `a` ou `t` | MRUV, cada equação isolada |
| N3 | Combinação de 2 equações | Ex.: tempo de frenagem dado v0, v, a |
| N3 | Leitura de gráfico | v×t (área) e S×t (inclinação) |

---

### 4.2 Lançamentos e Cinemática Vetorial
*(separado — exige composição de movimentos, degrau conceitual acima da escalar)*

**Fórmulas-chave:** queda livre (MRUV com `g`) · lançamento horizontal
(composição de MU horizontal + queda vertical) · lançamento oblíquo
(decomposição em componentes x e y).

| Nível | Incógnita | Descrição |
|---|---|---|
| N2 | `v`, `h` ou `t` | Queda livre / lançamento vertical |
| N3 | Alcance ou tempo de voo | Lançamento horizontal |
| N4 | Alcance, altura máxima, tempo de voo | Lançamento oblíquo — decomposição vetorial |

---

### 4.3 Dinâmica (Leis de Newton)
*(separado dos sistemas de corpos — aqui é um corpo só)*

**Fórmulas-chave:** `F = m·a` · atrito: `Fat = μ·N` · plano inclinado:
`P·senθ` e `P·cosθ`.

| Nível | Incógnita | Descrição |
|---|---|---|
| N1 | `F`, `m` ou `a` | 2ª Lei de Newton direta |
| N2 | `Fat`, `μ` ou `N` | Atrito, cada variável |
| N3 | `a` | Plano inclinado sem atrito |
| N3-N4 | `a` ou `Fat` | Plano inclinado com atrito |

**Nota pedagógica:** troca do papel de seno/cosseno no plano inclinado.

---

### 4.4 Sistemas de Corpos
*(separado — pré-requisito é a dinâmica de um corpo só; aqui entram múltiplos corpos)*

**Fórmulas-chave:** `F = m·a` aplicado ao sistema; tração como força interna.

| Nível | Incógnita | Descrição |
|---|---|---|
| N4 | `a` do sistema, `T` | Blocos conectados por fio (mesma superfície) |
| N4 | `a`, `T` | Polia com massas diferentes (Atwood) |

---

### 4.5 Trabalho e Energia
*(inalterado — já era um bloco coeso)*

**Fórmulas-chave:** `W = F·d·cosθ` · `Ec = m·v²/2` · `Ep = m·g·h` ·
`W = ΔEc` · conservação: `Ec_i+Ep_i = Ec_f+Ep_f`.

| Nível | Incógnita | Descrição |
|---|---|---|
| N1 | `W` | Trabalho direto |
| N1-N2 | `Ec` ou `Ep` | Isolando cada variável |
| N2-N3 | `W`, `ΔEc` ou `v` final | Teorema trabalho-energia |
| N3 | `v` ou `h` | Conservação sem atrito (montanha-russa, pêndulo) |
| N4 | Energia perdida, `μ` ou distância | Conservação com atrito |
| N4 | Múltiplas transformações | Sistemas com mola + gravidade |

---

### 4.6 Gravitação
*(agora uma chave própria, sem hidrostática junto)*

**Fórmulas-chave:** `F = G·M·m/r²` · `g = G·M/r²` · Kepler: `T²/a³ = constante`.

| Nível | Incógnita | Descrição |
|---|---|---|
| N1 | `F`, `G`, `M`, `m` ou `r` | Lei da gravitação universal |
| N2 | `g` em outro planeta | Relação com `g` da Terra |
| N3 | Comparação orbital | 3ª Lei de Kepler entre dois corpos celestes |

---

### 4.7 Hidrostática
*(agora uma chave própria, sem gravitação junto)*

**Fórmulas-chave:** `P = ρ·g·h` · Stevin: `Ptotal = Patm+ρ·g·h` ·
Empuxo: `E = ρfluido·V·g` · Pascal: `F1/A1 = F2/A2`.

| Nível | Incógnita | Descrição |
|---|---|---|
| N1 | `P`, `ρ`, `g` ou `h` | Pressão hidrostática |
| N2 | Pressão total | Teorema de Stevin, dois pontos |
| N3 | `E`, `ρ` ou `V` | Empuxo, cada variável |
| N3-N4 | Condição de flutuação | Empuxo vs. peso |
| N4 | `F2` ou `A2` | Princípio de Pascal — prensa hidráulica |
| N4 | Fração submersa | Corpo parcialmente submerso |

---

## 5. Óptica Geométrica
*(reconstruída como trilha real — dos princípios até a equação de Gauss)*

### 5.1 Princípios da Óptica Geométrica
*(fundamento conceitual, sem o qual espelhos e lentes não fazem sentido)*

| Nível | Descrição |
|---|---|
| N0 | Propagação retilínea da luz, fontes primárias/secundárias |
| N0-N1 | Câmara escura de orifício (relação geométrica simples entre objeto/imagem, semelhança de triângulos) |
| N0 | Formação de sombra e penumbra, eclipses |

### 5.2 Espelhos Planos
*(antes de esféricos — é o caso mais simples de reflexão)*

| Nível | Descrição |
|---|---|
| N0 | Leis da reflexão; características da imagem (virtual, direita, mesmo tamanho) |
| N2 | Campo visual de um espelho plano (geometria) |
| N3 | Associação de espelhos planos em ângulo (número de imagens) |
| N3 | Translação/rotação de espelho plano (deslocamento da imagem) |

### 5.3 Espelhos Esféricos
*(conceitual antes da fórmula — elementos e raios notáveis primeiro)*

| Nível | Descrição/Incógnita |
|---|---|
| N0 | Elementos: centro de curvatura, foco, vértice, raio de curvatura (`f = R/2`) |
| N0 | Raios notáveis e traçado de imagem (côncavo e convexo) — construção gráfica, sem conta |
| N1 | `f`, `p` ou `p'` | Equação de Gauss, isolando cada variável |
| N2 | `A`, tamanho/posição da imagem | Equação do aumento (`A = -p'/p`) |
| N3 | Classificação da imagem | Real/virtual, direita/invertida, maior/menor — cálculo + conceito |

### 5.4 Refração da Luz e Dioptro Plano
*(antes de lentes — refração isolada, sem curvatura envolvida)*

**Fórmulas-chave:** Snell: `n1·senθ1 = n2·senθ2` · `n = c/v`.

| Nível | Incógnita | Descrição |
|---|---|---|
| N0 | Conceitual | Índice de refração, desvio ao mudar de meio |
| N1 | `n`, `θ` ou `v` | Lei de Snell, cada variável |
| N3 | Ângulo limite | Reflexão total — cálculo + conceito |
| N4 | Contextual | Miragem, fibra óptica, dioptro plano (deslocamento aparente) |

### 5.5 Lentes Esféricas
*(mesma lógica dos espelhos — conceitual antes da fórmula)*

| Nível | Descrição/Incógnita |
|---|---|
| N0 | Elementos e tipos (convergente/divergente), raios notáveis, traçado de imagem |
| N1 | `f`, `p` ou `p'` | Equação de Gauss para lentes |
| N2 | `A`, tamanho/posição da imagem | Equação do aumento |
| N3 | Classificação da imagem | Real/virtual, direita/invertida — cálculo + conceito |
| N4 | Associação de lentes (justapostas) | Vergência total (`V = 1/f`) |

### 5.6 Instrumentos Ópticos
*(aplicação/contexto — depende de espelhos, lentes e refração já vistos)*

| Nível | Descrição |
|---|---|
| N3-N4 | Olho humano e defeitos de visão (miopia, hipermetropia — cálculo de lente corretiva) |
| N3-N4 | Lupa, microscópio, luneta — contextual, geralmente conceitual no Enem |

---

## 6. Física Moderna
*(separada da óptica — não depende de óptica geométrica)*

### 6.1 Efeito Fotoelétrico
**Fórmulas-chave:** `E = h·f` · `Ec_max = h·f - função trabalho`.

| Nível | Incógnita | Descrição |
|---|---|---|
| N0 | Conceitual | O que é o efeito, quantização da luz |
| N2 | `E` ou `Ec_max` | Cálculo direto |

### 6.2 Relatividade
| Nível | Descrição |
|---|---|
| N0 | Dilatação do tempo, contração do espaço, `E=mc²` — qualitativo (raramente numérico no Enem) |

### 6.3 Dualidade Onda-Partícula
| Nível | Descrição |
|---|---|
| N0 | Conceitual — De Broglie, experimentos de dupla fenda (qualitativo) |

### 6.4 Radioatividade
**Fórmulas-chave:** meia-vida: `N = N0·(1/2)^(t/T)`.

| Nível | Incógnita | Descrição |
|---|---|---|
| N0 | Conceitual | Decaimento alfa/beta/gama, o que muda em `Z` e `A` |
| N3 | `N`, `t` ou `T` | Meia-vida, cada variável |
| N4 | Balanceamento nuclear | Equações de decaimento, conservação de `Z` e `A` |
| N4 | Contextual | Datação radioativa, medicina nuclear |

---

## Resumo das Mudanças em Relação à v1

| Antes (v1) | Depois (v2) |
|---|---|
| 1.3 Eletromagnetismo (tudo junto) | 1.3 Magnetismo/Força Magnética + 1.4 Indução e Transformadores |
| 2.1 Termometria (escalas + dilatação) | 2.1 Termometria + 2.2 Dilatação Térmica |
| 2.4 Termodinâmica (gases + 1ª lei) | 2.5 Estudo dos Gases + 2.6 Termodinâmica |
| 4.1 Cinemática (escalar + lançamentos) | 4.1 Cinemática Escalar + 4.2 Lançamentos |
| 4.2 Dinâmica (1 corpo + sistemas) | 4.3 Dinâmica + 4.4 Sistemas de Corpos |
| 4.4 Gravitação e Hidrostática (junto) | 4.6 Gravitação + 4.7 Hidrostática |
| 5.1 Óptica Geométrica (direto pra Gauss) | 5.1 Princípios + 5.2 Espelhos Planos + 5.3 Espelhos Esféricos + 5.4 Refração + 5.5 Lentes + 5.6 Instrumentos |
| 5.2 Física Moderna (dentro de "óptica") | 6. Física Moderna (área própria) |
