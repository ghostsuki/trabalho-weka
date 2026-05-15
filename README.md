# Trabalho Prático I — Aprendizado de Máquina com Weka

Projeto desenvolvido para a disciplina de **Inteligência Artificial**, utilizando o software **Weka** para construção, pré-processamento, análise e modelagem de um dataset sintético de evasão acadêmica.

---

# Sumário

- [1. Objetivo do Projeto](#1-objetivo-do-projeto)
- [2. Estrutura do Repositório](#2-estrutura-do-repositório)
- [3. Dataset](#3-dataset)
- [4. Engenharia de Prompt](#4-engenharia-de-prompt)
- [5. Análise Exploratória Inicial](#5-análise-exploratória-inicial)
- [6. Pré-processamento](#6-pré-processamento)
- [7. Visualização dos Dados](#7-visualização-dos-dados)
- [8. Modelagem e Avaliação](#8-modelagem-e-avaliação)
- [9. Ajuste de Hiperparâmetros](#9-ajuste-de-hiperparâmetros)
- [10. Relatório Final](#10-relatório-final)
- [11. Tecnologias Utilizadas](#11-tecnologias-utilizadas)

---

# 1. Objetivo do Projeto

Construir um pipeline completo de aprendizado de máquina para prever **risco de evasão acadêmica** em estudantes universitários, utilizando dados sintéticos gerados com auxílio de LLMs.

Classes previstas:

- baixo
- medio
- alto

---

# 2. Estrutura do Repositório

```text
trabalho-weka/
├── dataset/
├── prompts/
├── preprocessamento/
├── imagens/
│   ├── prints_weka/
│   └── visualizacoes/
└── relatorio/
```

---

# 3. Dataset

O dataset foi construído artificialmente contendo:

- 500 instâncias
- 10 atributos preditores
- 1 atributo alvo (`risco_evasao`)
- 5% valores faltantes
- 5% ruído
- 3% outliers

Arquivos disponíveis em:

```text
/dataset/
```

---

# 4. Engenharia de Prompt

A geração do dataset foi realizada com auxílio do **ChatGPT**, utilizando engenharia iterativa de prompts.

Documentação disponível em:

```text
/prompts/prompts_utilizados.md
```

---

# 5. Análise Exploratória Inicial

Foi realizado um teste piloto para:

- identificar inconsistências;
- detectar outliers;
- localizar valores faltantes;
- analisar relações entre atributos.

Arquivo:

```text
/preprocessamento/analise_inicial.md
```

---

# 6. Pré-processamento

Etapas aplicadas no Weka:

- remoção de atributo irrelevante (`cor_favorita`);
- imputação de valores faltantes;
- identificação de outliers;
- normalização.

Arquivo:

```text
/preprocessamento/descricao_etapas.md
```

---

# 7. Visualização dos Dados

Visualizações realizadas:

- frequência × risco
- nota média × risco
- faltas × risco

Imagens disponíveis em:

```text
/imagens/visualizacoes/
```

---

# 8. Modelagem e Avaliação

Estratégia utilizada:

- 10-fold cross-validation

Algoritmos testados:

- J48
- Naive Bayes
- Random Forest
- IBk
- SMO

Resultados completos em:

```text
/relatorio/relatorio_final.md
```

---

# 9. Ajuste de Hiperparâmetros

Foi realizado ajuste no algoritmo **Random Forest**:

- `numIterations: 100 → 200`

Objetivo:
avaliar impacto no desempenho do modelo.

---

# 10. Relatório Final

Arquivo principal do trabalho:

```text
/relatorio/relatorio_final.md
```

---

# 11. Tecnologias Utilizadas

Ferramentas utilizadas:

- Weka
- ChatGPT
- GitHub
- Markdown
- CSV / ARFF

---

## Autor

Luiz Augusto
