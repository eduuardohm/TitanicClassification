# Titanic Classification

Este projeto aplica uma pipeline completa de análise exploratória, pré-processamento e classificação para o famoso dataset do Titanic. O objetivo é investigar as características dos passageiros e construir modelos preditivos para estimar a probabilidade de sobrevivência.

## Visão Geral

O fluxo do projeto foi organizado em três notebooks:

1. **Análise exploratória** – inspeção dos dados, tratamento inicial de valores ausentes, análise univariada e multivariada.
2. **Pré-processamento** – imputação de valores faltantes, codificação de variáveis categóricas, engenharia de features e exportação dos dados preparados.
3. **Classificação** – treinamento e avaliação de modelos, com foco em SVM e Random Forest.

## Estrutura do Repositório

```text
.
├── data/
│   ├── preprocessed/
│   │   ├── train_preprocessed.csv
│   │   └── test_preprocessed.csv
│   └── raw/
│       ├── train.csv
│       ├── test.csv
│       └── gender_submission.csv
├── notebooks/
│   ├── 01_analise_exploratoria.ipynb
│   ├── 02_preprocessamento.ipynb
│   └── 03_classificacao.ipynb
├── requirements.txt
└── README.md
```

## Pipeline do Projeto

### 1) Análise Exploratória

No notebook de análise exploratória, foram avaliados:

- estrutura e tipos das colunas;
- estatísticas descritivas;
- valores ausentes;
- duplicidades e inconsistências;
- distribuição de variáveis como sexo, classe, idade e tarifa;
- relação entre variáveis e a taxa de sobrevivência.

### 2) Pré-processamento

No notebook de pré-processamento, foram realizados:

- remoção de colunas irrelevantes ou com alto ruído, como PassengerId, Name, Ticket e Cabin;
- imputação de idade com base no sexo;
- preenchimento de valores ausentes em Embarked;
- criação de novas features, como FamilySize e IsAlone;
- codificação de variáveis categóricas;
- exportação dos datasets já tratados para a pasta data/preprocessed.

### 3) Classificação

No notebook de classificação, foram treinados e avaliados modelos para prever sobrevivência. O fluxo incluiu:

- divisão dos dados entre treino e teste;
- padronização das features;
- treinamento de um modelo SVM;
- treinamento de um modelo Random Forest;
- uso de RandomizedSearchCV para otimização dos hiperparâmetros do Random Forest;
- avaliação por métricas como acurácia e relatório de classificação.

## Dependências

As dependências principais estão listadas em requirements.txt. Para instalar, execute:

```bash
pip install -r requirements.txt
```

## Como Executar

Recomenda-se seguir a ordem dos notebooks:

1. Abrir e executar notebooks/01_analise_exploratoria.ipynb
2. Abrir e executar notebooks/02_preprocessamento.ipynb
3. Abrir e executar notebooks/03_classificacao.ipynb

Se preferir, você também pode abrir os notebooks no Jupyter Notebook ou JupyterLab.

## Resultados Esperados

Ao final do fluxo, o projeto gera dados pré-processados em data/preprocessed e permite comparar modelos de classificação para prever sobrevivência no Titanic.
