# Descrição das Etapas de Pré-processamento

Após a análise exploratória inicial, foi realizado o pré-processamento do dataset utilizando exclusivamente o software Weka.

---

## 1. Remoção de atributo irrelevante

O atributo `cor_favorita` foi removido do conjunto de dados.

Justificativa:
Esse atributo não apresenta relação semântica com o problema de evasão acadêmica e sua permanência poderia introduzir ruído desnecessário ao modelo.

Filtro utilizado:
- Remove

---

## 2. Tratamento de valores faltantes

Foram identificados valores ausentes em diferentes atributos do dataset.

Para resolver esse problema, foi aplicado o filtro:

- ReplaceMissingValues

Esse filtro substitui:
- média para atributos numéricos;
- moda para atributos categóricos.

Essa abordagem foi escolhida para preservar o número total de instâncias.

---

## 3. Identificação de outliers

Com base na análise inicial, observou-se a presença de valores extremos.

Foi utilizado o filtro:

- InterquartileRange

Esse método detecta outliers utilizando o intervalo interquartil (IQR), permitindo identificar instâncias discrepantes em relação à distribuição principal.

---

## 4. Normalização

Após limpeza e tratamento dos dados, aplicou-se:

- Normalize

Objetivo:
padronizar a escala dos atributos numéricos para evitar que variáveis com magnitudes maiores influenciassem indevidamente o treinamento dos modelos.

Resultado:
todos os atributos numéricos foram transformados para a escala entre 0 e 1.

---

## 5. Resultado final do pré-processamento

Ao final do processo:

- o atributo irrelevante foi removido;
- os valores faltantes foram tratados;
- os outliers foram identificados;
- os dados foram normalizados.

O dataset final foi salvo como:

`dataset_preprocessado.arff`

Esse conjunto foi utilizado nas etapas de visualização e modelagem.
