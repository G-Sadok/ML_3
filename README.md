# 🐟 Fish Weight Prediction: Regression Analysis

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-76B900?style=for-the-badge&logo=python&logoColor=white)

## 📖 Aperçu du Projet

Ce projet se concentre sur des tâches de **Régression** (Machine Learning Supervisé) utilisant le *Fish Dataset*. L'objectif est de prédire une variable continue, le **Poids (Weight)** d'un poisson, en fonction de ses mesures physiques et de son espèce.

Le projet compare différentes approches pour maximiser la précision des prédictions ($R^2$ Score), en explorant la sélection de caractéristiques et le réglage des hyperparamètres.

## 📂 Structure du Projet et Algorithmes

### 1. Régression Linéaire (`Fish Linear Regression.ipynb`)
Une approche statistique classique pour modéliser la relation entre les variables.
* **Feature Engineering :** Encodage des espèces (`LabelEncoder`).
* **Analyse de Corrélation :** Utilisation de `seaborn.heatmap` pour identifier les variables corrélées.
* **Sélection de Features Avancée :** Implémentation d'un algorithme de "Force Brute" qui teste **toutes les combinaisons possibles** de colonnes (Length1, Height, Width, etc.) pour trouver le groupe de variables offrant le meilleur score $R^2$.
* **Résultat :** Classement des 20 meilleures combinaisons.

### 2. Support Vector Regression - SVR (`Support Version Regression.ipynb`)
Utilisation des Machines à Vecteurs de Support pour la régression (`LinearSVR`).
* **Pré-traitement :** Application indispensable du `StandardScaler` pour normaliser les données, car les SVM sont sensibles aux échelles des variables.
* **Tuning d'Hyperparamètres :** Recherche de la valeur optimale pour le paramètre de régularisation **C** (test des valeurs `[0.01, 0.1, 1, 10, 100]`).
* **Visualisation :** Graphique de l'influence de `C` sur la performance du modèle.

### 3. Arbre de Décision (`Decision tree regression.ipynb`)
* *Structure prête pour l'implémentation d'un `DecisionTreeRegressor` (Work In Progress).*

## 🛠️ Stack Technique

* **Langage :** Python
* **Manipulation de Données :** Pandas, NumPy
* **Machine Learning :** Scikit-Learn (`LinearRegression`, `LinearSVR`, `StandardScaler`, `LabelEncoder`)
* **Visualisation :** Matplotlib, Seaborn

## 📊 Résultats Clés

Les notebooks génèrent des graphiques de comparaison "Réel vs Prédit" pour évaluer visuellement la qualité des modèles.
* La sélection de features a permis d'isoler les dimensions les plus pertinentes pour le poids.
* La normalisation des données a stabilisé la convergence du modèle SVR.

## 🚀 Installation et Utilisation

1.  **Cloner le dépôt :**
    ```bash
    git clone [https://github.com/ton-user/fish-regression.git](https://github.com/ton-user/fish-regression.git)
    cd fish-regression
    ```

2.  **Installer les dépendances :**
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn jupyter
    ```

3.  **Lancer les Notebooks :**
    ```bash
    jupyter notebook "Fish Linear Regression.ipynb"
    jupyter notebook "Support Version Regression.ipynb"
    ```

---

## 🇬🇧 English Summary

**Project:** Fish Weight Prediction (Regression)

**Goal:** Predict the continuous variable "Weight" based on physical measurements of fish using Linear Regression and SVR.

**Key Features:**
* **Brute-Force Feature Selection:** In the Linear Regression model, a custom loop tests all feature combinations to maximize the $R^2$ score.
* **SVR Optimization:** Implemented `LinearSVR` with data normalization (`StandardScaler`) and hyperparameter tuning for the regularization parameter `C`.
* **Evaluation:** Models are evaluated using $R^2$ scores and Scatter plots (True vs Predicted values).

**Tech Stack:** Python, Scikit-Learn, Pandas, Seaborn.
