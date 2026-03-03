# Regressão Polinomial

A **regressão polinomial** é uma extensão da regressão linear usada para modelar **relações não lineares** entre as variáveis.

Apesar do nome, ela **continua sendo um modelo linear nos coeficientes**, mas utiliza **variáveis elevadas a potências (graus)** para capturar curvaturas nos dados.

---

## 📐 Forma geral do modelo

Para um polinômio de grau 2:

\[
Y = \beta_0 + \beta_1 X + \beta_2 X^2 + \varepsilon
\]

Para um polinômio de grau n:

\[
Y = \beta_0 + \beta_1 X + \beta_2 X^2 + \beta_3 X^3 + \dots + \beta_n X^n + \varepsilon
\]

Onde:

- **Y** → variável dependente
- **X** → variável independente
- **β₀** → intercepto
- **β₁, β₂, β₃…** → coeficientes
- **ε** → erro do modelo

---

## 🎯 Exemplo prático

Queremos prever o **consumo de combustível** com base na **velocidade do veículo**.

Sabemos que o consumo não cresce de forma linear — existe uma curvatura.

Modelo de grau 2:

\[
Consumo = 5 + 0.1X + 0.02X^2
\]

### 📊 Interpretação

- **5** → consumo base
- **0.1X** → efeito linear da velocidade
- **0.02X²** → efeito quadrático (curvatura)

O termo \(X^2\) permite que o gráfico forme uma **parábola**, capturando padrões não lineares.

---

## 📈 Por que usar regressão polinomial?

Porque nem sempre os dados seguem uma linha reta.

Exemplos de relações não lineares:

- Crescimento populacional
- Desempenho vs. temperatura
- Velocidade vs. consumo
- Tempo de estudo vs. desempenho

---

## 🔍 Diferença para regressão linear

| Regressão Linear            | Regressão Polinomial         |
| --------------------------- | ---------------------------- |
| Modela linha reta           | Modela curvas                |
| Apenas X                    | X, X², X³...                 |
| Relação estritamente linear | Relação não linear nos dados |

⚠️ Importante: O modelo ainda é **linear nos parâmetros (β)**.

---

## ⚠️ Cuidados

- Graus muito altos podem causar **overfitting**
- Pode gerar alta correlação entre variáveis (multicolinearidade)
- Necessita validação adequada

---

## 🧠 Aplicações comuns

- Modelagem de tendências
- Séries temporais simples
- Engenharia
- Economia
- Machine Learning (como transformação antes de regressão linear)

---

## 🛠 Como funciona na prática (conceito)

1. Criamos novas variáveis:
   - X²
   - X³
   - etc

2. Aplicamos regressão linear normalmente sobre essas novas variáveis.

Ou seja, a regressão polinomial é basicamente:

> Engenharia de atributos + regressão linear
