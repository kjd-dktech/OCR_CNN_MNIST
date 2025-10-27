# OCR_CNN_MNIST

![status: work in progress](https://img.shields.io/badge/status-terminate-green)
![repo size](https://img.shields.io/github/repo-size/kjd-dktech/OCR_CNN_MNIST)
<!--![release](https://img.shields.io/github/v/release/kjd-dktech/OCR_CNN_MNIST)-->

<!--![python](https://img.shields.io/badge/python-3.8%2B-blue)-->

![PyPI - Version](https://img.shields.io/pypi/v/numpy)
![Python Versions](https://img.shields.io/pypi/pyversions/requests)
![tf](https://img.shields.io/badge/TensorFlow-2.2x-orange)

![stars](https://img.shields.io/github/stars/kjd-dktech/OCR_CNN_MNIST)
![forks](https://img.shields.io/github/forks/kjd-dktech/OCR_CNN_MNIST)

![model size](https://img.shields.io/badge/model-20.9MB-lightgrey)
[![dataset](https://img.shields.io/badge/dataset-available-green)](https://github.com/kjd-dktech/OCR_CNN_MNIST/raw/main/Data/data.zip)

![build](https://img.shields.io/github/actions/workflow/status/kjd-dktech/OCR_CNN_MNIST/ci.yml?branch=main)
![tests](https://img.shields.io/github/workflow/status/kjd-dktech/OCR_CNN_MNIST/CI?label=tests)

<!--
![coverage](https://img.shields.io/coveralls/github/kjd-dktech/OCR_CNN_MNIST)
![codecov](https://img.shields.io/codecov/c/github/kjd-dktech/OCR_CNN_MNIST)

![license](https://img.shields.io/github/license/kjd-dktech/OCR_CNN_MNIST)

![quality](https://img.shields.io/codacy/grade/PROJECT_ID)

![snyk](https://img.shields.io/snyk/vulnerabilities/github/kjd-dktech/OCR_CNN_MNIST)

![issues](https://img.shields.io/github/issues/kjd-dktech/OCR_CNN_MNIST)
![last commit](https://img.shields.io/github/last-commit/kjd-dktech/OCR_CNN_MNIST)

![docs](https://img.shields.io/readthedocs/your-project)

![docker pulls](https://img.shields.io/docker/pulls/your-docker-image)

![doi](https://img.shields.io/badge/doi-10.XXXX%2Fxxxx-blue)-->

## Description

Dépôt contenant le développement et l'entraînement d'un réseau de neurones convolutionnel (CNN) pour la classification de chiffres manuscrits, inspiré du jeu de données MNIST. Le projet rassemble le notebook d'expérimentation, les artefacts d'entraînement (modèles et checkpoints), les visualisations résultantes et les données prétraitées utilisées pour l'entraînement.

## Travail effectué

- Prétraitement des jeux de données (nettoyage, normalisation et mise en forme pour l'entraînement).
- Exploration et analyses effectuées dans le notebook `Notebooks/OCR_CNN_MNIST_2.ipynb`.
- Conception et entraînement d'un CNN pour la classification des chiffres manuscrits.
- Sauvegarde du modèle final et des checkpoints d'entraînement dans `Models/`.
- Génération de graphiques et métriques d'entraînement (courbes d'accuracy/loss, matrice de confusion, exemples prédits) conservés dans `Outputs/`.
- Production d'un jeu de données prétraité stocké dans `Processed_Data/` pour réutilisation et évaluation.

## Arborescence importante

- `Notebooks/OCR_CNN_MNIST_2.ipynb` — notebook principal (prétraitement, entraînement, évaluation).
- `Data/` — jeux de données bruts fournis (CSV et archives).
- `Processed_Data/` — fichiers produits par le prétraitement (pickle).
- `Models/` — modèle final (`mnist_cnn.keras`) et `checkpoints/` pour les sauvegardes par epoch.
- `Outputs/` — graphiques, logs d'entraînement et `final_metrics.json`.
- `Ressources/` et `RP/` — documents de rapport et images d'architecture.
- `ocrcnnmnist2venv/` — environnement virtuel utilisé localement.

## Installation

Les instructions ci‑dessous supposent un environnement Linux/Unix avec Python 3.8+.

1. Créer et activer un environnement virtuel (recommandé) :

```bash
python -m venv .venv
source .venv/bin/activate
```

2. Installer les dépendances :

```bash
pip install -r requirements.txt
```

## Utilisation

- Ouvrir `Notebooks/OCR_CNN_MNIST_2.ipynb` dans Jupyter ou JupyterLab et exécuter les cellules dans l'ordre pour reproduire le prétraitement, l'entraînement et l'évaluation.
- Le modèle final est disponible dans `Models/mnist_cnn.keras` et peut être chargé avec TensorFlow / Keras :

```python
from tensorflow import keras
model = keras.models.load_model('Models/mnist_cnn.keras')
# prédire sur des données préparées : model.predict(x)
```

## Résultats

Les résultats d'entraînement (courbes, matrice de confusion, exemples annotés) et les métriques finales se trouvent dans le répertoire `Outputs/`. Le fichier `final_metrics.json` résume les métriques principales obtenues sur l'évaluation.

## Reproductibilité

- Les checkpoints dans `Models/checkpoints/` permettent d'inspecter ou de reprendre l'entraînement à différents points.
- Pour reproduire les résultats, exécuter les cellules du notebook et s'assurer d'utiliser des versions proches des dépendances listées dans `requirements.txt`.

## Licence

## Contact

**Kodjo Jean DEGBEVI** - `kodjojeandegbevi@gmail.com`
