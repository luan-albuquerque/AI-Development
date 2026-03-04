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


## 🧠 Por que o código foi estruturado dessa forma?

O código original não faz apenas o básico; ele adota três grandes boas práticas estruturais para garantir que o modelo de *Machine Learning* seja robusto e confiável para cenários reais:

### 1. Prevenção de Vazamento de Dados (*Data Leakage*) com `Pipeline`
O código utiliza o `StandardScaler` para padronizar as variáveis numéricas. Em *Machine Learning*, a regra de ouro é: você só deve calcular a média e o desvio padrão usando exclusivamente os dados de **treino**. 
* **O Risco:** Se você padronizar o dataset inteiro antes de dividir, informações dos dados de teste acabam "vazando" para o modelo, criando uma falsa sensação de precisão (*Data Leakage*). 
* **A Solução:** O uso de um `Pipeline` garante que as transformações (padronização e criação de *features* polinomiais) aprendam **apenas** com os dados de treino dentro de cada rodada, blindando o seu modelo.

### 2. Validação Cruzada (`KFold`)
Em vez de depender de um simples `train_test_split` (uma divisão única entre treino e teste), o código utiliza o `KFold(n_splits=5)`. 



* **Como funciona:** Ele divide os seus dados em 5 partes (*folds*). O modelo é treinado 5 vezes; em cada uma delas, ele usa 4 partes para treinar e deixa 1 parte diferente para testar. 
* **A Vantagem:** Isso permite calcular a média das métricas de erro e acerto (como o R² e o RMSE), garantindo que a precisão do seu modelo é real e consistente, e não apenas "sorte" ou "azar" na hora de separar os dados.

### 3. Organização Escalável (`ColumnTransformer`)
O código isola as colunas numéricas específicas (`tempo_na_empresa` e `nivel_na_empresa`) para aplicar a padronização isoladamente nelas antes de elevar ao grau polinomial.
* **A Vantagem:** Essa modularidade deixa a porta aberta para, no futuro, adicionar transformações em variáveis categóricas (como *One-Hot Encoding*) de forma limpa, sem quebrar a lógica do código atual.