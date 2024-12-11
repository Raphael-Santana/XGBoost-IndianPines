# Classificação de Imagens Hiperespectrais com XGBoost

Este projeto aplica técnicas de machine learning para classificar imagens hiperespectrais do conjunto de dados **Indian Pines**, utilizando o modelo de **Extreme Gradient Boosting (XGBoost)**. A abordagem combina com o pré-processamento de dados, incluindo a normalização dos dados, redução de dimensionalidade, limpeza de valores nulos e o balanceamento dos dados (oversampling)

## Visão Geral
O conjunto de dados **Indian Pines** é amplamente utilizado em estudos de classificação de imagens hiperespectrais. Ele contém informações espectrais e espaciais de uma região rural capturadas no noroeste da Indiana (Estados Unidos) pelo sensor hiperespectral AVIRIS.

## Etapas do Projeto

### 1. Carregamento e Exploração dos Dados
Os dados são carregados a partir de arquivos `.mat` e analisados para entender a distribuição das classes e suas características espectrais. Visualizações gráficas ajudam a compreender o conjunto de dados antes do pré-processamento.

### 2. Pré-processamento
- **Normalização** das bandas espectrais para garantir uniformidade.
- **Redução de dimensionalidade** utilizando o **PCA** com 22 componentes principais (na qual explica 99% das bandas espectrais).
- **Limpeza de dados** para remover valores nulos.
- **Divisão de treino e teste** para validar o modelo posteriormente
- **Oversampling** para balancear os dados criando dados sintéticos das classes minoritárias

### 3. Treinamento com XGBoost
O modelo é treinado utilizando os dados pré-processados e otimizados. Hiperparâmetros como a profundidade das árvores e a taxa de aprendizado são ajustados para maximizar a performance.

### 4. Avaliação
O desempenho do modelo é avaliado com métricas como:
- **Acurácia**
- **Precisão**
- **F1-Score**

## Tecnologias Utilizadas
- **Python**: Linguagem principal do projeto.
- **XGBoost**: Modelo baseado em árvores de decisão com boosting de gradiente.
- **Pandas e NumPy**: Manipulação e análise de dados.
- **Scikit-learn**: Redução de dimensionalidade e divisão entre treino e teste.
- **Matplotlib**: Visualização na exploração dos dados.
