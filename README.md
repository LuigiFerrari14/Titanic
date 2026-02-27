# Titanic
Machine Learning project predicting Titanic survival using Logistic Regression and Random Forest with full evaluation metrics.


# 🚢 Projeto Titanic - Previsão de Sobrevivência

## 📖 Sobre o Projeto

Este projeto tem como objetivo prever quais passageiros sobreviveram ao naufrágio do Titanic utilizando técnicas de Machine Learning.

O dataset utilizado é o clássico dataset do Titanic (Kaggle), contendo informações como idade, sexo, classe, tarifa paga, entre outras variáveis.

O foco do projeto foi:

- Realizar tratamento de dados
- Explorar os dados com análise visual
- Aplicar modelos de classificação
- Avaliar métricas de desempenho
- Ajustar threshold com base na curva ROC
- Interpretar os coeficientes do modelo

---

## 🛠️ Tecnologias Utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn

---

## 📊 Tratamento de Dados

Foram realizadas as seguintes etapas:

- Preenchimento de valores ausentes na variável `Age` utilizando mediana agrupada por `Pclass` e `Sex`
- Criação da variável `has_cabin` (indicando presença ou ausência de cabine)
- Remoção das colunas `Cabin`, `Name`, `Ticket` e `PassengerId`
- Preenchimento da variável `Embarked` com a moda
- Conversão da variável `Sex` para formato numérico
- Aplicação de One-Hot Encoding na variável `Embarked`

---

## 📈 Análise Exploratória (EDA)

Foram analisadas:

- Distribuição de idade
- Idade por classe social
- Distribuição da tarifa por classe
- Taxa de sobrevivência por sexo

Essas análises ajudaram a entender padrões importantes nos dados antes da modelagem.

---

## 🤖 Modelos Utilizados

### 1️⃣ Regressão Logística

Modelo principal utilizado para previsão.

Foram avaliadas as seguintes métricas:

- Accuracy
- Recall
- Precision
- F1-Score
- ROC-AUC
- Matriz de Confusão
- Validação Cruzada (Stratified K-Fold)

Também foi realizado ajuste de threshold com base na menor distância ao ponto ideal (0,1) da curva ROC.

Além disso, foram analisados os coeficientes do modelo e calculadas as odds (exp(coef)) para interpretação das variáveis.

---

### 2️⃣ Random Forest

Modelo adicional treinado para comparação de desempenho com a Regressão Logística.

---

## 📉 Avaliação do Modelo

A performance foi avaliada utilizando:

- Hold-out (train/test split 80/20)
- Validação cruzada estratificada
- Curva ROC
- Matriz de confusão
- Comparação entre métricas de treino e teste para verificar possível overfitting

---

## 📌 Principais Insights

- Sexo é uma das variáveis mais relevantes para sobrevivência
- Passageiros da 1ª classe apresentaram maior taxa de sobrevivência
- Mulheres tiveram odds significativamente maiores de sobrevivência

---

## 🚀 Próximas Etapas

E agora?

- Split dos dados antes de qualquer transformação para evitar que estatísticas do teste influenciem o treino (data leakage) - pipeline  
- Explorar mais Feature Engineering exemplo o nome Mr, Ms..., esta sozinho?  
- Treinar outros modelos para comparar  
- Aplicação de escalonamento (padronização) nas variáveis numéricas Age e Fare  

---

## 🎯 Objetivo do Projeto

Projeto desenvolvido para fins de estudo e construção de portfólio na área de Ciência de Dados, com foco em boas práticas de modelagem e avaliação de modelos de classificação.

---

## 👨‍💻 Autor

Luigi Ferrari  
Graduado em Sistemas de Informação  
Foco em Ciência de Dados e Machine Learning
