# Análise Exploratória Inicial (Teste Piloto)

## 1. Objetivo

Antes de iniciar o pré-processamento, foi realizada uma análise exploratória inicial do dataset com o objetivo de identificar inconsistências, compreender a distribuição dos dados e levantar hipóteses que orientassem as decisões posteriores.

Essa etapa foi conduzida no software Weka, conforme exigido pelo trabalho.

---

## 2. Visão geral do dataset

O dataset sintético gerado contém:

- 500 instâncias;
- 11 atributos no total;
- 10 atributos preditores;
- 1 atributo alvo (`risco_evasao`).

A variável alvo foi definida com três classes:

- baixo
- medio
- alto

A distribuição foi propositalmente desbalanceada:

- baixo ≈ 50%
- medio ≈ 30%
- alto ≈ 20%

Esse desbalanceamento foi inserido para representar um cenário mais realista de evasão acadêmica.

---

## 3. Estatísticas básicas observadas

A inspeção inicial dos atributos numéricos mostrou:

| Atributo | Observação |
|----------|------------|
| idade | maioria entre 17 e 45 |
| frequencia | valores entre 0 e 100 |
| nota_media | valores entre 0 e 10 |
| horas_estudo | maioria abaixo de 40 |
| renda_familiar | maioria abaixo de 15000 |

---

## 4. Identificação de outliers

Durante a análise foram detectados valores extremos inseridos intencionalmente:

- idade = 72 e 80
- renda_familiar entre 50000 e 90000
- horas_estudo = 55 e 65

Esses registros foram classificados como outliers.

---

## 5. Identificação de valores faltantes

Foram observados valores ausentes (`?`) distribuídos em múltiplos atributos, principalmente:

- nota_media
- renda_familiar
- frequencia

Essa observação justificou a etapa posterior de imputação.

---

## 6. Identificação de atributo irrelevante

O atributo `cor_favorita` foi incluído propositalmente como atributo irrelevante.

Esse atributo não possui relação lógica com a evasão acadêmica e foi mantido inicialmente para avaliar a etapa de seleção de atributos.

---

## 7. Relações preliminares entre atributos

As visualizações iniciais mostraram:

- estudantes com menor frequência tendem a maior risco de evasão;
- maior número de faltas está associado a maior risco;
- notas mais baixas aparecem com maior frequência em alunos de alto risco;
- mais horas de estudo tendem a reduzir o risco.

Essas relações indicaram consistência semântica no dataset.

---

## 8. Decisões para o pré-processamento

Com base na análise exploratória inicial, definiu-se:

1. remover atributo irrelevante (`cor_favorita`);
2. tratar valores faltantes;
3. identificar e tratar outliers;
4. aplicar normalização.

Dessa forma, o pré-processamento foi guiado por evidências observadas nos dados.
