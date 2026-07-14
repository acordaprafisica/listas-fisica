# Proposta de Estrutura de Repositório

Auditoria conforme `prompt_auditoria_code.md`, Etapa 4.

> **Status: executada em 2026-07-13.** A árvore proposta abaixo foi aplicada
> ao repositório com `git mv` (histórico de cada arquivo preservado),
> `index.html` foi atualizado com os novos caminhos, e `README.md`/`CLAUDE.md`
> foram atualizados para refletir a nova estrutura. Este documento fica como
> registro histórico da decisão — a árvore "Árvore resultante" abaixo é a
> estrutura real atual do repositório, não mais uma proposta pendente.

## Critério usado

O template sugerido no prompt de auditoria propõe uma subpasta por subtema
do mapa v2 (ex. `/eletrostatica`, `/espelhos-esfericos`). Isso funciona bem
para os 3 arquivos temáticos de eletrostática, que mapeiam 1:1 a subtemas.
Mas boa parte do repositório é formada por **listas de revisão que
propositalmente misturam vários subtemas** (`eletro-revisao-vetores.html`,
`onda-revisao.html`, `termo-revisao-calorimetria.html`) ou por **listas que
cobrem uma trilha inteira de uma área** (`optica-geometrica.html`,
`optica-lentes-aplicada.html`, que juntas atravessam praticamente toda a
seção 5 do mapa). Forçar esses arquivos dentro de uma única subpasta de
subtema classificaria mal o conteúdo.

Por isso a proposta usa duas regras simples (mantendo a estrutura fácil de
editar manualmente, como pede a regra geral do prompt):

1. Arquivo que cobre **um único subtema** do mapa → vai na subpasta
   correspondente àquele subtema.
2. Arquivo de **revisão que mistura subtemas da mesma área** → vai em uma
   subpasta `revisoes/` dentro da área, em vez de ser fatiado ou duplicado
   entre subpastas.

Áreas do mapa sem nenhum arquivo hoje (Mecânica, Física Moderna,
Eletrodinâmica, Magnetismo, Indução/Transformadores, Dilatação,
Propagação de Calor, Gases, Termodinâmica) **não** ganham pasta agora — 
criar pasta vazia não ajuda em nada; a pasta nasce junto com a primeira
lista daquele subtema, quando for gerada (ver `relatorio_cobertura.md`,
seção "Backlog de Listas a Criar").

## Tabela — caminho atual → caminho novo proposto

| Caminho atual | Caminho novo proposto |
|---|---|
| `eletro-cargas-eletricas.html` | `listas/01-eletricidade/eletrostatica/eletro-cargas-eletricas.html` |
| `eletro-eletrizacao.html` | `listas/01-eletricidade/eletrostatica/eletro-eletrizacao.html` |
| `eletro-lei-de-coulomb.html` | `listas/01-eletricidade/eletrostatica/eletro-lei-de-coulomb.html` |
| `eletro-revisao-vetores.html` | `listas/01-eletricidade/revisoes/eletro-revisao-vetores.html` |
| `termo-calorimetria.html` | `listas/02-termologia/calorimetria/termo-calorimetria.html` |
| `termo-equilibrio-mudanca-estado.html` | `listas/02-termologia/calorimetria/termo-equilibrio-mudanca-estado.html` |
| `termo-revisao-calorimetria.html` | `listas/02-termologia/revisoes/termo-revisao-calorimetria.html` |
| `onda-periodo-frequencia.html` | `listas/03-ondulatoria/ondulatoria-geral/onda-periodo-frequencia.html` |
| `onda-comprimento-frequencia.html` | `listas/03-ondulatoria/ondulatoria-geral/onda-comprimento-frequencia.html` |
| `onda-revisao.html` | `listas/03-ondulatoria/revisoes/onda-revisao.html` |
| `optica-geometrica.html` | `listas/05-optica-geometrica/optica-geometrica.html` *(fica na raiz da área — cobre princípios, espelhos planos, espelhos esféricos e refração de uma vez, não um único subtema)* |
| `optica-lentes-aplicada.html` | `listas/05-optica-geometrica/optica-lentes-aplicada.html` *(mesma razão: cobre lentes, vergência, instrumentos e refração aplicada)* |
| `mu_muv.html` | **Não incluído em `/listas`** — não é uma lista no formato padrão (ver `inventario_listas.md`, seção "Não classificados"). Sugestão: `experimentais/mu_muv.html`, ou o professor decide removê-lo/tratá-lo à parte. |
| `index.html` | Mantido na raiz do repositório — será **regenerado depois** da reorganização aprovada (os links `href` para cada lista mudam de raiz para subpasta), conforme a regra do prompt de auditoria. Não precisa ser atualizado nesta etapa. |
| `README.md`, `mapa_conteudos_fisica_enem_v2.md`, `prompt_projeto_fisica.md`, `prompt_progressao_fisica.md`, `prompt_auditoria_code.md` | Mantidos na raiz — são documentação/configuração do projeto, não listas de exercício. |
| `inventario_listas.md`, `relatorio_duplicatas.md`, `relatorio_cobertura.md`, `proposta_estrutura_repositorio.md` (este arquivo) | Mantidos na raiz junto com os demais documentos — ou movidos para uma pasta `/auditoria` ou `/docs`, à escolha do professor. |

## Árvore resultante (se aprovada)

```
/listas
  /01-eletricidade
    /eletrostatica
      eletro-cargas-eletricas.html
      eletro-eletrizacao.html
      eletro-lei-de-coulomb.html
    /revisoes
      eletro-revisao-vetores.html
  /02-termologia
    /calorimetria
      termo-calorimetria.html
      termo-equilibrio-mudanca-estado.html
    /revisoes
      termo-revisao-calorimetria.html
  /03-ondulatoria
    /ondulatoria-geral
      onda-periodo-frequencia.html
      onda-comprimento-frequencia.html
    /revisoes
      onda-revisao.html
  /05-optica-geometrica
    optica-geometrica.html
    optica-lentes-aplicada.html
```

(As pastas `/04-mecanica` e `/06-fisica-moderna` — e as subpastas vazias de
`/01-eletricidade`, `/02-termologia` correspondentes aos subtemas sem
cobertura — nascem quando as primeiras listas desses temas forem criadas.)

## Pontos de atenção antes de executar

- `optica-lentes-aplicada.html` tem um link interno
  `href="optica-geometrica.html"` (botão "← Lista 1"). Como a proposta move
  os dois arquivos juntos para a mesma pasta, **esse link continua
  funcionando sem alteração**. Se um dia forem separados em pastas
  diferentes, o link precisa ser ajustado manualmente.
- `index.html` referencia todos os 12 arquivos por caminho relativo à raiz
  (`href="eletro-cargas-eletricas.html"`, etc.). Mover os arquivos para
  subpastas **quebra esses 12 links** até o `index.html` ser regenerado —
  por isso a regra do prompt de auditoria de tratar a regeneração do índice
  como etapa separada, posterior à aprovação desta reorganização.
- Nenhum arquivo tem gabarito (`.md`) hoje, então não há par lista+gabarito
  para mover junto — só o `.html` de cada lista.
- Execução recomendada: `git mv <caminho atual> <caminho novo>` para cada
  linha da tabela, preservando o histórico do arquivo.
