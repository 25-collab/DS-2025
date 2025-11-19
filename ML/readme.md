
# NOM: BENAZZOUZ
# PRENOM: OUMAIMA
# FILIERE: CONTROLE, AUDIT ET CONSEIL
# GROUPE: 1
# Rapport Descriptif du Notebook Machine Learning


---

## Objectif du notebook

Ce notebook met en œuvre une analyse de données et des modèles de machine learning sur le jeu de données "Wine Quality" de l'UCI. L’objectif principal est de modéliser la qualité des vins blancs à partir de mesures physico-chimiques en utilisant une approche de classification supervisée par un algorithme des k-plus proches voisins (k-NN)[file:1].

---

## Description des données utilisées

Le jeu de données exploité provient de l'UCI Machine Learning Repository et porte sur la qualité de vins blancs ("Vinho Verde") produits au Portugal. Il comporte :
- **4898 instances** (échantillons de vin)
- **11 variables** explicatives (physico-chimiques : acidité, sucre, sulfites, etc.)
- **1 cible** : la qualité du vin, notée entre 0 et 10, que le notebook réduit à deux classes (bons et mauvais vins)[file:1].

---

## Étapes principales et structure du code

Les étapes essentielles du notebook sont :
- **Chargement des packages** : pandas, numpy, matplotlib, seaborn, sklearn...
- **Importation des données** via ucimlrepo ou un lien CSV.
- **Inspection et nettoyage** : affichage du résumé du DataFrame, vérification des valeurs manquantes, aperçu de quelques lignes.
- **Transformation de la cible** : binarisation de la variable "quality" : qualité ≤ 5 = "mauvais" (0), qualité > 5 = "bon" (1).
- **Analyse exploratoire** : distribution des classes, diagrammes en boîte et matrice de corrélation pour explorer la structure des données.
- **Construction des ensembles d’apprentissage et validation** : séparation stratifiée.
- **Modélisation k-NN** : 
    - Boucle sur différentes valeurs de k pour le nombre de voisins.
    - Évaluation des taux d’erreur pour l’entraînement et la validation.
    - Sélection de la meilleure valeur de k (celle minimisant l’erreur sur validation).
- **Normalisation des variables** : standardisation des attributs via StandardScaler.
- **Évaluation du modèle** : prédiction et mesure de l’exactitude sur les ensembles de validation et test[file:1].

---

## Remarques complémentaires

- Le notebook propose également des graphiques (boîtes, heatmaps) pour l’analyse exploratoire.
- Les résultats incluent la détermination automatique de la valeur optimale de k pour la classification, ce qui montre la rigueur de la démarche.
- L’ensemble du projet illustre la chaîne complète "préparation des données – modélisation – évaluation", adaptée à l’apprentissage supervisé.

---

```


