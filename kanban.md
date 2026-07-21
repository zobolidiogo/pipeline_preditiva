# Quadro Kanban - Pipeline Preditivo

> **Status do Projeto:** Não iniciado
> **Metodologia:** Kanban Visual adaptado para documentação Markdown.

---

## 1. A FAZER (To Do)

* [ ] **[Técnico]** Elaboração da documentação completa no `README.md`
* [ ] **[Técnico]** Gravação do vídeo demonstrativo (máx. 7 minutos)
* [ ] **[Técnico]** Submissão dos links no AVA (GitHub + Google Drive do vídeo)

---

## 3. CONCLUÍDO (Done)

* [x] Configuração do ambiente local de desenvolvimento | Ambiente: VS Code + Jupyter Notebook
* [x] Instalação e registro das dependências no `requirements.txt` | pandas, numpy, scikit-learn, imbalanced-learn, seaborn
* [x] Mapeamento e leitura completa dos requisitos do edital | 7 fases identificadas e planejadas
* [x] Estudo do dataset AI4I 2020 Predictive Maintenance | Identificação das colunas, variável-alvo e nível de desbalanceamento
* [x] Estruturação do repositório do projeto | Criação das pastas `data/`, `outputs/graficos/` e arquivo principal `.ipynb`
* [x] **[Fase 1 — EDA]** Apresentação das dimensões do dataset com `.shape`, tipos de dados com `.dtypes` e resumo estatístico com `.describe()`
* [x] **[Fase 1 — EDA]** Gráfico de barras do desbalanceamento da variável-alvo `Machine failure` com percentuais anotados
* [x] **[Fase 1 — EDA]** Histogramas das variáveis preditoras contínuas para análise de distribuição e assimetria
* [x] **[Fase 1 — EDA]** Mapa de calor com correlação de Pearson entre variáveis numéricas
* [x] **[Fase 1 — EDA]** Célula de texto interpretando os padrões encontrados e direcionando a estratégia de modelagem
* [x] **[Fase 2 — Data Prep]** Identificação e remoção de registros duplicados
* [x] **[Fase 2 — Data Prep]** Verificação de valores ausentes por coluna
* [x] **[Fase 2 — Data Prep]** Definição e aplicação da estratégia de imputação para valores faltantes
* [x] **[Fase 2 — Data Prep]** Geração de boxplots para identificação e análise de outliers nas variáveis contínuas
* [x] **[Fase 3 — Feature Engineering]** Criação da coluna `potencia = Rotational speed × Torque`
* [x] **[Fase 3 — Feature Engineering]** Validação da nova feature por meio de análises gráficas e estatísticas
* [x] **[Fase 4 — Divisão e Balanceamento]** Separação de X (features) e y (target), removendo colunas irrelevantes
* [x] **[Fase 4 — Divisão e Balanceamento]** Split 80/20 com `stratify=y`
* [x] **[Fase 4 — Balanceamento]** Aplicação do SMOTE apenas na base de treino
* [x] **[Fase 5 — Escalonamento]** Aplicação do `StandardScaler` para o modelo KNN
* [x] **[Fase 5 — Escalonamento]** Registro da justificativa para utilização ou não de escalonamento nos modelos
* [x] **[Fase 6 — Hiperparâmetros]** Treinamento do KNN com diferentes valores de K
* [x] **[Fase 6 — Hiperparâmetros]** Treinamento da Árvore de Decisão com diferentes valores de profundidade
* [x] **[Fase 6 — Overfitting]** Comparação entre desempenho de treino e teste
* [x] **[Fase 6 — Overfitting]** Geração de gráficos para análise de overfitting
* [x] **[Fase 6 — Overfitting]** Interpretação dos resultados obtidos
* [x] **[Fase 7 — Veredito]** Avaliação final dos modelos selecionados
* [x] **[Fase 7 — Veredito]** Gráfico comparativo de desempenho dos modelos
* [x] **[Fase 7 — Veredito]** Escolha do modelo final com justificativa técnica
* [x] **[Técnico]** Versionamento do projeto com Git e definição da estratégia de branches


---
