# 📊 Projet – Analyse Cinématographique : Exploration & Visualisation des Données

![](streamlit_app/architecturephase2.png)

## 🎯 Objectif
Déployer une chaîne complète d’analyse et de visualisation à partir de données issues d’une API cinématographique, en exploitant un SDK Python, Jupyter Notebook, et une application web interactive développée avec Streamlit.

---

## 🔍 Analyse Exploratoire des Données (EDA)

### 🔹 Interrogation de l'API via un SDK Python
- Utilisation du SDK `damsmoviesdk` développé pour ce projet
- Récupération des données de films, notes, genres, utilisateurs
- Analyse des tendances dans les notes de films
- Étude des genres cinématographiques les plus populaires
- Identification de profils utilisateurs selon leurs évaluations

### 🔹 Notebook Jupyter interactif
- Analyse pas à pas avec cellules indépendantes
- Visualisations dynamiques intégrées (`matplotlib`, `seaborn`)
- Documentation fluide avec Markdown
- Création d’un notebook lisible et réutilisable dans un portfolio professionnel

➡️ **Fichier livré** : `movies_analytics/film_data_analysis.ipynb`

---

## 📈 Visualisation avancée avec Streamlit

### 🔹 Création d’une application web interactive
- Développement d’une app multi-pages avec navigation
- Visualisation des tendances du cinéma par genres, notes et tags
- Intégration de **filtres dynamiques** et **graphes interactifs**
- Utilisation des bibliothèques Python les plus adaptées : `matplotlib`, `seaborn`, `pandas`

### 🔹 Fonctionnalités de l'application
- Exploration interactive des films les mieux notés
- Tri par genre, utilisateur, moyenne de notes
- Affichage dynamique des données enrichies (liens IMDb, affiches de films via API OMDb)

➡️ **Structure de l'app Streamlit** :  
- `movielens_app.py` : point d’entrée  
- `page0.py`, `page1.py`, `page2.py`, `page3.py` : Les différentes pages de l’application  
- Visualisation directe depuis navigateur local via la commande: `streamlit run movielens_app.py`

➡️ **Fichier livré** : `movies_analytics/streamlit_app`

---

## 🖼️ Enrichissement des données (affiches & IMDb)

- Appel à l’API OMDb pour récupérer les **liens vers les affiches de films** et leurs pages IMDb
- Génération d’un fichier `.parquet` enrichi : `output/links_enriched.parquet`

➡️ **Fichier Python livré** : `get_movie_poster.py`

---

## ⚙️ Environnement de travail

### 🔧 Mise en place locale
- Dépôt Git structuré : une phase = un répertoire
- Environnement virtuel Python avec `venv`
- Utilisation de **VSCode** comme IDE principal

### 🔢 Installation & lancement
```bash
# Cloner le projet
git clone https://github.com/DamaSangare/movies_analytics.git
cd movies_analytics

# Créer et activer l’environnement virtuel
python -m venv .venv
source .venv\Scripts\activate # ou  source .venv/bin/activate sous Linux

# Installer les dépendances nécessaires
pip install damsmoviesdk
pip install streamlit
