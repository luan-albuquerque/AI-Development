# 🌱 Desafio: Análise de Dados de Irrigação com Regressão Linear

## 📋 Sobre o Desafio

Você é o administrador de uma fazenda que depende da irrigação para garantir a produtividade das culturas. Recentemente, começou a registrar os dados de irrigação em um arquivo CSV, contendo informações sobre:

- **Horas de irrigação**
- **Área irrigada correspondente por ângulo**

Seu objetivo é **analisar esses dados para entender a relação entre o tempo de irrigação e a área efetivamente irrigada**, permitindo otimizar os recursos hídricos da fazenda. Para isso, será utilizado um **modelo de regressão linear simples**.

---

## ✅ Tarefas

### 1. 📂 Carregar e Visualizar os Dados

- Carregar os dados a partir de um arquivo `.csv`.
- Exibir as primeiras linhas do dataset.
- Verificar a estrutura das variáveis.

### 2. 📊 Análise Exploratória de Dados (EDA)

- Calcular estatísticas descritivas.
- Criar gráficos de dispersão entre horas de irrigação e área irrigada por ângulo.
- Avaliar a correlação entre as variáveis.

### 3. 📈 Construção do Modelo de Regressão Linear

- Dividir os dados em conjunto de treino e teste.
- Treinar o modelo utilizando:
  - `Horas de irrigação (X)` como variável independente
  - `Área irrigada por ângulo (Y)` como variável dependente
- Exibir a equação da reta gerada pelo modelo.

### 4. 🧪 Avaliação do Modelo

- Avaliar o desempenho do modelo com métricas como:
  - **MSE** (Erro Quadrático Médio)
  - **MAE** (Erro Absoluto Médio)
- Visualizar os valores reais vs. preditos em um gráfico.

### 5. 📉 Análise de Resíduos

- Calcular e analisar os resíduos do modelo.
- Verificar a normalidade dos resíduos com:
  - Histograma
  - Q-Q Plot
  - Testes estatísticos (Shapiro-Wilk, por exemplo)

### 6. 🔮 Predições de Exemplo

- Realizar predições com base no modelo treinado.
- Exemplo: prever a área irrigada para **15 horas de irrigação**.

---

## 🧰 Tecnologias e Bibliotecas Utilizadas

- Python 3.x
- Pandas
- NumPy
- Matplotlib / Seaborn
- Scikit-learn
- SciPy / Statsmodels

---

## 📁 Estrutura do Projeto

```
├── datasets/
│   └── dados_de_irrigacao.csv
├── src/
│   └── analise_irrigacao.ipynb
|   └── api_modelo.py     
├── README.md
```


## 📌 Observações

- Certifique-se de que o arquivo `dados_de_irrigacao.csv` esteja no diretório `datasets/`.
- O modelo de regressão linear assume uma relação linear entre as variáveis — verifique se essa suposição faz sentido com os seus dados.

---

## 📬 Contato

Caso tenha dúvidas ou sugestões, fique à vontade para abrir uma *issue* ou entrar em contato!
