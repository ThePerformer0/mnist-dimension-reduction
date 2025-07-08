# 🧠 MNIST Dimension Reduction

Ce projet explore et compare trois techniques de **réduction de dimension** appliquées au célèbre dataset **MNIST** (images de chiffres manuscrits). L’objectif est de transformer des données initialement en **784 dimensions** (28x28 pixels) vers **2 ou 3 dimensions** pour :
- Faciliter la **visualisation**,
- Réduire la complexité des modèles,
- Améliorer certaines étapes de **clustering ou classification**.

---

## 🎯 Objectifs pédagogiques

Ce projet a été conçu pour :
- Comprendre les **principes fondamentaux** de la réduction de dimension.
- Comparer les méthodes **linéaires (PCA)** et **non-linéaires (t-SNE, UMAP)**.
- Visualiser l’impact des réductions sur la séparation des classes.
- Analyser l’utilité de ces techniques en **prétraitement** avant clustering ou apprentissage supervisé.

---

## 📊 Techniques étudiées

| Méthode | Type | Avantages | Limites |
|--------|------|-----------|---------|
| **PCA** | Linéaire | Simple, rapide, interprétable | Ne capte pas les relations non linéaires |
| **t-SNE** | Non-linéaire | Très bon pour la visualisation locale | Coûteux, pas généralisable |
| **UMAP** | Non-linéaire | Rapide, préserve mieux la structure globale | Paramétrage plus complexe |

---

## 🧱 Structure du projet

```

mnist-dimension-reduction/
│
├── README.md                   # Documentation du projet
├── requirements.txt            # Bibliothèques à installer
├── .gitignore                  # Fichiers/dossiers à ignorer par Git
│
├── data/                       # Données d'entrée (CSV MNIST)
│   └── mnist.csv
│
├── notebooks/                  # Notebooks Jupyter pour chaque méthode
│   ├── 01\_pca\_mnist.ipynb
│   ├── 02\_tsne\_mnist.ipynb
│   ├── 03\_umap\_mnist.ipynb
│   └── 04\_comparaison.ipynb
│
├── src/                        # Fonctions Python réutilisables
│   ├── **init**.py
│   ├── utils.py
│   └── reducers.py
│
└── visualisations/             # Graphiques et figures générés
└── figures/

````

---

## ⚙️ Installation et exécution

```bash
# Cloner le repo
git clone https://github.com/ThePerformer0/mnist-dimension-reduction.git
cd mnist-dimension-reduction

# Créer un environnement virtuel
python3 -m venv venv
source venv/bin/activate

# Installer les dépendances
pip install -r requirements.txt
````

---

## 🧪 Datasets

Nous utilisons le dataset MNIST au format CSV :

* Lien Kaggle : [MNIST CSV Format – Aditya Kashyap](https://www.kaggle.com/datasets/adityaanilkashyap/the-mnist-dataset-in-csv-format)
* Contenu : 70 000 échantillons (60k train + 10k test), avec labels inclus
* Format : chaque ligne contient un label (0 à 9) suivi des 784 pixels

---

## 📈 Résultats attendus

📌 À compléter à la fin du projet :

* Graphiques 2D/3D montrant la séparation des chiffres par méthode
* Comparaison des performances (temps, clarté visuelle, structure)
* Analyse qualitative : structure locale vs globale

---

## 🧠 Interprétations & analyses

📌 À compléter à la fin du projet :

* Ce qu’on apprend sur la nature des données
* Utilité en prétraitement pour clustering/classification
* Cas où chaque méthode est préférable

---

## 🔗 Ressources utiles

* [scikit-learn – PCA & t-SNE](https://scikit-learn.org/stable/modules/manifold.html)
* [UMAP-learn Documentation](https://umap-learn.readthedocs.io/en/latest/)
* [MNIST Dataset Info – Yann LeCun](http://yann.lecun.com/exdb/mnist/)

---

## 🤝 Contribution

Toute contribution (amélioration du code, meilleure visualisation, benchmark additionnel…) est la bienvenue !
Pour contribuer :

1. Fork le projet
2. Crée une branche
3. Propose un Pull Request

---

## 🧑‍💻 Auteur

Projet réalisé par [ThePerformer](https://github.com/ThePerformer0) dans un but éducatif et de partage.
