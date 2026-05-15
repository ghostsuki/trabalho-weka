# Prompts Utilizados para Geração do Dataset

## Ferramenta utilizada

- ChatGPT (OpenAI)

---

## Objetivo

Gerar um dataset sintético para classificação de risco de evasão acadêmica em estudantes universitários, garantindo coerência semântica entre os atributos, distribuição realista entre classes e inserção controlada de problemas típicos encontrados em bases de dados reais.

---

# Prompt 1 — Definição inicial do dataset

```text
Gere um dataset sintético com 500 estudantes universitários para prever risco de evasão acadêmica.

Atributos:
- idade (17 a 45)
- frequencia (0 a 100)
- nota_media (0 a 10)
- horas_estudo (0 a 40)
- renda_familiar (800 a 15000)
- acesso_internet (sim/nao)
- faltas (0 a 60)
- extracurricular (sim/nao)
- distancia_km (0 a 80)

Classe alvo:
risco_evasao = baixo, medio ou alto
```

### Objetivo do prompt
Criar a estrutura inicial do dataset e definir os atributos principais relacionados ao problema de evasão acadêmica.

---

# Prompt 2 — Ajuste para maior realismo

```text
Torne o dataset mais realista:
- adicione desbalanceamento entre as classes;
- mantenha coerência entre atributos e classe;
- simule um cenário próximo ao real.
```

### Objetivo do prompt
Representar um cenário mais próximo da realidade acadêmica, onde a maioria dos estudantes permanece na universidade e apenas uma parcela apresenta risco elevado.

### Resultado obtido
Distribuição definida:

- 50% baixo
- 30% medio
- 20% alto

---

# Prompt 3 — Definição de regras semânticas

```text
Considere que:
- baixa frequência aumenta o risco de evasão;
- muitas faltas aumentam o risco;
- nota média baixa aumenta o risco;
- poucas horas de estudo aumentam o risco;
- alta frequência e boas notas reduzem o risco.
```

### Objetivo do prompt
Garantir que os dados possuam relações lógicas entre atributos e classe, permitindo aprendizado significativo pelos algoritmos.

---

# Prompt 4 — Inserção de problemas reais

```text
Adicione:
- 5% de valores faltantes;
- 5% de ruído;
- 3% de outliers.
```

### Objetivo do prompt
Simular problemas comuns encontrados em datasets reais para permitir aplicação de técnicas de pré-processamento.

### Resultado obtido
Foram inseridos:

- valores faltantes distribuídos em múltiplos atributos;
- registros com ruído proposital;
- valores extremos para representar outliers.

---

# Prompt 5 — Inserção de atributo irrelevante

```text
Adicione um atributo irrelevante que não tenha relação com evasão acadêmica.
```

### Resultado obtido
Foi criado o atributo:

```text
cor_favorita
```

### Objetivo do prompt
Permitir análise de relevância de atributos e remoção durante o pré-processamento.

---

# Prompt 6 — Exportação final

```text
Exporte o dataset final em formato CSV compatível com Weka.
```

### Objetivo do prompt
Garantir compatibilidade direta com o software Weka para as etapas experimentais.

---

# Estratégia de Engenharia de Prompt

A geração do dataset foi realizada utilizando uma abordagem iterativa de engenharia de prompts.

O processo ocorreu em múltiplas etapas:

1. definição inicial do problema;
2. definição dos atributos;
3. ajuste para maior realismo;
4. inserção de relações semânticas;
5. inclusão de valores faltantes, ruído e outliers;
6. inserção de atributo irrelevante;
7. exportação final para uso no Weka.

Essa abordagem permitiu rastreabilidade completa da geração dos dados, conforme exigido no enunciado do trabalho.

---

# Conclusão

O uso de um modelo de linguagem de grande escala (LLM) permitiu gerar um dataset sintético controlado, coerente e adequado para experimentação em aprendizado de máquina, atendendo integralmente aos requisitos propostos pelo trabalho.
