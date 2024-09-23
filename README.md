# Case de Predição de Fraudes em Transações de Cartão de Crédito 💳

## Contexto:

Me coloco no lugar de um cientista de dados em uma instituição financeira renomada. A empresa está enfrentando um aumento significativo nas transações fraudulentas de cartões de crédito, o que está prejudicando a confiança dos clientes e causando prejuízos financeiros. Sua tarefa é desenvolver um modelo preditivo que possa identificar transações fraudulentas com alta precisão, minimizando assim o impacto financeiro e protegendo a reputação da instituição.

## Base de Dados:

"**fraud_dataset.csv**", que contém informações detalhadas sobre as transações de cartões de crédito. 

## Objetivo:

Desenvolver um modelo preditivo utilizando o algoritmo de Regressão Logística com regularização L2 para prever se uma transação de cartão de crédito é fraudulenta ou não.

**Realize os seguintes passos na sua entrega:**

- Pré-processamento de Dados:
  - Verifique se a base de dados contém informações nulas.
  - Considere a padronização de variáveis numéricas.
- Divisão da Base de Dados:
  - Separe a base de dados utilizando a técnica hold out, mantendo uma proporção adequada para garantir a representatividade dos dados.
  - Caso a base de dados tenha algum tipo de desequilíbrio, aplique uma técnica de oversampling para equilibrar as classes.
- Modelagem:
  - Implemente o algoritmo de Regressão Logística com regularização L2.
  - Utilize a técnica de validação cruzada k-fold (com 5 folds) para avaliar o desempenho do modelo.
- Avaliação do Modelo:
  - Avalie o modelo utilizando métricas como precisão, recall, F1-score e área sob a curva ROC (AUC-ROC).
- Interpretação e Comunicação de Resultados:
  - Comunique os resultados de forma clara e acessível para as partes interessadas, destacando a eficácia do modelo na identificação de transações fraudulentas.

# Além do objetivo proposto

Pretendo implementar uma classificação usando LightGBM e comparar o resultados

# LightGBM

Boosting é uma técnica de ensemble que cria um modelo preditivo forte a partir de uma combinação de vários modelos fracos. Ao contrário do Bagging, onde os modelos são treinados de forma independente, o Boosting treina modelos de forma sequencial. Cada novo modelo tenta corrigir os erros cometidos pelos modelos anteriores, resultando em um modelo final mais preciso e robusto.

## Como o Boosting Funciona:

1. Modelo Inicial:

  - O processo começa com a criação de um modelo fraco (geralmente uma árvore de decisão simples). Um modelo fraco é um modelo que, por si só, tem desempenho ligeiramente melhor que uma escolha aleatória.
2. Pesos e Erros:

  - Após o primeiro modelo ser treinado, o Boosting atribui pesos maiores às observações que foram incorretamente classificadas ou previstas. Isso significa que as observações que foram difíceis de prever terão mais importância na próxima rodada de treinamento.

3. Modelo Sequencial:

  - Um novo modelo é treinado com base nos dados ajustados (ou seja, com os pesos atualizados). Esse novo modelo tenta corrigir os erros do modelo anterior, focando mais nos casos onde o primeiro modelo falhou.

4. Combinação de Modelos:

  - O processo continua de forma iterativa, adicionando novos modelos que tentam corrigir os erros de seus predecessores.
    O modelo final é obtido através da combinação ponderada dos modelos fracos, onde os modelos que têm melhor desempenho recebem maior peso na predição final.
    
5. Resultado Final:

  - O modelo final é uma "soma ponderada" de todos os modelos fracos, resultando em um modelo preditivo forte que geralmente tem alta precisão.

### Como funciona o Gradient Boosting:

  - Esta técnica ajusta modelos sequenciais para minimizar o erro residual do modelo anterior, utilizando técnicas de otimização de gradiente.

## Como funciona o Light GBM:

  - É uma implementação otimizada do algoritmo de boosting, projetada para ser mais eficiente, rápida e escalável do que outras abordagens de gradient boosting, como o GBM tradicional.
  - LightGBM usa um conceito de boosting semelhante ao GBM, onde várias árvores de decisão são ajustadas sequencialmente, com cada nova árvore corrigindo os erros das árvores anteriores. O objetivo é minimizar uma função de perda através de iterações.
 

