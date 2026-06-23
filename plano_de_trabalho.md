# Plano de Trabalho — Horse Colic Analysis

**Trabalho Prático II — Inteligência Artificial**
**Data de entrega:** 23 de junho de 2026
**Valor:** 3.0 pontos

---

## PARTE 1 — Pré-processamento

- [ ] **1. Identificação do atributo alvo**
  - Isolar coluna 24 (`surgical lesion?`) como target
  - Converter valores: 1→1 (cirúrgico), 2→0 (não cirúrgico)
  - Celular markdown explicando a escolha

- [ ] **2. Identificação dos tipos de dados**
  - Tabela: cada coluna → tipo (quantitativo contínuo/discreto, qualitativo)

- [ ] **3. Identificação da escala dos dados**
  - Tabela: cada coluna → escala (nominal, ordinal, intervalar, racional)

- [ ] **4. Medidas de localidade**
  - Numéricas: média, mediana, moda
  - Categóricas: tabela de frequência

- [ ] **5. Medidas de espalhamento**
  - Desvio padrão, variância, IQR, range, coeficiente de variação

- [ ] **6. Medidas de distribuição**
  - Histogramas com KDE, boxplots, skewness, kurtosis

- [ ] **7. Separação do conjunto de teste**
  - Carregar `horse-colic.test` (68 instâncias)
  - Comparar distribuições treino vs teste (histogramas sobrepostos)
  - Separar target de ambos

- [ ] **8. Remoção de atributos não necessários**
  - Remover: col 0 (`surgery?`), col 2 (`hospital number`), col 23 (`outcome`), col 25/26/27 (`lesion type`), col 28 (`cp_data`)
  - Justificativa individual para cada remoção

- [ ] **9. Remoção de exemplos não necessários**
  - Verificar duplicatas e linhas com >80% missing

- [ ] **10. Análise de amostragem**
  - Discutir se 300 instâncias é suficiente; provavelmente não precisa de técnica adicional

- [ ] **11. Análise de desbalanceamento**
  - Contar proporção das classes no target
  - Se gap > 60/40, aplicar SMOTE

- [ ] **12. Limpeza de dados**
  - [ ] **12a.** Outliers via IQR (numéricas)
  - [ ] **12b.** Valores fora do range fisiológico
  - [ ] **12c.** Matriz de correlação; remover se >0.95
  - [ ] **12d.** Missing: 3 estratégias (mediana por classe, categoria "não avaliado", remover colunas >50%)

- [ ] **13. Conversão de tipos**
  - [ ] **13a.** One-hot encoding nas categóricas nominais
  - [ ] **13b.** StandardScaler nas numéricas

- [ ] **14. Redução de dimensionalidade**
  - PCA com variância explicada acumulada
  - Decidir se aplica ou justifica não usar

---

## PARTE 2 — Análise Preditiva

- [ ] **15. Técnica de validação**
  - Stratified 5-Fold Cross-Validation
  - Hold-out final com os 68 de teste

- [ ] **16. Métricas**
  - Accuracy, Precision, Recall, F1, Confusion Matrix, ROC AUC

- [ ] **17. Baseline — classe majoritária**
  - `DummyClassifier(strategy='most_frequent')`

- [ ] **18. k-NN**
  - Testar k = 1, 3, 5, 7, 9, 11, 15
  - Escolher melhor com validação cruzada

- [ ] **19. Árvore de decisão**
  - Testar profundidades (3, 5, 7, 10, None)
  - Pós-poda e feature importance

- [ ] **20. MLP (rede neural)**
  - Arquitetura (64, 32), ReLU, Adam, early stopping

- [ ] **21. Análise do baseline**
  - Comparar baseline com os 3 modelos

- [ ] **22. Análise comparativa final**
  - Tabela resumo de métricas
  - Matrizes de confusão lado a lado
  - Feature importance clínica
  - Conclusão: qual modelo é mais adequado

---

## Extras

- [ ] **Features artificiais:** índice de choque, razão PCV/proteína, flag exames ausentes
- [ ] **Documentação:** células markdown com justificativas em cada etapa
- [ ] **Verificação final:** notebook executado do início ao fim sem erros
