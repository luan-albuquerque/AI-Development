# Regressão Linear Múltipla

A **regressão linear múltipla** é um modelo estatístico/matemático usado para **prever um valor numérico** com base em **duas ou mais variáveis explicativas**.

Ela é uma extensão da **regressão linear simples**, que utiliza apenas uma variável independente.

---

## 📐 Forma geral do modelo

\[
Y = \beta_0 + \beta_1 X_1 + \beta_2 X_2 + \beta_3 X_3 + \dots + \beta_n X_n + \varepsilon
\]

Onde:
- **Y** → variável dependente (o que queremos prever)
- **X₁, X₂, X₃…** → variáveis independentes (explicativas)
- **β₀** → intercepto (valor de Y quando todos os X = 0)
- **β₁, β₂, β₃…** → coeficientes (impacto de cada variável)
- **ε** → erro do modelo

---

## 🎯 Exemplo prático

Queremos prever o **salário mensal** de uma pessoa:

- **X₁** = anos de experiência  
- **X₂** = horas de treinamento por mês  
- **X₃** = nível de escolaridade  
  - 0 = médio  
  - 1 = superior  

Modelo estimado:

\[
Salário = 1500 + 300X_1 + 20X_2 + 800X_3
\]

### Interpretação dos coeficientes

- **1500** → salário base
- **300** → cada ano de experiência aumenta o salário em R$300
- **20** → cada hora de treinamento aumenta o salário em R$20
- **800** → ter ensino superior adiciona R$800 ao salário

---

## 🔍 Para que serve?

- Previsão de valores (salários, vendas, demanda, custos)
- Análise do impacto das variáveis
- Apoio à tomada de decisão
- Base para modelos de Machine Learning supervisionados

---

## ⚠️ Premissas do modelo

A regressão linear múltipla assume que:

- A relação entre X e Y é **linear**
- Os erros são **independentes**
- Não há **multicolinearidade forte** entre as variáveis independentes
- Os resíduos possuem **variância constante** (homocedasticidade)

---

## 🧠 Aplicações comuns

- Economia e finanças
- Ciência de dados
- Previsão de demanda
- Modelos preditivos
- Engenharia e sistemas analíticos
