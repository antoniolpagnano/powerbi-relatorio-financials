# 📊 Relatório Financials | Power BI

> Relatório interativo construído sobre a base **sample financials** do Power BI, com navegação por botões, indicadores e visuais alternáveis.

![Página 1 do relatório](pagina-1.png)

## 📌 Sobre o projeto

Projeto desenvolvido como parte do desafio **"Criando um Relatório Gerencial com Power BI"** da [DIO](https://www.dio.me/).

A proposta era ir além de um relatório simples: construir uma estrutura de páginas definida, com navegabilidade por botões, segmentadores com imagem associada e indicadores que permitem alternar entre diferentes visuais sobre um mesmo assunto.

## 🗂️ Estrutura do relatório

### Página 1 — Visão Geral
Painel executivo com os indicadores do negócio e visuais alternáveis.

| Elemento | Descrição |
|---|---|
| **Cards de indicadores** | Métricas principais: Sales, Profit, Units Sold, Gross Sales, COGS e Discounts |
| **Segmentador** | Filtro por período/categoria aplicado a todos os visuais da página |
| **Gráfico de área** | Evolução de vendas ao longo do tempo |
| **Gráficos de barras** | Comparação por Produto e por Segmento |
| **Visual alternável** | Rosca, barras, mapa ou treemap, selecionados pelos botões |
| **Botão de navegação** | Avança para a Página 2 |

### Página 2 — Análise Detalhada
Página de aprofundamento, com visuais analíticos e customizados.

| Elemento | Descrição |
|---|---|
| **Chiclet Slicer** | Segmentador com imagem associada (visual customizado) |
| **Árvore hierárquica** | Decomposição do resultado por dimensões (Decomposition Tree) |
| **Gráfico cascata** | Composição do lucro (Waterfall) |
| **Gráfico radar** | Comparativo multidimensional (visual customizado) |
| **Treemap** | Participação por categoria |
| **Botão de navegação** | Retorna à Página 1 |

## 🔘 Navegação e indicadores

O relatório usa **indicadores (bookmarks)** acionados por botões, permitindo ver o mesmo assunto sob diferentes perspectivas sem sair da página:

| Botão | Visual exibido |
|---|---|
| Pie Chart | Gráfico de rosca |
| Bar Chart | Gráfico de barras |
| Map Chart | Mapa geográfico |
| Treemap | Treemap |
| Clean Data | Limpa a seleção e restaura o estado inicial |

A navegação entre as páginas é feita por botões de seta, com ação **Navegação de Página**.

## 🧮 Base de dados

Base **financials** (amostra oficial do Power BI), com as dimensões e métricas:

- **Dimensões:** Country, Product, Segment, Date (com hierarquia de Ano, Trimestre, Mês e Dia)
- **Métricas:** Sales, Gross Sales, Profit, COGS, Units Sold, Discounts

Arquivos de dados disponíveis em: [julianazanelatto/power_bi_analyst](https://github.com/julianazanelatto/power_bi_analyst)

## 🖼️ Visuais customizados

Importados do AppSource:

- **Chiclet Slicer** — segmentador em formato de botões com imagem
- **Radar Chart** — comparativo em teia

Ao abrir o arquivo, o Power BI Desktop carrega esses visuais automaticamente.

## 📂 Arquivos

```
powerbi-relatorio-financials/
├── README.md
├── Relatorio_Financials.pbix
├── pagina-1.png
└── pagina-2.png
```

➡️ **[Baixar o arquivo .pbix](Relatorio_Financials.pbix)**

### Página 2 — Análise Detalhada

![Página 2 do relatório](pagina-2.png)

## 🚀 Como abrir

1. Baixe e instale o [Power BI Desktop](https://powerbi.microsoft.com/pt-br/desktop/) (gratuito).
2. Baixe o arquivo `Relatorio_Financials.pbix` deste repositório.
3. Abra o arquivo. Os visuais customizados são carregados junto com o relatório.

## 🛠️ Recursos aplicados

- Estrutura de páginas com layout definido em 1920x1080
- Botões de navegação entre páginas
- Indicadores (bookmarks) para alternar visuais
- Segmentadores de dados e chiclet slicer com imagem
- Visuais customizados do AppSource
- Formas e caixas de texto para composição do layout

## 🙋 Autor

**Antônio Leite Pagnano**

