# Metodologia de Progressão por Incógnitas — Adendo ao Prompt do Projeto

Este documento complementa o `prompt_projeto_fisica.md`. Ele não substitui as regras
já existentes (identidade do material, formato dos arquivos, fluxo de aprovação) —
ele define **como as questões de cada lista devem ser escolhidas e ordenadas**.

---

## O Problema que Isso Resolve

Uma lista de exercícios "boa" cobre um tema. Uma lista **completa** cobre
**todas as incógnitas possíveis** das fórmulas daquele tema, em ordem crescente
de complexidade — de forma que o aluno que resolve a lista inteira treinou
isolar algebricamente cada variável e combinar fenômenos, não só repetiu o
mesmo tipo de conta várias vezes.

Isso é o que diferencia o material do "acordaprafisica" de uma lista genérica.

---

## O Método: Isolamento de Incógnitas + Composição de Fenômenos

Para qualquer tema de física, o processo de montagem de uma lista segue 4 passos:

### Passo 1 — Mapear as fórmulas-chave do tema
Liste todas as equações centrais do assunto (ex.: em calorimetria, `Q = m·c·ΔT`
e `Q = m·L`).

### Passo 2 — Mapear todas as variáveis de cada fórmula
Para cada fórmula, listar todas as variáveis que podem ser a incógnita.
Ex.: em `Q = m·c·ΔT`, as incógnitas possíveis são `Q`, `m`, `c`, `ΔT` (que se
desdobra em `Tf` ou `Ti` conhecendo a outra).

### Passo 3 — Uma questão por incógnita, isolada
Criar pelo menos uma questão para cada variável possível, mantendo as demais
como dados fornecidos. Isso garante que o aluno pratique o isolamento
algébrico em todas as direções da fórmula, não só a "conta direta".

### Passo 4 — Composição progressiva de fenômenos
Depois de esgotar as incógnitas de cada fórmula isoladamente, avançar para
questões que **combinam duas ou mais fórmulas/fenômenos do mesmo tema**,
aumentando o número de corpos, de incógnitas simultâneas, ou introduzindo
casos-armadilha (situações onde o erro conceitual comum aparece).

---

## Níveis de Complexidade (Tags Internas)

Cada questão gerada deve ser mentalmente classificada em um nível — isso não
aparece no documento do aluno, mas orienta a ordem de apresentação e evita
repetir o mesmo nível várias vezes seguidas:

- **N1 — Substituição direta**: uma fórmula, um passo, isolar a variável mais
  óbvia (geralmente já isolada na fórmula original).
- **N2 — Isolamento algébrico**: mesma fórmula, mas isolando uma variável que
  exige manipulação (raiz, razão inversa) ou conversão de unidade (ex.: W → kWh,
  min → h, °C → K).
- **N3 — Composição de duas fórmulas/fenômenos**: a questão exige encadear
  dois passos de cálculo ou dois conceitos do mesmo tema (ex.: calor sensível
  seguido de equilíbrio térmico; MRUV seguido de leitura gráfica).
- **N4 — Sistema ou caso especial**: múltiplos corpos, múltiplas incógnitas
  simultâneas, ou uma situação-armadilha conceitual conhecida (ex.: coexistência
  de fases em calorimetria, troca do papel de seno/cosseno em plano inclinado,
  sinal do trabalho em atrito).

Uma lista bem construída normalmente segue a progressão **N1 → N1 → N2 → N2 →
N3 → N3 → N4 → N4**, variando o tamanho conforme a quantidade de questões pedida.

---

## Regra de Não-Repetição

Duas questões não podem testar o mesmo par **(fórmula, incógnita)** na mesma
lista, a menos que a segunda ocorrência aumente genuinamente a complexidade
(mais corpos, conversão de unidade adicional, dado que precisa ser calculado
antes de entrar na fórmula principal, etc.). Isso vale mesmo quando o contexto
narrativo muda (não adianta trocar "carro" por "trem" — se a incógnita e a
fórmula são as mesmas, é repetição).

---

## Como Isso se Encaixa no Fluxo Existente

Este método se insere **entre os passos 2 e 3** do fluxo já definido no
`prompt_projeto_fisica.md`:

1. Se houver prova em anexo, extrair conteúdo primeiro.
2. Validar exercícios matematicamente via Python.
3. **[NOVO] Antes de apresentar a proposta, apresentar também a estrutura de
   progressão**: quais fórmulas serão cobertas, qual incógnita cada questão
   isola, e o nível (N1–N4) de cada uma — em formato de tabela ou lista curta,
   para aprovação do professor junto com os valores numéricos.
4. Gerar a lista no formato escolhido, sem gabarito.
5. Gerar o gabarito em Markdown, indicando o nível de cada questão e, quando
   aplicável, o erro conceitual comum associado (mesma prática já usada nas
   notas pedagógicas do gabarito).

---

## Uso do Mapa de Conteúdos

Este método deve ser aplicado usando o `mapa_conteudos_fisica_enem.md` como
referência de quais fórmulas e incógnitas existem em cada subtema. Quando o
professor pedir uma lista sobre um tema já mapeado, a IA deve:

1. Consultar o mapa para aquele subtema.
2. Selecionar as incógnitas/níveis apropriados à quantidade de questões pedida
   (ex.: 6 questões → normalmente 2×N1, 2×N2, 1×N3, 1×N4).
3. Gerar valores numéricos "redondos" para cada uma (regra já existente:
   ajustar parâmetros até obter resultados limpos).
4. Seguir o fluxo de validação e aprovação normalmente.

Se o tema pedido ainda não estiver no mapa, a IA deve construir a progressão
na hora, seguindo os Passos 1–4 acima, e sugerir que o mapa seja atualizado
com esse novo tema depois.
