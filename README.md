# House Prices
Este repositório foi desenvolvido como parte da avaliação da pós-graduação em Ciência de Dados e Analytics (PUC-Rio).
O objetivo é prever o preço de venda de imóveis utilizando o conjunto de dados da competição House Prices: Advanced Regression Techniques (Kaggle).

Dados e regras da competição: Kaggle – House Prices: Advanced Regression Techniques.

🎯 Objetivo

Construir um pipeline de Machine Learning para estimar o SalePrice a partir de variáveis estruturais, de qualidade e localização, avaliando modelos e comparando resultados com a métrica oficial da competição (RMSE do log do preço).

🗂️ Dataset

Train: contém as features e a variável alvo (SalePrice).

Test: contém apenas as features; as previsões são submetidas ao Kaggle. (Resultado: 0.25)

Presença de dados faltantes, variáveis categóricas, distribuições assimétricas e outliers.

🔧 Metodologia (resumo)

EDA: análise de distribuição, correlações, detecção de outliers e skewness.

Tratamento de nulos: estratégias diferentes para numéricas e categóricas (ex.: imputação constante ou mediana/moda).

Feature engineering (exemplos usuais):

Criação de métricas agregadas de área (ex.: TotalSF), idade do imóvel, qualidade combinada etc.

Transformações de log em variáveis altamente assimétricas (incluindo SalePrice).


Modelagem:

Modelos de baseline (Regressão Linear).

Regularização: Ridge e Lasso.

Modelos de árvore: Random Forest, Gradient Boosting (e opcionalmente XGBoost/LightGBM).

Validação:

Cross-validation (K-Fold/StratifiedKFold no log do preço).

Seleção de hiperparâmetros via GridSearchCV/RandomizedSearchCV.

Pipeline:

Uso de Pipeline + ColumnTransformer para garantir reprodutibilidade (mesmos passos em treino e teste).

Métrica:

RMSE do log(SalePrice), alinhada à avaliação do Kaggle.
