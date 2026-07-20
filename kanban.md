# Quadro Kanban — Pipeline Preditivo

> **Status do Projeto:** Não iniciado
> **Metodologia:** Kanban Visual adaptado para documentação Markdown.

---

## 1. A FAZER (To Do)

* [ ] Configuração do ambiente local de desenvolvimento | Ambiente: VS Code + Jupyter Notebook
* [ ] Instalação e registro das dependências no `requirements.txt` | pandas, numpy, scikit-learn, imbalanced-learn, seaborn
* [ ] Mapeamento e leitura completa dos requisitos do edital | 7 fases identificadas e planejadas
* [ ] Estudo do dataset AI4I 2020 Predictive Maintenance | Identificação das colunas, variável-alvo e nível de desbalanceamento
* [ ] Estruturação do repositório do projeto | Criação das pastas `data/`, `outputs/graficos/` e arquivo principal `.ipynb`
* [ ] **[Fase 1 — EDA]** Apresentação das dimensões do dataset com `.shape`, tipos de dados com `.dtypes` e resumo estatístico com `.describe()`
* [ ] **[Fase 1 — EDA]** Gráfico de barras do desbalanceamento da variável-alvo `Machine failure` com percentuais anotados
* [ ] **[Fase 1 — EDA]** Histogramas das variáveis preditoras contínuas para análise de distribuição e assimetria
* [ ] **[Fase 1 — EDA]** Mapa de calor com correlação de Pearson entre variáveis numéricas
* [ ] **[Fase 1 — EDA]** Célula de texto interpretando os padrões encontrados e direcionando a estratégia de modelagem
* [ ] **[Fase 2 — Data Prep]** Identificação e remoção de registros duplicados
* [ ] **[Fase 2 — Data Prep]** Verificação de valores ausentes por coluna
* [ ] **[Fase 2 — Data Prep]** Definição e aplicação da estratégia de imputação para valores faltantes
* [ ] **[Fase 2 — Data Prep]** Geração de boxplots para identificação e análise de outliers nas variáveis contínuas
* [ ] **[Fase 3 — Feature Engineering]** Criação da coluna `potencia = Rotational speed × Torque`
* [ ] **[Fase 3 — Feature Engineering]** Validação da nova feature por meio de análises gráficas e estatísticas
* [ ] **[Fase 4 — Divisão e Balanceamento]** Separação de X (features) e y (target), removendo colunas irrelevantes
* [ ] **[Fase 4 — Divisão e Balanceamento]** Split 80/20 com `stratify=y`
* [ ] **[Fase 4 — Balanceamento]** Aplicação do SMOTE apenas na base de treino
* [ ] **[Fase 5 — Escalonamento]** Aplicação do `StandardScaler` para o modelo KNN
* [ ] **[Fase 5 — Escalonamento]** Registro da justificativa para utilização ou não de escalonamento nos modelos
* [ ] **[Fase 6 — Hiperparâmetros]** Treinamento do KNN com diferentes valores de K
* [ ] **[Fase 6 — Hiperparâmetros]** Treinamento da Árvore de Decisão com diferentes valores de profundidade
* [ ] **[Fase 6 — Overfitting]** Comparação entre desempenho de treino e teste
* [ ] **[Fase 6 — Overfitting]** Geração de gráficos para análise de overfitting
* [ ] **[Fase 6 — Overfitting]** Interpretação dos resultados obtidos
* [ ] **[Fase 7 — Veredito]** Avaliação final dos modelos selecionados
* [ ] **[Fase 7 — Veredito]** Gráfico comparativo de desempenho dos modelos
* [ ] **[Fase 7 — Veredito]** Escolha do modelo final com justificativa técnica
* [ ] **[Técnico]** Versionamento do projeto com Git e definição da estratégia de branches
* [ ] **[Técnico]** Elaboração da documentação completa no `README.md`
* [ ] **[Técnico]** Gravação do vídeo demonstrativo (máx. 7 minutos)
* [ ] **[Técnico]** Submissão dos links no AVA (GitHub + Google Drive do vídeo)

---

## 2. EM ANDAMENTO (Doing)

---

## 3. CONCLUÍDO (Done)

---
