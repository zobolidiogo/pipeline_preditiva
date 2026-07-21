# PIPELINE PREDITIVO - Previsão de Falhas em Equipamentos Industriais

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge)

Pipeline de Machine Learning desenvolvido em Python para previsão de falhas mecânicas em equipamentos industriais, utilizando Pandas, Scikit-learn, balanceamento de classes com SMOTE e comparação entre modelos de classificação.

Projeto desenvolvido para a disciplina de IA para Análise Preditiva - SENAI/SCTEC.

---

# O Desafio

Desenvolver um pipeline completo de análise preditiva capaz de:

* Realizar análise exploratória de um dataset real de sensores industriais
* Tratar valores nulos e outliers de forma justificada
* Criar uma feature derivada com significado físico
* Lidar com desbalanceamento de classes
* Comparar dois algoritmos de classificação com ajuste de hiperparâmetros
* Justificar tecnicamente cada decisão tomada no processo

Tudo isso seguindo os critérios de avaliação definidos na atividade.

---

# A Solução

O projeto implementa um pipeline completo de previsão de falhas baseado no dataset:

**manutencao_preditiva.csv** (10.000 registros de sensores industriais)

O fluxo executado no notebook é:

```text
Dataset (sensores industriais)
      ↓
Análise Exploratória (EDA)
      ↓
Limpeza de Dados
      ↓
Feature Engineering
      ↓
Split Treino/Teste Estratificado
      ↓
Balanceamento (SMOTE)
      ↓
Escalonamento (StandardScaler)
      ↓
Ajuste de Hiperparâmetros
      ↓
Avaliação e Comparação dos Modelos
```

Toda a execução está organizada em fases sequenciais dentro do notebook `pipeline_preditiva.ipynb`.

---

# Funcionalidades Principais

## Análise Exploratória (EDA)

* Inspeção de dimensões, tipos de dados e valores nulos
* Gráfico de desbalanceamento da variável-alvo
* Distribuição das variáveis contínuas (histogramas)
* Mapa de calor de correlação de Pearson

---

## Limpeza de Dados

Processamento para:

* Remoção de registros duplicados
* Imputação de valores nulos pela mediana (justificada pela assimetria das distribuições, skewness ≈ 2)
* Detecção de outliers via boxplot, mantidos por representarem possíveis precursores de falha

---

## Feature Engineering

Criação da variável `potencia`, combinando torque e velocidade de rotação:

```python
df["potencia"] = df["velocidade_rotacao_rpm"] * df["torque_nm"]
```

Baseada na relação física da potência mecânica (torque × velocidade angular).

---

## Divisão e Balanceamento dos Dados

* Split treino/teste estratificado (`stratify=y`), preservando a proporção real de falhas
* Remoção de colunas que causariam data leakage (`falha_twf`, `falha_hdf`, `falha_pwf`, `falha_osf`, `falha_rnf`), por representarem subtipos/consequência da falha e não a causa
* Balanceamento com **SMOTE**, aplicado somente no conjunto de treino após o split

---

## Escalonamento de Variáveis

* `StandardScaler` aplicado ao KNN, que depende de distância entre pontos no espaço de features
* Dispensado na Árvore de Decisão, que decide por limiares (ex: `velocidade_rotacao_rpm > 1500`), onde a escala não influencia o resultado

---

## Ajuste de Hiperparâmetros

Cálculo comparativo de acurácia treino vs teste para identificar overfitting:

* **KNN:** variação de `n_neighbors` (K = 3, 5, 7, 9, 11)
* **Árvore de Decisão:** variação de `max_depth` (3, 5, 7, sem limite), com `random_state=42` fixo

---

## Avaliação Final

* Comparação da acurácia dos dois modelos na base de teste, já com os melhores hiperparâmetros de cada um
* Gráfico de barras comparando o desempenho final
* Conclusão sobre qual modelo apresentou melhor equilíbrio entre acurácia e generalização

---

# Conceitos Aplicados

O projeto contempla diversos conceitos estudados durante a disciplina:

### Ciência de Dados

* Pandas / NumPy
* Análise exploratória (EDA)
* Tratamento de nulos e outliers
* Feature Engineering

### Machine Learning

* KNN (K-Nearest Neighbors)
* Árvore de Decisão
* StandardScaler
* SMOTE (balanceamento de classes)
* Ajuste de hiperparâmetros e análise de overfitting

### Visualização

* Matplotlib
* Seaborn

---

# Estrutura do Projeto

```text
pipeline_preditiva/
│
├── data/
│   └── manutencao_preditiva.csv
│
├── outputs/
│   └── graficos/
│
├── pipeline_preditiva.ipynb
├── data_dict.md
├── README.md
├── requirements.txt
├── kanban.md
└── anotacoes.docx
```

## Vídeo Demonstrativo

Link do vídeo: 

O vídeo apresenta o objetivo do sistema, demonstração de funcionamento, organização das tarefas, branches utilizadas e argumentação das escolhas técnicas do projeto.

---

# Como Executar

## 1. Clonar o repositório

```bash
git clone https://github.com/zobolidiogo/pipeline_preditiva.git
cd pipeline_preditiva
```

## 2. Instalar dependências

```bash
pip install -r requirements.txt
```

## 3. Executar o projeto

```bash
jupyter notebook pipeline_preditiva.ipynb
```

Rode as células em ordem, do início ao fim.

## 4. Resultados

Os gráficos gerados serão armazenados automaticamente na pasta:

```text
outputs/graficos/
```

---

# Tecnologias Utilizadas

### Linguagem

* Python

### Bibliotecas

* Pandas
* NumPy
* Scikit-learn
* Imbalanced-learn (SMOTE)
* Matplotlib
* Seaborn

### Ferramentas

* Git
* GitHub
* Jupyter Notebook

---

# Aprendizados

Este projeto consolidou conhecimentos em:

* Análise exploratória de dados de sensores industriais
* Tratamento justificado de valores nulos e outliers
* Criação de features com significado físico/de negócio
* Prevenção de data leakage
* Balanceamento de classes com SMOTE
* Diferença entre a necessidade de escalonamento no KNN e na Árvore de Decisão
* Diagnóstico de overfitting por comparação treino vs teste
* Comparação técnica entre modelos de classificação

---

# Autor

**Diogo Zoboli**

* GitHub: [https://github.com/zobolidiogo](https://github.com/zobolidiogo)
* LinkedIn: [https://linkedin.com/in/zobolidiogo](https://linkedin.com/in/zobolidiogo)

---

⭐ Se você gostou, considere dar uma estrela no repositório!