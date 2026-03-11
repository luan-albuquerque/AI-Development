# 🤖 Guia Fundamental: Machine Learning Supervisionado

Este repositório serve como um guia prático e teórico sobre o universo do **Aprendizado Supervisionado**. Aqui você encontrará conceitos essenciais, etapas de preparação de dados e como medir o sucesso dos seus modelos.

---

## 📌 1. O que é Aprendizado Supervisionado?

No aprendizado supervisionado, o algoritmo aprende a partir de um conjunto de dados **rotulado**. É como um aluno estudando com um gabarito: para cada entrada ($X$), ele conhece a resposta correta ($y$).

Existem dois tipos principais de problemas:

1.  **Regressão:** Quando queremos prever um **valor numérico contínuo**.
    * *Exemplo:* Prever o preço de uma casa com base no tamanho e localização.
2.  **Classificação:** Quando queremos prever uma **categoria ou classe**.
    * *Exemplo:* Identificar se um e-mail é "Spam" ou "Não Spam".

---

## 🔍 2. Análise Exploratória de Dados (EDA)

Antes de "dar o play" no treinamento, precisamos entender nossos dados. A EDA ajuda a evitar que o modelo aprenda padrões errados.

* **Identificação de Outliers:** Valores muito fora da curva (ex: uma casa de 10 quartos custando R$ 500,00) que podem confundir o modelo.
* **Análise de Correlação:** Verificar quais variáveis realmente importam para o resultado final.
* **Visualização:** Uso de histogramas e gráficos de dispersão (scatter plots).



---

## 🛠️ 3. Preparação dos Dados (Data Prep)

O segredo de um bom modelo não é o algoritmo, mas a qualidade do dado.

* **Tratamento de Missing Values:** Preencher valores vazios com a média, mediana ou simplesmente remover linhas incompletas.
* **Feature Scaling (Normalização/Padronização):** Colocar todos os números na mesma escala (ex: transformar "Idade" de 0-100 e "Salário" de 0-50.000 para uma escala entre 0 e 1).
* **Encoding:** Transformar texto em números. 
    * *Ex:* Transformar "Masculino/Feminino" em "0/1".

---

## 🏗️ 4. Formas de Treinamento

### Split de Dados (Treino e Teste)
Dividimos o dataset para garantir que o modelo seja testado em dados que ele **nunca viu antes**:
* **Treino (80%):** Onde o modelo ajusta seus parâmetros.
* **Teste (20%):** Onde validamos a performance real.

### Validação Cruzada (K-Fold)
Para evitar que o modelo tenha "sorte" com uma divisão específica, dividimos os dados em $K$ partes. O modelo treina e testa $K$ vezes, alternando as partes.



---

## 📊 5. Métricas de Validação

Como saber se o seu modelo está mentindo para você?

### Para Regressão:
* **MAE (Erro Médio Absoluto):** A média simples do erro (em unidades reais).
* **RMSE (Raiz do Erro Quadrático Médio):** Penaliza erros grandes de forma mais severa.
* **$R^2$:** O quão bem o modelo se ajusta aos dados (0 a 1).

### Para Classificação:
* **Acurácia:** Total de acertos (pode ser enganosa em dados desbalanceados).
* **Matriz de Confusão:** Mostra exatamente o que o modelo confundiu (ex: previu que era doença, mas era saúde).
* **Precision & Recall:** Importantes quando o custo de um "Falso Positivo" ou "Falso Negativo" é alto.



---

## 🚀 Extras Importantes

### Overfitting vs Underfitting
* **Overfitting:** O modelo "decora" o treino e vai mal no teste (especialista demais).
* **Underfitting:** O modelo é simples demais e não aprende nem o básico.

### Principais Algoritmos
| Tipo | Algoritmo | Complexidade |
| :--- | :--- | :--- |
| **Regressão** | Linear Regression | Baixa |
| **Regressão** | Random Forest Regressor | Alta |
| **Classificação** | Naive Bayes | Baixa |
| **Classificação** | XGBoost / LightGBM | Alta |
