# Dados do TCC — Análise de Preços em Licitações Públicas no Espírito Santo

Dados utilizados no Trabalho de Conclusão de Curso (Projeto de Graduação II) de **Leonardo Loureiro de Almeida**, sobre análise de discrepâncias de preços em compras públicas (licitações) nas esferas federal, estadual e municipal do Espírito Santo.

## Arquivos

| Arquivo | Descrição |
|---|---|
| `precos_v3_todos.csv` | Base consolidada com todos os registros de preços padronizados (todas as fontes) |
| `precos_v3_federal.csv` | Registros da esfera federal (PNCP / Compras.gov.br) |
| `precos_v3_estadual.csv` | Registros da esfera estadual (ComprasNet ES) |
| `precos_v3_municipal_atas.csv` | Registros municipais — atas de registro de preços (PNCP) |
| `precos_v3_municipal_tcees.csv` | Registros municipais — dados abertos do TCE-ES |
| `precos_v3_municipal_ws.csv` | Registros municipais — web services / portais municipais |
| `precos_padronizados_resumo_v3.csv` | Resumo estatístico por produto/ano/fonte (mediana, média, mín., máx., nº de registros) |
| `stats_v3.json` | Estatísticas gerais do conjunto de dados (totais, distribuição por fonte/ano, municípios) |

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

- **93.337** registros de preços consolidados
- **188** produtos normalizados
- **15** municípios do ES + esferas estadual e federal
- Período: **2019 a 2026**

## Fontes originais

- [PNCP — Portal Nacional de Contratações Públicas](https://pncp.gov.br/)
- [Compras.gov.br — Dados Abertos](https://dadosabertos.compras.gov.br/)
- [TCE-ES — Dados Abertos](https://dados.tce.es.gov.br/)
- ComprasNet ES (Governo do Estado do Espírito Santo)

Os dados são públicos e foram coletados entre 2025 e 2026 por meio das APIs e portais de dados abertos acima.
