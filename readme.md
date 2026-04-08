<img width="240" height="900" alt="image" src="https://github.com/user-attachments/assets/8c29a49c-e361-47b3-a368-7edc658bc000" /># 🏠 Previsão de Preço de Imóveis com Machine Learning

## 📌 Sobre o Projeto

  Este projeto tem como objetivo prever o valor de imóveis com base em características estruturais e geográficas, utilizando técnicas de Machine Learning.
  
  Além da construção do modelo, o foco principal foi a análise crítica dos erros, identificando limitações do dataset e oportunidades de melhoria no modelo.

### 🎯 Objetivo

  Desenvolver um modelo de regressão capaz de prever o preço de imóveis e analisar seu desempenho em diferentes faixas de valor.

### 🧠 Abordagem

  O projeto foi estruturado nas seguintes etapas:
  
  - Exploração dos dados (EDA)
  - Pré-processamento
  - Treinamento do modelo (Random Forest) e baseline (Linear e Dummy)
  - Avaliação com múltiplas métricas
  - Análise de erro por faixa de valor
  - Diagnóstico de problemas no dataset
  
## 📊 Principais Análises

### 📌 Distribuição dos dados

  - O dataset apresenta desbalanceamento
  - Concentração de dados nas faixas intermediárias
  - Baixa representatividade nos extremos (valores baixos e altos)
  
### 📌 Erro por faixa de valor

  O modelo apresenta:
  - Boa performance em valores médios
  - Maior erro em valores baixos
    
  Identificado que:
  - Parte do erro elevado era causado pelo uso de erro percentual (MAPE)
  - Ao utilizar erro absoluto (MAE), o modelo se mostrou mais estável
  
### 📌 Problema identificado no dataset
  - Existe um CAP no valor máximo (5)
  - Imóveis com valores superiores foram truncados

### Impacto:

- Introduz ruído no treinamento
- Dificulta a diferenciação entre imóveis de alto valor
📉 Visualizações

### O projeto inclui análises como:

- Distribuição de dados por faixa (pd.cut)
- Erro médio por faixa de valor
- Dispersão entre valor real vs erro
- Identificação de outliers

## ⚠️ Principais Desafios

- Desbalanceamento do dataset
- Presença de outliers
- Limitação artificial do target (CAP)
- Escolha adequada de métricas de avaliação

## 🚀 Possíveis Melhorias
- Aplicar transformação logarítmica no target
- Utilizar sample weights para balanceamento
- Engenharia de features geográficas
Clusterização por região (latitude/longitude)
- Testar outros modelos (XGBoost, LightGBM)
- Tratamento de outliers

## 🛠 Tecnologias Utilizadas

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib / Seaborn
  
# 📈 Resultado
O modelo apresentou:

- Boa capacidade preditiva nas faixas intermediárias
- Maior dificuldade em regiões com baixa representatividade
- Sensibilidade à métrica utilizada (MAPE vs MAE)
- R² de 0.80 com MAE de 0.33 (explica 80% da variância do target com uma margem de erro absoluto de 0.33 no valor), enquanto o base line foi definido em R² 0.59 com MAE de 0.53 (explica 59% da variância do target com uma margem de erro absoluto de 0.53 no valor)

## Gráficos:

### Dispersão dos dados para indentificação de melhor modelo para os dados
<img width="668" height="549" alt="image" src="https://github.com/user-attachments/assets/04021b34-6e62-48c5-9e08-3ff8d42678d0" />

### Volume de dados por Faixa de Preço do Imóvel
<img width="1187" height="586" alt="image" src="https://github.com/user-attachments/assets/986cbe1a-e739-4d95-977f-c55fec0df490" />

### Valor Médio do Erro por Faixa de Preço
<img width="674" height="626" alt="image" src="https://github.com/user-attachments/assets/c52133b7-30d7-437f-a4c2-24c294e85f22" />

### Identificação da Dispersão dos Erros pelo Preço do Imóvel
<img width="679" height="550" alt="image" src="https://github.com/user-attachments/assets/335bdfc3-35c4-48fe-8110-62d696239b60" />


## 📂 Como executar o projeto
```
# Clone o repositório
git clone https://github.com/HenriqueAntunesAguiar/machine_learn_imoveis.git

# Instale as dependências
pip install -r requirements.txt

# Execute o notebook
jupyter notebook
```
