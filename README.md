# 💉 Análise de Vacinação Covid-19: Foco nas Capitais Brasileiras

Este projeto consiste em um painel analítico desenvolvido no **Power BI** para monitorar e comparar a cobertura vacinal contra a Covid-19 nas capitais brasileiras, com um foco estratégico na cidade de **Recife-PE**.

O objetivo foi transformar dados brutos do Vacinômetro e do IBGE em insights acionáveis sobre o desempenho das campanhas de imunização.

![Print Principal do Dashboard]()

## 📊 Visão Geral do Projeto

O desafio propôs a análise de duas bases de dados distintas para gerar indicadores de saúde pública. O painel final permite:
- Visualizar o **Ranking Nacional** de cobertura vacinal completa.
- Filtrar dados dinamicamente por **Região** (Norte, Nordeste, Sul, etc.).
- Comparar o desempenho de **Recife** contra médias e medianas nacionais.
- Identificar discrepâncias entre população residente e doses aplicadas.

## 🛠️ Tecnologias e Técnicas Utilizadas

- **Power BI Desktop:** Ferramenta principal de Dataviz e ETL.
- **Power Query:** Limpeza e tratamento de dados.
- **Modelagem de Dados:** Criação de relacionamentos (Esquema Estrela) entre tabelas de Fato (Vacinômetro) e Dimensão (IBGE) usando a chave `COD_IBGE`.
- **DAX (Data Analysis Expressions):**
  - Criação de métricas calculadas (`% Cobertura Completa`, `Total Doses`).
  - Utilização de funções estatísticas avançadas (`AVERAGEX`, `MEDIANX`) para traçar linhas de referência dinâmicas.
  - Funções de inteligência de tempo e divisão segura.
- **UX/UI Design:** Foco em clareza, uso de KPIs, formatação condicional e interatividade (Drill-down e Tooltips).

## 💡 Principais Insights da Análise

Durante a exploração dos dados, quatro pontos principais foram identificados:

1.  **O Fenômeno >100% em Recife:** Recife apresenta uma cobertura vacinal superior a 103%. A análise indica que isso se deve ao efeito de "Polo Metropolitano", onde a capital absorve a demanda vacinal de cidades vizinhas (população flutuante), inflando o numerador (doses) em relação ao denominador (população residente IBGE).
2.  **Liderança do Nordeste:** Fortaleza lidera o ranking nacional, seguida por Recife no contexto regional, demonstrando forte adesão no Nordeste.
3.  **Disparidade Nacional:** Existe um gap de mais de 120 pontos percentuais entre a capital com maior cobertura e a com menor (Boa Vista-RR).
4.  **Média vs. Mediana:** Devido a *outliers* positivos (como Fortaleza com 190%), a média nacional foi puxada para cima. Para uma análise mais realista, utilizou-se a **Mediana** como linha de corte no dashboard, posicionando Recife confortavelmente no quartil superior.

## 📂 Estrutura dos Arquivos

- `dataset/`: Arquivos CSV utilizados (Dados públicos do Vacinômetro e IBGE/Censo).
- `dashboard/`: Arquivo `.pbix` com o projeto completo (Editável).
- `images/`: Capturas de tela do relatório.

## 🚀 Próximos Passos (Roadmap de Data Science)

Como evolução deste projeto para uma abordagem de Ciência de Dados Preditiva, planejo:
- [ ] Enriquecer o dataset com dados socioeconômicos (IDH, Renda per capita).
- [ ] Utilizar **Python (Pandas/Scikit-learn)** para analisar correlações entre IDH e taxa de vacinação.
- [ ] Criar um modelo de clusterização para agrupar municípios com perfis de vacinação semelhantes.

---
*Desenvolvido por André [Seu Sobrenome]*
