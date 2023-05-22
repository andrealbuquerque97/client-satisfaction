# Análise de Satisfação do Cliente e Previsão de Churn

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

Bem-vindo ao meu projeto de análise de satisfação de clientes e previsão de churn! Este projeto é baseado na competição "Santander Customer Satisfaction" do Kaggle, onde meu objetivo foi desenvolver um modelo de aprendizado de máquina para identificar clientes insatisfeitos e prever a probabilidade de churn (cancelamento) em uma instituição financeira.

## Contexto e Importância

Em um mundo altamente competitivo, a satisfação do cliente é um fator crucial para o sucesso de qualquer negócio. Instituições financeiras, como bancos, estão constantemente buscando maneiras de melhorar seus serviços e reter clientes fiéis. Identificar clientes insatisfeitos e prever o churn com antecedência pode permitir que as empresas adotem medidas proativas para mitigar esses riscos, aumentar a retenção e melhorar a experiência do cliente.

Este projeto busca oferecer uma solução eficiente e precisa para enfrentar esse desafio. Utilizando técnicas de análise de dados e aprendizado de máquina, analisamos um conjunto de dados abrangente fornecido pela competição Kaggle e construímos um modelo preditivo capaz de identificar com precisão os clientes com maior probabilidade de churn.

## Conhecimentos Abordados no Projeto

- **Exploração de Dados:** Os dados fornecidos são anonimizados e portanto não é possível conhecer profundamente o que representa cada coluna. Desse modo, a exploração dos dados é feita de forma puramente estatística e numérica, avaliando possíveis outliers e colunas com maior relevância para o modelo preditivo.
 

- **Pré-processamento e Engenharia de Recursos:** Foram testadas as técnicas de **Variance Thresholding** onde mantemos apenas colunas que têm uma variância acima de um limite específico e **Principal Component Analysis**

- **Modelagem Preditiva:** O modelo escolhido para esse projeto por motivo de simplicidade e explanabilidade foi a **Regressão Logística**, que atingiu um resultado considerável apesar das suas limitações. Foi construída uma pipeline onde os dados passavam primeiramente por técnicas de undersampling e oversampling, visando corrigir o desbalanceamento dos dados (havia muito mais dados de clientes que não abandonaram o banco). Posteriormente, utilizamos o PCA para formar as componentes principais do modelo e por último passamos o resultado para um modelo de Regressão Logística. Essa pipeline então foi treinada utilizando validação cruzada e o método de busca aleatória para encontrar os melhores hiperparâmetros.


- **Avaliação e Interpretação de Resultados:** Analisei cuidadosamente as métricas de desempenho do modelo, como precisão, recall e área sob a curva ROC. Também conduzi uma análise de importância de recursos para entender quais variáveis tiveram maior impacto nas previsões. Por último, submeti as previsões no conjunto de teste para a API do kaggle a fim de obter os resultados do modelo, obtendo um score público de 0.735 e um score privado de 0.723.

- **Futuros Desenvolvimentos:** Utilizar modelos mais avançados de aprendizado de máquina, como Random Forests, XGBoost e Redes Neurais Profundas. Além disso, podem ser testadas outras abordagens de engenharia de recursos para obter features mais significativas para o projeto.

## Como Usar o Projeto

Para reproduzir e explorar este projeto em sua máquina local, siga estas etapas simples:

1. Faça um clone deste repositório para o seu ambiente de desenvolvimento.
   ```
   git clone https://github.com/andrealbuquerque97/client-satisfaction.git