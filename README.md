- [1. 🧠 MLClassifySimple](#1--mlclassifysimple)
  - [1.1. 📌 Objetivo](#11--objetivo)
  - [1.2. ⚙️ O que você encontrará neste repositório](#12-️-o-que-você-encontrará-neste-repositório)
    - [1.2.1. 🤖 Treinamento de modelos de classificação](#121--treinamento-de-modelos-de-classificação)
    - [1.2.2. 📊 Geração e análise de métricas](#122--geração-e-análise-de-métricas)
    - [1.2.3. 📈 Visualizações](#123--visualizações)
  - [1.3. 🧪 Tecnologias utilizadas](#13--tecnologias-utilizadas)
  - [1.4. ▶️ Como executar localmente](#14-️-como-executar-localmente)
    - [1.4.1. 🔧 Pré-requisitos](#141--pré-requisitos)
  - [1.5. 📁 Estrutura do projeto](#15--estrutura-do-projeto)
  - [1.6. 📬 Contato](#16--contato)

# 1. 🧠 MLClassifySimple

Um repositório de estudos com modelos simples de **classificação** para fins de **estudo, implementação** e **análise de métricas de performance** em Machine Learning.

Os datasets utilizados são simples e pré-processados para proporcionar um **ambiente direto e focado em aprendizado prático**.

---

## 1.1. 📌 Objetivo
Estudar modelos de Machine Learning com foco em classificação para:

- Entender como modelos de classificação funcionam na prática

- Aprender a interpretar métricas e visualizações

- Experimentar e comparar modelos de forma clara e direta

---

## 1.2. ⚙️ O que você encontrará neste repositório


### 1.2.1. 🤖 Treinamento de modelos de classificação
- `LinearSVC`
- `SVC (Support Vector Classifier)`
- `DummyClassifier`
- `DecisionTreeClassifier`

### 1.2.2. 📊 Geração e análise de métricas
- Acurácia
- Precisão
- Revocação (Recall)
- F1-Score
- Curva ROC e AUC
- Matriz de confusão com **anotações interpretativas**

### 1.2.3. 📈 Visualizações
- Gráficos com `matplotlib` e `seaborn` para facilitar a **interpretação visual dos resultados**.

---

## 1.3. 🧪 Tecnologias utilizadas

- Python `3.11+`
- [scikit-learn](https://scikit-learn.org/)
- [pandas](https://pandas.pydata.org/)
- [seaborn](https://seaborn.pydata.org/)
- [matplotlib](https://matplotlib.org/)
- [poetry](https://python-poetry.org/) – gerenciamento de dependências

---

## 1.4. ▶️ Como executar localmente

### 1.4.1. 🔧 Pré-requisitos

- Python `3.11+`
- Poetry instalado:
```bash
pip install poetry
```
▶️ Passos para executar o projeto:
```bash
# Clone o repositório
git clone https://github.com/SEU_USUARIO/MLClassifySimple.git
cd MLClassifySimple

# Instale as dependências e ative o ambiente virtual
poetry install
poetry shell

# Execute os notebooks
jupyter notebook

# Caso não tenha o Jupyter instalado no ambiente, você pode adicioná-lo com:

```bash
poetry add notebook
```
## 1.5. 📁 Estrutura do projeto
```bash
MLClassifySimple/
├── data/            # Dados brutos e processados
├── docs/            # Documentação complementar do projeto
├── notebooks/       # Análises e experimentos em Jupyter
├── tests/           # Scripts de teste e validação
├── poetry.lock      # Arquivo de bloqueio de dependências (gerado pelo Poetry)
├── pyproject.toml   # Configuração do projeto e dependências
├── README.md        # Documentação principal do projeto

```

## 1.6. 📬 Contato

- ✉️ **E-mail:** [espedito.ferreira.alves@outlook.com](espedito.ferreira.alves@outlook.com) 
- 🔗 **LinkedIn:** [Espedito Ferreira Alves](https://www.linkedin.com/in/espedito-ferreira-alves/)  