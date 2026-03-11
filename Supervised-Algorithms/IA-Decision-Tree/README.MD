# 🌳 Árvore de Decisão (Decision Tree)

## 📌 Introdução

A **Árvore de Decisão** é um algoritmo de **Machine Learning supervisionado** utilizado tanto para **classificação** quanto para **regressão**.

Ela funciona de forma semelhante a um **fluxograma**, onde cada nó representa uma decisão baseada em uma característica do conjunto de dados.

Esse modelo é muito utilizado por ser **simples de entender, interpretar e visualizar**.

---

## ⚙️ Como funciona

Uma árvore de decisão é composta por três partes principais:

- **Nó raiz (Root Node)**  
  Representa o conjunto de dados completo e é o ponto inicial da árvore.

- **Nós internos (Decision Nodes)**  
  Representam testes ou decisões baseadas em atributos do dataset.

- **Nós folha (Leaf Nodes)**  
  Representam o resultado final da previsão (classe ou valor).

### Exemplo simples

Suponha que queremos prever se uma pessoa irá **comprar um produto**.

---

## 📊 Tipos de Problemas

### Classificação

A árvore prevê **categorias ou classes**.

Exemplo:

- Aprovar ou reprovar crédito
- Diagnóstico de doenças
- Spam ou não spam

### Regressão

A árvore prevê **valores numéricos**.

Exemplo:

- Preço de casas
- Previsão de vendas
- Receita de vendedores

---

## 🧠 Critérios de Divisão

Para decidir qual atributo será usado para dividir os dados, a árvore utiliza métricas como:

### Entropia

Mede o nível de **desorganização** nos dados.

### Ganho de Informação

Mede o quanto uma divisão **reduz a entropia**.

### Índice de Gini

Mede a **impureza dos dados**.

Muito utilizado no algoritmo **CART**.

---

## 💻 Exemplo em Python

Utilizando a biblioteca **Scikit-Learn**:

```python
from sklearn.tree import DecisionTreeClassifier
from sklearn.model_selection import train_test_split
from sklearn.datasets import load_iris

# carregando dataset
data = load_iris()
X = data.data
y = data.target

# separando treino e teste
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3)

# criando modelo
model = DecisionTreeClassifier()

# treinando
model.fit(X_train, y_train)

# previsão
predictions = model.predict(X_test)

print(predictions)
```
