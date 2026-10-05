# 📊 Relatório Financials | Power BI

> Relatório interativo construído sobre a base **sample financials** do Power BI, com menu de navegação persistente, indicadores e visuais alternáveis — em três páginas.

![Página 1 — Sales Report](pagina-1.png)

---

## 📌 Sobre o projeto

Projeto desenvolvido ao longo de dois desafios da [DIO](https://www.dio.me), na Formação Power BI Analyst:

| Desafio | O que acrescentou |
|---|---|
| **Criando um Relatório Gerencial com Power BI** | A estrutura de páginas, os indicadores que alternam visuais e os segmentadores com imagem |
| **Atualizando Relatório Financeiro com Foco na Experiência do Usuário** | O redesenho visual, o menu de navegação em todas as páginas e a terceira página analítica |

A proposta do primeiro era ir além de um relatório simples: construir uma estrutura de páginas definida, com navegabilidade por botões, segmentadores com imagem associada e indicadores que permitem alternar entre diferentes visuais sobre um mesmo assunto.

O segundo manteve toda essa base e atacou a **experiência de quem lê** — como a informação se posiciona na tela, como o olho é guiado, e como a navegação deixa de ser um botão solto para virar um menu presente em qualquer ponto do relatório.

---

## 🎨 A atualização de experiência do usuário

O desafio propõe quatro princípios. O que cada um mudou aqui:

**Posicionamento.** Os indicadores saíram de posições dispersas e passaram a ocupar a faixa superior da área de conteúdo, onde o olho chega primeiro. Abaixo deles vem a evolução temporal, e só então o detalhamento por categoria — do agregado ao específico, de cima para baixo.

**Contraste.** A faixa lateral em azul-marinho profundo contra a área de conteúdo clara separa navegação de informação sem precisar de bordas ou títulos explicando o que é o quê. Os cards de indicadores repetem o mesmo marinho, o que os amarra visualmente ao menu e os destaca do fundo claro.

**Proporção áurea.** A divisão entre a faixa de navegação e a área de conteúdo, e entre a faixa de indicadores e os gráficos abaixo dela, segue proporções aproximadamente áureas em vez de metades iguais. O resultado é um layout que não parece dividido ao meio — parece composto.

**Segmentação dos dados.** Na página 1, o filtro de período ficou junto do título, com um botão **CLEAR** ao lado para desfazer a seleção sem procurar onde clicar. Na página 2, os segmentadores de ano ganharam destaque próprio no canto superior esquerdo, antes dos visuais que eles controlam.

> Como o próprio desafio observa, não são regras rígidas. Alguns visuais rompem a grade de propósito — é o que evita que o relatório fique simétrico demais e, por consequência, sem hierarquia.

---

## 🧭 Menu de navegação

Cada uma das três páginas tem o mesmo menu na faixa lateral esquerda, com botões para **Page 1**, **Page 2** e **Page 3**. Estar sempre no mesmo lugar é o que torna a navegação previsível: o leitor não procura como sair de onde está.

Os botões usam os três estados que o Power BI oferece, e cada um comunica uma coisa diferente:

| Estado | Quando aparece | O que comunica |
|---|---|---|
| **Padrão** | Em repouso | Destino disponível |
| **Focalizar** | Ao passar o mouse | "Este é clicável" |
| **Selecionado** | Na página atual | "Você está aqui" |

A ação de cada botão é **Navegação de Página**.

---

## 📁 Estrutura do relatório

### Página 1 — Sales Report

Painel executivo com os indicadores do negócio e visuais alternáveis.

| Elemento | Descrição |
|---|---|
| Cards de indicadores | Sales, Units Sold, Discounts, Gross Sales e COGS |
| Segmentador de data | Intervalo de período no topo, com botão **CLEAR** para limpar a seleção |
| Gráfico de área | Evolução de Sales ao longo dos meses |
| Gráfico de barras | Soma de Sales por Product |
| Visual alternável — segmento | Rosca ou barras, pelos botões *Pie Chart* e *Bar Chart* |
| Visual alternável — país | Treemap ou mapa, pelos botões *Treemap* e *Map Chart* |
| Menu lateral | Navegação para as páginas 2 e 3 |

### Página 2 — Profit Report

Página de aprofundamento, com visuais analíticos e customizados.

| Elemento | Descrição |
|---|---|
| Segmentadores de ano | 2013 e 2014, em destaque antes dos visuais |
| Segmentadores de dimensão | Ano, Country e Mês |
| Árvore hierárquica | Decomposição do lucro por dimensões (Decomposition Tree) |
| Gráfico radar | Soma de Profit por Product (visual customizado) |
| Treemap | Soma de Profit por Segment |
| Gráfico cascata | Composição do lucro por trimestre (Waterfall) |
| Menu lateral | Navegação para as páginas 1 e 3 |

### Página 3 — Report de Vendas Detalhado

Página criada no desafio de experiência do usuário, com foco em leitura temporal e detalhamento tabular.

| Elemento | Descrição |
|---|---|
| Gráfico combinado | Soma de Sales em colunas e Soma de Gross Sales em linha, por mês, com rótulos de dados |
| Visual alternável | Botões *Vendas Gross X Período* e *Vendas e Lucro X Período* trocam a métrica comparada |
| Matriz de vendas | Trimestre nas linhas, ano nas colunas, com subtotais e total geral, expansível por hierarquia |
| Menu lateral | Navegação para as páginas 1 e 2 |

![Página 3 — Report de Vendas Detalhado](pagina-3.png)

---

## ⚪ Indicadores e visuais alternáveis

O relatório usa **indicadores (bookmarks)** acionados por botões, permitindo ver o mesmo assunto sob diferentes perspectivas sem sair da página nem perder o contexto dos filtros aplicados:

| Botão | Visual exibido | Página |
|---|---|---|
| Pie Chart | Gráfico de rosca por segmento | 1 |
| Bar Chart | Gráfico de barras por segmento | 1 |
| Treemap | Treemap por país | 1 |
| Map Chart | Mapa geográfico por país | 1 |
| CLEAR | Limpa a seleção e restaura o estado inicial | 1 |
| Vendas Gross X Período | Sales e Gross Sales por mês | 3 |
| Vendas e Lucro X Período | Sales e Profit por mês | 3 |

---

## 🗄️ Base de dados

Base **financials** (amostra oficial do Power BI), com as dimensões e métricas:

- **Dimensões:** Country, Product, Segment, Date (com hierarquia de Ano, Trimestre, Mês e Dia)
- **Métricas:** Sales, Gross Sales, Profit, COGS, Units Sold, Discounts

Arquivos de dados disponíveis em: [julianazanelatto/power_bi_analyst](https://github.com/julianazanelatto/power_bi_analyst)

---

## 🖼️ Visuais customizados

Importados do AppSource:

- **Chiclet Slicer** — segmentador em formato de botões com imagem
- **Radar Chart** — comparativo em teia

Ao abrir o arquivo, o Power BI Desktop carrega esses visuais automaticamente.

---

## 📂 Arquivos

```
powerbi-relatorio-financials/
├── README.md
├── Relatorio_Financials.pbix
├── pagina-1.png
├── pagina-2.png
└── pagina-3.png
```

[⬇️ Baixar o arquivo .pbix](Relatorio_Financials.pbix)

![Página 2 — Profit Report](pagina-2.png)

---

## 🚀 Como abrir

1. Baixe e instale o [Power BI Desktop](https://powerbi.microsoft.com/pt-br/desktop/) (gratuito).
2. Baixe o arquivo `Relatorio_Financials.pbix` deste repositório.
3. Abra o arquivo. Os visuais customizados são carregados junto com o relatório.

---

## 🛠️ Recursos aplicados

- Estrutura de três páginas com layout definido em 1920x1080
- Menu de navegação lateral replicado em todas as páginas
- Botões com estados de **padrão**, **focalizar** e **selecionado**
- Indicadores (bookmarks) para alternar visuais sem trocar de página
- Segmentadores de data, de dimensão e chiclet slicer com imagem
- Matriz com hierarquia de tempo e subtotais
- Gráfico combinado de colunas e linha
- Visuais customizados do AppSource
- Composição de layout por formas, faixas de cor e caixas de texto
- Princípios de posicionamento, contraste, proporção áurea e segmentação

---

## 👨‍💻 Autor

**Antônio Leite Pagnano**
