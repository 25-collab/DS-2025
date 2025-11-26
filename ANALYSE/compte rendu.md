<img src="IMAGE CARTE ETUDIANT.jpg" style="height:464px;margin-right:432px"/>
## NOM ET PRENOM : OUMAIMA BENAZZOUZ
## FILIERE: CONTROLE, AUDIT ET CONSEIL
## GROUPE: 2


📊 Compte Rendu du Projet Machine Learning – Sales Insights
Ce document résume les différentes étapes exécutées dans le notebook Python consacré à l’analyse d’un problème business lié aux ventes (Sales Insights) en utilisant les techniques de Data Analytics et Machine Learning.

## 1. 🎯 Objectif du Projet

Le notebook vise à analyser un dataset de ventes afin de :
Comprendre les tendances commerciales,
Identifier les produits les plus performants,
Détecter les facteurs influençant les ventes,
Prédire le volume de ventes,
Classifier des catégories de produits selon leur performance.
Le projet suit l’ensemble du pipeline classique de Machine Learning.

## 2. 📥 Importation et Chargement des Données

Les bibliothèques utilisées incluent :
pandas
numpy
matplotlib
seaborn
scikit-learn
Les données sont chargées depuis un fichier CSV contenant des informations détaillées sur :
les produits,
les périodes de vente,
les catégories,
les volumes de ventes,
les prix.
Objectif de cette étape :
Préparer les données pour l’analyse,
Vérifier la structure du dataset,
Comprendre les types de variables.

## 3. 🔍 Exploration et Nettoyage des Données

Les actions réalisées :
Affichage des premières lignes du dataset (head()),
Analyse des valeurs manquantes,
Vérification des types de variables,
Résumé statistique (describe()).
Cette étape permet de :
Comprendre le comportement des données,
Identifier les valeurs extrêmes ou incohérences,
Définir les variables pertinentes pour la modélisation.

## 4. 📊 Visualisation des Tendances de Vente

Des visualisations graphiques sont générées à l’aide de matplotlib et seaborn :
Les principaux graphiques :
Line plot : évolution des ventes selon les saisons,
Bar charts : comparaison des catégories de produits,
Heatmaps : corrélations entre les variables,
Distribution plots : analyse de la répartition des volumes de ventes.
Objectif :
💡 Faire ressortir des tendances concrètes pour comprendre la dynamique du marché.

## 5. ⚙️ Préparation des Données pour Machine Learning

Étapes appliquées :
Encodage des variables catégorielles (get_dummies()),
Normalisation éventuelle des features,
Séparation du dataset en variables explicatives X et cible y,
Division en jeu d’entraînement et jeu de test (train_test_split).
Cette préparation constitue le socle nécessaire pour entraîner des modèles robustes.

## 6. 📈 Modèle de Régression Linéaire

Un modèle LinearRegression est entraîné pour prédire le volume de ventes.
Évaluation du modèle :
Mean Absolute Error (MAE)
Coefficient de détermination R²
Des visualisations "Actual vs Predicted" permettent de mesurer la qualité des prédictions.
Objectif :
📌 Estimer la performance future d’un produit en fonction de ses caractéristiques.

## 7. 🧠 Modèle de Régression Logistique (Classification)

Un modèle LogisticRegression est construit pour prédire une classe, par exemple :
Best-seller vs Non best-seller,
Article performant vs article faible.
Analyse \& Évaluation :
Matrice de confusion,
Score d’exactitude,
Précision, rappel, F1-score,
Visualisation des résultats.
Objectif :
🎯 Aider les responsables business à cibler les articles prometteurs.

## 8. 📤 Visualisation des Résultats des Modèles

Le notebook génère :
Scatters,
Courbes comparatives,
Heatmaps,
Graphiques d’actual vs. predicted,
Visualisations de décision.
Ces graphiques facilitent l’interprétation business des modèles ML.

## 9. 📝 Conclusion du Projet

Le notebook couvre l’ensemble du pipeline de Machine Learning appliqué au domaine du retail :
Chargement et exploration du dataset
Visualisation des insights
Préparation des données
Modélisation (régression + classification)
Évaluation et interprétation
Production de graphiques orientés business
Grâce à cette démarche, l’entreprise peut :
Optimiser ses stocks,
Identifier les produits à fort potentiel,
Prédire les ventes avec plus de précision,
Renforcer sa stratégie commerciale sur des données fiables.



