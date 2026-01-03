# Pipeline de Dados para Cotação do Bitcoin usando Python, SQL e Databricks

Este projeto tem como objetivo consumir uma API pública para obter a cotação atual do Bitcoin, realizando o processamento e armazenamento dos dados utilizando Python, SQL e Databricks. A solução demonstra uma pipeline de dados básica, desde a ingestão até a persistência das informações para análise.

## Arquitetura do Projeto

```mermaid
flowchart TB
    A["🌐 API Coinbase<br/><b>Bitcoin USD</b>"] --> E["📥 EXTRACT"]
    B["🌐 API CurrencyFreaks<br/><b>USD-BRL Rate</b>"] --> E
    E --> T["🔄 TRANSFORM<br/>• Convert USD→BRL<br/>• Add timestamp<br/>• Structure data"]
    T --> L["💾 LOAD<br/>Delta Table<br/>Unity Catalog"]
    L --> W["⚙️ WORKFLOW<br/>Databricks Jobs<br/>Automação"]
    W --> D["📊 DASHBOARD<br/>Visualizações<br/>Métricas em Tempo Real"]

```

## Componentes do Projeto:

    📥 EXTRACT: Extração de dados de 2 APIs (Coinbase e CurrencyFreaks)
    🔄 TRANSFORM: Conversão de moedas e estruturação de dados
    💾 LOAD: Armazenamento em Delta Table no Unity Catalog
    ⚙️ WORKFLOW: Automação via Databricks Jobs & Pipelines
    📊 DASHBOARD: Visualização interativa com métricas e gráficos

## Job para automatização 

<img width="1867" height="933" alt="image" src="https://github.com/user-attachments/assets/1c3e6b5f-383b-4549-8c6c-38e81e353872" />

## Dashboard para visualização de resultados

<img width="1857" height="928" alt="image" src="https://github.com/user-attachments/assets/a9a067b0-1410-46bf-808a-8f07224c86d3" />
