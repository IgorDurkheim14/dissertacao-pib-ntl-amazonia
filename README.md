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
