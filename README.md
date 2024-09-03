### Classification de Trafic Réseau (Dataset KDD)

Ce projet implémente deux méthodes de classification du trafic réseau à partir du dataset KDD, utilisé pour la détection d'intrusions.

### Méthode 1 : Réseau de Neurones

- **Prétraitement :**
  - Mapping des étiquettes d'attaques en cinq catégories : `benign`, `probe`, `r2l`, `u2r`, `dos`.
  - Encodage des caractéristiques catégorielles (`protocol_type`, `service`, `flag`).
  - Normalisation des données.
- **Modélisation :**
  - Réseau de neurones à trois couches : entrée, cachée, sortie.
  - Activation ReLU, optimisation par SGD.
- **Résultats :**
  - Rapport de classification : précision, rappel, F1-score.
  - Visualisation de la perte d'entraînement et de validation.

### Méthode 2 : KMeans avec PCA

- **Prétraitement :**
  - Encodage des caractéristiques et réduction de dimensionnalité par PCA.
- **Clustering :**
  - Application de KMeans avec 5 clusters.
- **Résultats :**
  - Indice de Rand ajusté, précision.
  - Visualisation 3D des clusters après PCA.

### Exécution

- **Réseau de Neurones :** `python neural_network_classification.py`
- **KMeans avec PCA :** `python kmeans_clustering_pca.py`

### Données

- Dataset KDD a placer dans `./datasets/KDD/` sous les noms `KDDTrain+.txt` et `KDDTest+.txt`.

