# 🧠 MLP Keras - Classificação de Câncer (WDBC)

## 📌 Visão Geral

Este projeto utiliza uma **Rede Neural Artificial (MLP - Multilayer Perceptron)** com a API do Keras para realizar a classificação de tumores de mama como **benignos ou malignos**, com base em características extraídas de células.

O objetivo é aplicar conceitos fundamentais de redes neurais em um problema real de classificação binária na área da saúde.

---

## 🎯 Objetivo

Desenvolver um modelo de Deep Learning capaz de:

- Classificar tumores como benignos (0) ou malignos (1)
- Aprender padrões não lineares em dados tabulares
- Avaliar desempenho utilizando métricas de classificação

---

## 📊 Dataset

**WDBC - Wisconsin Diagnostic Breast Cancer**

- Tipo: Classificação binária
- Classes:
  - M → Maligno (1)
  - B → Benigno (0)
- Features: 30 variáveis numéricas derivadas de imagens de células mamárias

---

## 🧠 Conceitos Aplicados

### 🔹 Neurônio Artificial
Unidade básica que realiza combinações lineares e aplicação de função de ativação.

### 🔹 Perceptron
Modelo inicial de rede neural para separação linear.

### 🔹 MLP (Multilayer Perceptron)
Rede neural com múltiplas camadas capazes de aprender relações não lineares.

### 🔹 Funções de Ativação
- ReLU nas camadas ocultas
- Sigmoid na camada de saída

### 🔹 Função de Perda
- binary_crossentropy (classificação binária)

### 🔹 Otimizador
- Adam (otimização adaptativa dos pesos)

---

## ⚙️ Pipeline do Projeto

1. Carregamento do dataset
2. Separação entre features (X) e target (y)
3. Conversão do target para valores numéricos
4. Normalização dos dados (StandardScaler)
5. Divisão treino/teste
6. Construção do modelo MLP
7. Compilação do modelo
8. Treinamento da rede
9. Avaliação do modelo
10. Predição e validação final

---

## 🧱 Arquitetura do Modelo

```python
Dense(16, activation='relu')
Dense(8, activation='relu')
Dense(1, activation='sigmoid')

## 📈 Avaliação do Modelo

### 📊 Matriz de Confusão

```text
[[72  0]
 [ 2 40]]

## 📌 Métricas

- Accuracy: ~98%
- Precision: alta
- Recall: alto para classe positiva
- Boa capacidade de generalização