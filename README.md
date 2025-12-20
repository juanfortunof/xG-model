⚽ Expected Goals (xG) Model from Scratch

📌 Español
Descripción del Proyecto

Este proyecto desarrolla un modelo de Expected Goals (xG) desde cero utilizando datos de StatsBomb.
El objetivo es estimar la probabilidad de que un tiro termine en gol a partir de características geométricas y contextuales del disparo.

A diferencia de usar modelos preconstruidos, este enfoque busca entender el impacto individual de cada variable, entrenando una regresión logística personalizada y analizando sus resultados en detalle.

📊 Datos

Fuente: StatsBomb Open Data

Unidad de análisis: Tiros

Variable objetivo:

shot_outcome (Gol = 1, No gol = 0)

🧮 Variables Utilizadas
1. Características Geométricas

Distancia euclidiana al arco

Ángulo de tiro (en grados)

Distancia al centro del arco (abs(40 - y))

2. Contexto del Tiro

Parte del cuerpo

Tipo de jugada (open play, set piece, etc.)

Técnica del disparo

Disparo a primer toque

Arco abierto (open goal)

Número de defensores entre el tirador y el arco

Distancia al balón

🤖 Metodología

Limpieza y transformación de datos

Ingeniería de variables geométricas

Selección de variables mediante Mutual Information

Entrenamiento de un modelo de Regresión Logística

Ajuste de pesos de clase para manejar el desbalance entre goles y no goles

Predicción de probabilidades (xG)

Evaluación del modelo y análisis de errores

Comparación visual con el modelo xG de StatsBomb

📈 Resultados y Análisis

El modelo asigna probabilidades coherentes según:

Distancia al arco

Ángulo de tiro

Presencia de defensores

Arco abierto

Se observa que el modelo tiende a:

Asignar xG más altos en tiros cercanos, comparado con StatsBomb

Se identifican posibles mejoras:

Incorporar mejor la relación entre distancia al balón y ejecución del disparo

Añadir información temporal o del portero

🛠️ Tecnologías Utilizadas

Python

Pandas

NumPy

Matplotlib / Seaborn

Scikit-learn

StatsBombPy

🚀 Posibles Extensiones

Uso de modelos no lineales (XGBoost, Random Forest)

Incorporar datos del portero

Entrenamiento por ligas o competiciones

Validación cruzada temporal

Aplicación del modelo a análisis de jugadores o equipos

----------------------------------------------------------------------------------------------------------

📌 English
Project Description

This project builds an Expected Goals (xG) model from scratch using StatsBomb data.
The goal is to estimate the probability that a shot results in a goal based on geometric and contextual shot features.

Instead of relying on pre-built models, this approach focuses on understanding the contribution of each variable, using a custom-trained logistic regression model and detailed exploratory analysis.

📊 Data

Source: StatsBomb Open Data

Unit of analysis: Shots

Target variable:

shot_outcome (Goal = 1, No Goal = 0)

🧮 Features Used
1. Geometric Features

Euclidean distance to goal

Shooting angle (degrees)

Distance to goal center (abs(40 - y))

2. Shot Context

Body part

Play type

Shot technique

First-time shot

Open goal indicator

Number of defenders in the shooting triangle

Distance to the ball

🤖 Methodology

Data cleaning and preprocessing

Feature engineering of geometric variables

Feature selection using Mutual Information

Training a Logistic Regression model

Class weight adjustment to handle goal imbalance

Probability prediction (xG)

Model evaluation and error analysis

Visual comparison with StatsBomb’s xG model

📈 Results and Insights

The model produces intuitive probabilities based on:

Shot distance

Shot angle

Defensive pressure

Open goal situations

Compared to StatsBomb, the model:

Tends to assign higher xG to close-range shots

Identified areas for improvement:

Better modeling of ball distance and shot execution

Inclusion of goalkeeper-related variables

🛠️ Technologies

Python

Pandas

NumPy

Matplotlib / Seaborn

Scikit-learn

StatsBombPy

🚀 Future Work

Non-linear models (XGBoost, Random Forest)

Goalkeeper positioning features

League- or competition-specific models

Temporal cross-validation

Player and team performance evaluation
