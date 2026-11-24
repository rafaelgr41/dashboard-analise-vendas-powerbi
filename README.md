# Dashboard de Análise de Vendas (2014–2017) — Power BI

## Objetivo do Projeto
Desenvolver um painel executivo interativo para análise do histórico comercial entre 2014 e 2017, consolidando indicadores financeiros, sazonalidade, desempenho da equipe comercial, portfólio de produtos e distribuição geográfica para apoiar a tomada de decisão estratégica.

## Ferramentas Utilizadas
* **Power BI Desktop:** Desenvolvimento do painel interativo, hierarquia visual e segmentações dinâmicas.
* **Power Query:** ETL, limpeza de inconsistências, tipagem de colunas e criação de colunas auxiliares.
* **DAX (Data Analysis Expressions):** Criação de medidas calculadas, indicadores de rentabilidade, rankings e inteligência de tempo.

## Arquitetura e Modelagem Dimensional (Star Schema)
* **ETL no Power Query:** Padronização de tipos de dados, tratamento de valores nulos e estruturação de chaves relacionais.
* **Modelo Estrela (Star Schema):** Tabela fato central (`Vendas`) relacionada a dimensões de negócio (`Calendario`, `RepresentanteVendas`, `Geografia` e hierarquia `Produto` → `SubCategorias` → `Categorias`), garantindo integridade nas agregações e performance nas filtragens cruzadas.

### Diagrama do Modelo Dimensional
<img width="573" height="329" alt="powerbi modelo estrela" src="https://github.com/user-attachments/assets/a84d6cec-75f5-4ebc-a935-b13428509a12" />

## Visualização do Dashboard

### Página 1 — Visão Executiva: Performance Financeira e Evolução
Apresenta os cartões de KPIs principais (Receita Total, Lucro Bruto, Margem Bruta % e Crescimento YoY %), segmentadores dinâmicos (Ano, País e Categoria), evolução mensal por ano, ranking de receita por país e participação por categoria.

<img width="719" height="330" alt="powerbi p1 visão executiva" src="https://github.com/user-attachments/assets/40412d63-05bc-4d45-b2a5-6434fe3fe5d5" />

### Página 2 — Performance Comercial: Vendedores, Subcategorias e Matriz Regional
Detalha o ranking da equipe de vendas (com Margem Bruta, Lucro Bruto e Receita Total), árvore hierárquica e treemap por subcategoria de produto, além de matriz cruzando receita e margem por país e categoria.

<img width="644" height="333" alt="powerbi p2 vendedores e produtos" src="https://github.com/user-attachments/assets/af059b4b-bc92-481b-b33a-32639d87a197" />

### Página 3 — Síntese Executiva, Recomendações e Documentação DAX
Consolida os principais diagnósticos de negócio, recomendações acionáveis para expansão comercial e a documentação técnica de todas as medidas DAX implementadas no modelo.

<img width="509" height="308" alt="powerbi p3 insights e recomendações" src="https://github.com/user-attachments/assets/6337487f-534c-47f4-9630-ba5f62a40a85" />

## Principais Resultados e Insights
* **Indicadores Financeiros Consolidados:** O período analisado totalizou **R$ 73,65 milhões em Receita Total**, **R$ 35,66 milhões em Lucro Bruto** e **Margem Bruta média de 48,41%**.
* **Crescimento Consistente:** A receita evoluiu de R$ 16,8 milhões (2014) para R$ 22,9 milhões (2017), registrando **crescimento anual (YoY) de 45,08%**.
* **Concentração Geográfica e Oportunidades:** **Argentina (31,8%) e Colômbia (27,3%)** respondem juntas por quase **60% da receita**. Já **Brasil (6,0%) e Peru (4,2%)** apresentam menor participação atual, destacando-se o Peru pela maior margem bruta do portfólio (**49,26%**), sinalizando oportunidade de replicação de mix e expansão comercial.
* **Sazonalidade e Portfólio:** Os picos de vendas ocorrem em **julho** e os vales em **fevereiro**, orientando o planejamento de estoque e campanhas. No portfólio, a categoria **"Especial"** gera **64,47% das vendas** (R$ 47,48 milhões), liderada pela subcategoria **"Extra Grande"** (R$ 36,77 milhões).
* **Desempenho Comercial:** As vendedoras **Ellen Viana** (R$ 20,10 milhões) e **Bruno Dias** (R$ 15,92 milhões) lideram o faturamento da equipe, mantendo margens brutas consistentes acima de 48,4%.

## Arquivos do Projeto
* `pratique_powerbi.pbix` — Arquivo completo do Power BI Desktop contendo o tratamento no Power Query, modelo estrela, medidas DAX e visualizações.
