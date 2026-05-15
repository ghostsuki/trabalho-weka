# Trabalho Prático I — Aprendizado de Máquina com Weka

## 1. Problema
Foi definido o problema de classificação de risco de evasão universitária.

Objetivo: prever estudantes com risco:
- baixo
- medio
- alto

---

## 2. Geração do dataset
O dataset foi gerado com auxílio do ChatGPT (LLM), utilizando engenharia de prompts iterativa.

Características:
- 500 instâncias
- 10 atributos preditores
- 1 atributo alvo
- 5% valores faltantes
- 5% ruído
- 3% outliers

---

## 3. Teste piloto
Foi realizada análise exploratória inicial, identificando:
- valores faltantes
- outliers
- atributo irrelevante
- padrões preliminares entre atributos

---

## 4. Pré-processamento
Aplicadas as seguintes etapas:
- remoção de atributo irrelevante;
- imputação de faltantes;
- identificação de outliers;
- normalização.

---

## 5. Visualização
As visualizações mostraram que:
- maior frequência reduz risco;
- maior nota média reduz risco;
- maior número de faltas aumenta risco.

---

## 6. Modelagem
Estratégia:
10-fold cross-validation.

Algoritmos testados:
- J48
- Naive Bayes
- Random Forest
- IBk
- SMO

---

## 7. Resultados

| Algoritmo | Accuracy | Precision | Recall | F1 |
|-----------|----------|-----------|--------|----|
| J48 | ... | ... | ... | ... |
| Naive Bayes | ... | ... | ... | ... |
| Random Forest | ... | ... | ... | ... |
| IBk | ... | ... | ... | ... |
| SMO | ... | ... | ... | ... |

---

## 8. Ajuste de hiperparâmetro
Foi realizado ajuste em Random Forest, alterando `numIterations` de 100 para 200 e avaliando impacto no desempenho.


## 9. Conclusão
Os modelos apresentaram bom desempenho no dataset sintético. O Random Forest apresentou melhor capacidade de generalização.

Como limitação, destaca-se o fato de o conjunto ser sintético, podendo não refletir totalmente dados reais.
