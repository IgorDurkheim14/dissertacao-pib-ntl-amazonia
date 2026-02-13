# dissertacao-pib-ntl-amazonia
Pipeline de processamento de dados e Machine Learning para Nowcasting do PIB na Amazônia Legal usando luminosidade noturna

# Nowcasting do PIB na Amazônia Legal via Machine Learning e NTL

Este repositório contém o pipeline de processamento de dados da minha dissertação de mestrado (PPGOM/UFPel). O objetivo é prever a atividade econômica municipal utilizando dados de luminosidade noturna (*Nighttime Lights* - NTL).

## 📌 Diferenciais Metodológicos
* **Harmonização Territorial:** Uso de Áreas Mínimas Comparáveis (AMCs) do IPEA para garantir a replicabilidade e consistência diante da emancipação de municípios (1991-2010).
* **Tratamento Monetário:** Deflação da série histórica (2002-2020) via IPCA a preços de 2023, utilizando o pacote `deflatebr`.
* **Escalabilidade:** Código desenvolvido para execução em nuvem e integrado ao Google Drive.

## 🛠️ Tecnologias Utilizadas
* **Python 3.10+**
* **Bibliotecas Espaciais:** `geobr`, `geopandas`
* **Tratamento de Dados:** `pandas`, `numpy`, `deflatebr`

## 📊 Estrutura do Dataset Final
O output gerado consolida 15.420 registros originais em 270 unidades territoriais estáveis (AMCs), contendo:
* `pib_real`: PIB deflacionado (Target)
* `sum_ntl`: Soma da luminosidade noturna (Feature principal)
* `amc_code`: Identificador único padronizado pelo IPEA.

Nowcasting do PIB na Amazônia Legal via Machine Learning 🌲📈
Este repositório contém os notebooks e a metodologia da minha dissertação de mestrado em Economia Aplicada (UFPEL). O projeto foca na construção de uma série histórica consistente de PIB para os municípios da Amazônia Legal entre 1992 e 2023, utilizando modelos de Machine Learning para superar as limitações de dados estáticos e luminosidade noturna.

🎯 Objetivo do Projeto
O problema central da pesquisa busca avaliar o poder preditivo de modelos de aprendizado de máquina na estimativa do PIB municipal, integrando dados de mercado de trabalho formal (RAIS) e infraestrutura (Luz Noturna).

📂 Estrutura dos Notebooks
03_modelagem_avancada_pib_rais.ipynb: Extração de dados via API (Base dos Dados), integração de microdados da RAIS e treinamento do modelo Random Forest. Alcançou uma redução significativa no erro médio (MAPE) ao incluir variáveis salariais.

04_analise_resultados_pib_amazonia.ipynb: Análise de performance, validação de resultados para os principais polos econômicos e geração de visualizações em escala logarítmica.

🛠️ Tecnologias Utilizadas
Linguagem: Python (VSCode + Jupyter Notebooks).

Bibliotecas: pandas, scikit-learn, basedosdados, matplotlib, joblib.

Infraestrutura: Google Cloud / BigQuery (via Base dos Dados).

📊 Principais Resultados
O modelo integra dados de 10.056 registros de municípios da Amazônia.

Redução drástica do erro de estimativa (MAPE) de 224% (baseline apenas com luz) para 64,52% (modelo integrado com RAIS).

Alta acurácia em polos industriais e urbanos, com erros individuais abaixo de 11% em grandes capitais.
