# Dados do TCC — Análise de Preços em Licitações Públicas no Espírito Santo

Dados utilizados no Trabalho de Conclusão de Curso (Projeto de Graduação II) de **Leonardo Loureiro de Almeida**, sobre análise de discrepâncias de preços em compras públicas (licitações) nas esferas federal, estadual e municipal do Espírito Santo.

A base consolidada reúne **102.634 registros de itens de licitação**, coletados de fontes públicas oficiais, abrangendo o período de **2019 a 2026**.

## Arquivos

| Arquivo | Registros | Descrição |
|---|---|---|
| `precos_v3_todos.csv` | 102.634 | Base consolidada com todos os registros de preços padronizados (todas as fontes) |
| `precos_v3_federal.csv` | 7.860 | Registros da esfera federal (PNCP / Compras.gov.br) |
| `precos_v3_estadual.csv` | 14.149 | Registros da esfera estadual (ComprasNet ES) |
| `precos_v3_municipal_atas.csv` | 27.626 | Registros municipais — atas de registro de preços (PNCP) |
| `precos_v3_municipal_tcees.csv` | 48.908 | Registros municipais — dados abertos do TCE-ES |
| `precos_v3_municipal_ws.csv` | 4.091 | Registros municipais — web services / portais municipais |
| `precos_padronizados_resumo_v3.csv` | 2.578 | Resumo estatístico por produto/ano/fonte (mediana, média, mín., máx., nº de registros) |
| `stats_v3.json` | — | Estatísticas gerais do conjunto de dados (totais, distribuição por fonte/ano, municípios) |

## Estrutura dos dados

Colunas dos arquivos `precos_v3_*.csv`:

- `fonte` — esfera de origem (federal, estadual, municipal)
- `produto` — produto normalizado (ex.: diesel, arroz, dipirona)
- `ano` — ano da contratação (2019–2026)
- `cidade` — município ou esfera (ex.: Vitória, Federal/ES)
- `preco_padrao` — preço unitário padronizado
- `unidade_padrao` — unidade de medida padronizada (litro, kg, unidade etc.)
- `fonte_conversao` — regra utilizada na conversão de unidade
- `descricao` — descrição original do item na licitação

## Números gerais

- **102.634** registros de itens de licitação consolidados
  - Federal: 7.860 | Estadual: 14.149 | Municipal: 80.625
- **93.337** registros efetivamente utilizados no cálculo das medianas (após corte dos percentis 5–95 para remoção de outliers)
- **2.578** medianas de preço (combinações produto × ano × fonte)
- **188** produtos normalizados
- **15** municípios do ES + esferas estadual e federal
- Período: **2019 a 2026**

## Fontes originais

- [PNCP — Portal Nacional de Contratações Públicas](https://pncp.gov.br/)
- [Compras.gov.br — Dados Abertos](https://dadosabertos.compras.gov.br/)
- [TCE-ES — Dados Abertos](https://dados.tce.es.gov.br/)
- ComprasNet ES (Governo do Estado do Espírito Santo)

Os dados são públicos e foram coletados entre 2025 e 2026 por meio das APIs e portais de dados abertos acima.
