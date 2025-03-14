# 📊 Análise de Dados da PNS 2019: Desafios da Saúde Brasileira

## 📌 Descrição

Este projeto realiza um processo de **ETL (Extração, Transformação e Carga)** e **análise exploratória** dos dados da **Pesquisa Nacional de Saúde (PNS) 2019**, com o objetivo de construir um **dashboard interativo** no Power BI. O foco é identificar **desafios e tendências na área da saúde no Brasil**, facilitando o acesso e a interpretação de informações relevantes para **pesquisadores, estudantes e profissionais da saúde**.

## 🎯 Objetivos
✅ Facilitar a extração de informações significativas a partir de grandes volumes de dados da PNS 2019.  
✅ Integrar dados de diferentes fontes (objetivo futuro).  
✅ Criar uma ferramenta acessível e intuitiva para visualização e análise de dados da saúde.  
✅ Identificar correlações entre variáveis relacionadas a trabalho, saúde e condições socioeconômicas.  
✅ Disponibilizar um **dashboard interativo** para exploração dos dados.  

## 📂 Estrutura do Repositório
```
📂 etl_pns2019
├── 📁 data              # Dados brutos e transformados
│   ├── pns2019.csv     # Base de dados original
│   ├── PNS_trabalhoXSaude.csv  # Base de dados tratada
│   ├── dicionario_PNS_microdados_2019.csv  # Dicionário dos dados, contendo todos os códigos e suas respectivas perguntas.
│   ├── dicionario_PNS_microdados_2019.csv  # Dicionário dos dados, contendo todos os códigos e suas respectivas perguntas.
│
├── 📁 notebooks        # Notebooks para análise e ETL
│   ├── EDA_completa.ipynb   # Extração, Tratamento, e Análise Exploratória dos dados.
│
├── 📁 dashboards       # Arquivos do Power BI
│   ├── PNS_dashboard.pbix  # Dashboard interativo

├── README.md          # Documentação principal
```

## 🏛 Fonte de Dados
📌 **Pesquisa Nacional de Saúde (PNS) 2019**, disponibilizada pelo **Ministério da Saúde e IBGE**.  
🔗 [Link para a base de dados](#) *(https://www.ibge.gov.br/estatisticas/sociais/saude/29540-2013-pesquisa-nacional-de-saude.html?edicao=9177&t=microdados).*  

## ⚙️ Tecnologias Utilizadas
![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)  
![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)  
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-red?logo=pandas)  
![NumPy](https://img.shields.io/badge/NumPy-Math%20Operations-blue?logo=numpy)  
![Power BI](https://img.shields.io/badge/Power%20BI-Data%20Visualization-yellow?logo=powerbi)  

## 🔍 Metodologia

### 📥 Extração
📂 Os dados foram extraídos do arquivo **pns2019.csv**.

### 🧼 Limpeza e Pré-processamento
✔️ Seleção de **44 colunas** relevantes, dentre as mais de 1000 do dataset.  
✔️ Redução do número de linhas do dataset.  
✔️ Tratamento de valores faltantes (NaN → 0).  
✔️ Renomeação de colunas para melhor compreensão.  
✔️ Mapeamento de códigos para valores descritivos (**sexo, raça/cor, estado**).  

### 🔨 Engenharia de Atributos
🛠️ **Criação da coluna** `total_horas_trabalho`, somando `horas_trabalho_principal` e `horas_trabalho_outros`.

### 📊 Análise Exploratória
 📌 Verificação da proporção de valores nulos.  
📌 Análise de distribuições e estatísticas descritivas.  
📌 Criação de visualizações no **Power BI**.

### 🚀 Transformação (Load)
💾 Os dados tratados foram exportados para um novo arquivo **PNS_trabalhoXSaude.csv** para importação no **Power BI**.

## 📊 Estrutura do Dashboard (Power BI)
📄 **Total de Entrevistas**: 279 Mil 
### 📌 Página 1 (Trabalho e Saúde) 
✅ **Filtros**: Ocupação do Trabalho, Estado, Exposição a Fatores de Risco, Doenças.  
✅ **Visualizações**:
- Uso de Medicamentos p/ Depressão (Homens x Mulheres)
- Relatos de Sentimentos Depressivos (Gráfico de Rosca)
- Diagnósticos por Faixa Etária (Gráfico de barras)
- Diagnósticos por Doença (Diabetes, Hipertensão, Câncer...)
- Internações por Frequência (1 a 6+)
- Percepção da Saúde (Tabela: Bom, Ruim, Regular...)

### 📌 Página 2 (Socioeconômico)
✅ **Visualizações**:
- Consultas no último ano por faixa salarial
- Plano de Saúde por Raça
- População ativa exposta a riscos no trabalho
- Plano de Saúde por Faixa Salarial
- Comparação de depressão entre homens e mulheres
- Exposição a riscos no trabalho (Mapa do Brasil)

## 🎯 Insights Importantes
📌 **Ocupação e Saúde**: Depressão é mais comum entre trabalhadores domésticos, já entre militares apreval~encia é menor.  
      Dos que responderam a pergunta: Sentiu-se deprimido ultimamente, 35,9% dos trabalhadores domésticos relataram que sim, 
      contra 14,44% dos militares.
📌 **Renda e Saúde**: Quanto menor a renda, maior a frequência de consultas médicas.  
📌 **Raça e Plano de Saúde**: Indígenas possuem a menor taxa de cobertura.  
📌 **Sexo e Depressão**: Mulheres têm maior prevalência de diagnósticos.  
📌 **Exposição a Riscos**: Mapa interativo mostra variação por estado.  

---

