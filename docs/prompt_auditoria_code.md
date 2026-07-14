# Prompt para Claude Code — Auditoria e Reorganização do Repositório de Listas

## Contexto (leia antes de começar)

Este repositório contém listas de exercícios de Física em HTML (e seus
gabaritos em Markdown) produzidas ao longo do tempo para turmas diferentes
(9º ano, 1EM, 2EM, 3EM). Várias listas cobrem o mesmo assunto, geradas em
momentos diferentes para turmas diferentes — isso gerou **conteúdo duplicado
ou parcialmente sobreposto** que precisa ser identificado antes de qualquer
reorganização.

O objetivo final do projeto é consolidar tudo em **um repositório definitivo,
organizado por área de conteúdo (não por turma)**, que sirva de base para um
infoproduto. Mas essa estrutura precisa continuar **fluida** — o professor
precisa poder editar, mover e ajustar qualquer coisa manualmente depois, sem
depender de scripts rígidos ou convenções que quebrem fácil.

**Sua tarefa nesta etapa é só auditoria e organização — não gerar conteúdo
novo de exercício nenhum.** A geração de listas continua acontecendo no
Claude (via chat/claude.ai), onde o professor valida os números e aprova
antes de qualquer arquivo ser criado. Você não deve escrever nenhum
enunciado, questão ou gabarito novo neste processo.

### Arquivos de referência (leia antes de mapear qualquer coisa)

Três arquivos definem a taxonomia e o padrão do projeto — devem estar na raiz
do repositório (ou em uma pasta `/docs`):

- `mapa_conteudos_fisica_enem_v2.md` — a taxonomia de temas/subtemas e a
  progressão de incógnitas (N0–N4) que toda lista deveria seguir. Use as
  chaves deste mapa (ex.: "1.1 Eletrodinâmica", "5.3 Espelhos Esféricos")
  como categorias-padrão para classificar cada arquivo existente.
- `prompt_progressao_fisica.md` — explica a metodologia de progressão por
  incógnitas usada para montar as listas.
- `prompt_projeto_fisica.md` — define identidade visual, formato dos
  arquivos e regras de geração (não é relevante para a auditoria em si, mas
  ajuda a entender os nomes de arquivo e a estrutura esperada).

---

## Etapa 1 — Inventário Completo

Percorra o repositório e catalogue **todo arquivo de lista (`.html`) e seu
gabarito correspondente (`.md`)**. Para cada par, extraia:

- Nome do arquivo (lista e gabarito)
- Tema/subtema mapeado (tentar casar com uma chave do
  `mapa_conteudos_fisica_enem_v2.md`; se não encontrar correspondência clara,
  marcar como "não classificado" em vez de forçar um encaixe)
- Turma (extrair do nome do arquivo ou do conteúdo — ex.: 9º ano, 1EM, 2EM, 3EM)
- Número de questões
- Incógnitas/fórmulas abordadas em cada questão, na medida do possível pela
  leitura do enunciado (ex.: "obtenção de massa em calor sensível", "circuito
  paralelo, achar Req")
- Nível estimado de cada questão (N0–N4, seguindo a mesma escala do mapa)
- Data de criação/modificação (via `git log` do arquivo, se o repositório
  tiver histórico)

Produza um arquivo `inventario_listas.md` com uma tabela contendo todas essas
colunas, uma linha por lista.

---

## Etapa 2 — Identificação de Duplicatas e Oportunidades de Reaproveitamento

Agrupe o inventário por **(tema/subtema do mapa)**, independente da turma.

Para cada grupo com 2 ou mais arquivos:

- Liste os arquivos envolvidos e as turmas de cada um.
- Compare as incógnitas/níveis cobertos por cada arquivo do grupo — aponte
  o que é repetido entre eles e o que é complementar (ex.: a versão do 2EM
  cobre N1–N3 de calorimetria, a versão do 3EM adiciona um N4 que a outra
  não tem).
- Sugira, para cada grupo, se faz sentido **consolidar em uma lista única
  por subtema** (aproveitando o melhor conjunto de questões já validado de
  cada versão) ou se as diferenças justificam manter versões separadas por
  turma. Não decida sozinho — apresente a sugestão para aprovação.

Produza um arquivo `relatorio_duplicatas.md` com essa análise.

**Não delete, não sobrescreva e não mescle nenhum arquivo automaticamente
nesta etapa.** Isso só acontece depois que o professor revisar o relatório.

---

## Etapa 3 — Relatório de Cobertura vs. Mapa de Conteúdos

Cruzando o inventário (Etapa 1) com o `mapa_conteudos_fisica_enem_v2.md`,
monte uma matriz de cobertura: para cada linha de incógnita/nível de cada
subtema do mapa, indicar:

- **Coberto** — já existe lista com essa incógnita/nível, citando o(s)
  arquivo(s).
- **Parcialmente coberto** — existe algo próximo, mas não exatamente aquele
  nível/incógnita (explicar a diferença).
- **Não coberto** — nada no repositório aborda isso ainda.

Produza `relatorio_cobertura.md` com essa matriz completa, e ao final uma
seção **"Backlog de Listas a Criar"** — a lista consolidada de tudo que está
como "não coberto", organizada por área do mapa, pronta para eu (Claude, no
chat) usar como pauta quando o professor pedir a próxima lista.

---

## Etapa 4 — Proposta de Estrutura de Repositório (não executar sem aprovação)

Proponha uma estrutura de pastas organizada por área de conteúdo, seguindo as
chaves do mapa v2, por exemplo:

```
/listas
  /01-eletricidade
    /eletrodinamica
    /eletrostatica
    /magnetismo-forca-magnetica
    /inducao-transformadores
  /02-termologia
    /termometria
    /dilatacao-termica
    /calorimetria
    /propagacao-calor
    /estudo-dos-gases
    /termodinamica
  /03-ondulatoria
  /04-mecanica
    /cinematica-escalar
    /lancamentos
    /dinamica
    /sistemas-de-corpos
    /trabalho-e-energia
    /gravitacao
    /hidrostatica
  /05-optica-geometrica
    /principios
    /espelhos-planos
    /espelhos-esfericos
    /refracao-dioptro-plano
    /lentes-esfericas
    /instrumentos-opticos
  /06-fisica-moderna
```

Cada pasta de subtema recebe os pares `lista_*.html` / `gabarito_*.md`
existentes, mantendo a turma no nome do arquivo até que uma eventual
consolidação (Etapa 2) aconteça — ex.:
`eletrodinamica/lista_circuitos_2EM.html`.

Apresente essa proposta como uma **tabela de caminho antigo → caminho novo**
em `proposta_estrutura_repositorio.md`. **Não mova, renomeie ou reorganize
nenhum arquivo automaticamente** — isso só deve ser executado depois que o
professor aprovar explicitamente, e preferencialmente usando `git mv` para
preservar o histórico.

Mantenha o índice/página principal do repositório (o que você já ajudou a
montar antes) como algo a ser **regenerado depois** da reorganização
aprovada — não precisa atualizá-lo nesta auditoria.

---

## Regras Gerais (aplicam-se a todas as etapas)

- **Nunca gerar conteúdo novo de exercício, enunciado ou gabarito.** Isso é
  trabalho do Claude no chat, com validação numérica em Python e aprovação
  explícita do professor antes de qualquer arquivo ser criado.
- **Tudo deve ser reversível.** Qualquer movimentação de arquivo deve usar
  `git mv`; nada é deletado sem confirmação explícita do professor.
- **A estrutura final precisa ser fácil de editar manualmente.** Evite
  convenções rígidas, scripts frágeis ou nomenclatura que dependa de padrões
  não documentados — o professor precisa conseguir mover/renomear pastas
  livremente depois sem quebrar nada.
- **Se um arquivo não puder ser classificado com confiança**, liste-o em uma
  seção separada de "não classificados" no inventário, para revisão manual —
  não force um encaixe em uma categoria errada.
- Ao final das 4 etapas, apresente um resumo curto (não um relatório extenso)
  destacando: quantas listas existem, quantos grupos de duplicata foram
  encontrados, e quantas células do mapa de conteúdo ainda estão sem
  cobertura — para o professor decidir os próximos passos.

## Observação à parte (opcional, não bloqueia a auditoria)

Há um bug conhecido nos arquivos HTML existentes: o ano exibido está fixo em
2025 em vez de 2026. Se for de baixo custo, você pode identificar quantos
arquivos têm essa ocorrência e listar no relatório de inventário (coluna
extra "ano incorreto: sim/não"), mas a correção em lote deve ser tratada
como uma tarefa separada, após a reorganização ser aprovada.
