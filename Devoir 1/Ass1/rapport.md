# OUMAIMA BENAZZOUZ
<img src="IMAGE CARTE ETUDIANT.jpg" style="height:464px;margin-right:432px"/>
Ce rapport synthétise les données démographiques et cliniques essentielles, les distributions, ainsi que les corrélations pour une analyse approfondie dans un contexte médical et machine learning. Le code Python fournit un outil simple pour générer ces statistiques et mieux comprendre le profil des patients du dataset 1988.[^1][^2][^3]

<div align="center">⁂</div>

[^1]: https://pmc.ncbi.nlm.nih.gov/articles/PMC11471268/

[^2]: https://archive.ics.uci.edu/ml/datasets/heart disease

[^3]: https://lecabinet4-0.fr/prompt-methodo/




Voici une analyse statistique descriptive détaillée du dataset "Heart Disease 1988," provenant des bases Cleveland, Hongrie, Suisse, et VA Long Beach, avec un total de 303 patients.

### Statistiques descriptives des variables quantitatives 

Les principales variables quantitatives analysées sont l'âge, la pression artérielle au repos, le cholestérol sérique et la fréquence cardiaque maximale.

- Âge : moyenne environ 54 ans, médiane proche, écart-type montrant une dispersion modérée, extrêmes entre 29 et 71 ans.
- Pression artérielle : moyenne autour de 131 mm Hg, avec un minimum de 94 et un maximum de 200.
- Cholestérol : moyenne élevée à environ 246 mg/dl, avec un large intervalle.
- Fréquence cardiaque maximale : moyenne proche de 150 battements par minute.


### Distribution des variables catégorielles

- Sexe : majorité d'hommes (environ 68%) par rapport aux femmes (32%).
- Sucre sanguin à jeun élevé (>120 mg/dl) : faible prévalence (environ 15% des patients).
- Type de douleur thoracique : varie en 4 classes, avec une répartition variable.
- Résultats ECG, angine d'effort, nombre de vaisseaux majeurs, et thallium ont également des répartitions spécifiques, utiles pour le diagnostic.


### Prévalence de la maladie cardiaque

- La cible binaire (présence ou absence de maladie) montre environ 54% de patients avec maladie (valeurs 1+) et 46% sans (valeur 0).


### Corrélations

- Les corrélations entre variables quantitatives et la maladie (target) ont été calculées, ce qui aide à comprendre les relations linéaires potentielles entre les facteurs cliniques et la pathologie.


### Gestion des valeurs manquantes

- Mention explicite de l'absence ou gestion des valeurs manquantes, garantissant la robustesse des analyses.

***

### Code Python pour reproduire cette analyse

```python
import pandas as pd
import numpy as np

# Chargement du dataset Heart Disease
# Remplacer 'heart_disease.csv' par le chemin réel du fichier

df = pd.read_csv('heart_disease.csv')

# Variables quantitatives
quant_vars = ['age', 'resting_bp', 'cholesterol', 'max_heart_rate']

# Statistiques descriptives
print(df[quant_vars].describe())
print(df[quant_vars].median())

# Variables catégorielles
cat_vars = ['sex', 'fasting_bs', 'chest_pain_type', 'ecg_result', 'exercise_angina', 'num_major_vessels', 'thal']
for var in cat_vars:
    print(df[var].value_counts())
    print(df[var].value_counts(normalize=True) * 100)

# Prévalence maladie cardiaque
print(df['target'].value_counts(normalize=True) * 100)

# Valeurs manquantes
print(df.isnull().sum())

# Matrice de corrélation
corr = df[quant_vars + ['target']].corr()
print(corr)
```
VA Long Beach, avec un total de 303 patients.

