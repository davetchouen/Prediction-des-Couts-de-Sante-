# Prediction-des-Coûts-de-Santé


# 🩺 Prédiction des Coûts de Santé : Analyse de Données et Modélisation des Reclamations d’Assurance Médicale aux États-Unis

## 📌 Contexte
Ce projet consiste à analyser un jeu de données d’assurance santé pour mieux comprendre les facteurs qui influencent les charges médicales facturées aux clients. L’étude est réalisée à l’aide de Python et de bibliothèques courantes telles que `pandas`, `matplotlib`, `seaborn` et `scikit-learn`.

## 🎯 Objectifs
- Explorer la distribution des variables dans le jeu de données.
- Identifier les relations entre les variables indépendantes et les charges médicales.
- Évaluer l’impact de certaines caractéristiques (âge, tabagisme, IMC, etc.) sur les coûts.
- Construire des modèles de régression pour prédire les charges.

## 🗂️ Jeu de données
Le jeu de données contient les colonnes suivantes :
- `age` : âge de l’individu
- `sex` : sexe
- `bmi` : indice de masse corporelle
- `children` : nombre d’enfants à charge
- `smoker` : statut de tabagisme
- `region` : région géographique
- `charges` : frais médicaux facturés

## 🔍 Analyse exploratoire (toutes les analyses sont dans le fichier Assurance santé analyse-1.ipynb)
- Distribution uniforme de l’âge sauf pour 18-19 ans (plus représentés).
- IMC suit une distribution gaussienne centrée autour de 30.
- Tabagisme : 20% de fumeurs, plus fréquents chez les hommes dans l’échantillon.
- Les fumeurs avec un IMC > 30 ont des charges significativement plus élevées.

## 📈 Modélisation
### Régression Linéaire Simple
- Modèle `charges ~ age` séparé pour non-fumeurs et fumeurs.
- Résultat : erreur moyenne (RMSE) ≈ 4000 $.

### Régression Multiple
- Modèle utilisant `age`, `bmi`, `children`, `smoker`, etc.
- Application de l’encodage pour les variables catégorielles (`sex`, `smoker`, `region`).
- Feature scaling avec `StandardScaler`.

### Comparaison des modèles
- Meilleurs résultats obtenus en séparant fumeurs et non-fumeurs.
  - Non-fumeurs : RMSE ≈ 4500 $
  - Fumeurs : RMSE ≈ 5000 $
  - Dataset combiné : RMSE ≈ 6000 $

## 🔧 Techniques employées
- Analyse univariée et bivariée
- Visualisation : histogrammes, scatter plots, box plots
- Corrélation et interprétation des coefficients
- Régression linéaire avec `scikit-learn`
- Standardisation des variables numériques
- Encodage one-hot des variables catégorielles

## 🧪 Évaluation
- Séparation d’un jeu de test
- Évaluation du modèle avec la Root Mean Squared Error (RMSE)
- Conclusion : la variable `smoker` est de loin la plus influente

## 📚 Fichiers
- `assurance santé analyse-1.ipynb` : notebook complet d’analyse
- `README.md` : documentation du projet (ce fichier)

## 🚀 Prochaines améliorations
- Tester des modèles plus complexes (Random Forest, XGBoost)
- Analyse de l’importance des variables
- Ajout de validation croisée


