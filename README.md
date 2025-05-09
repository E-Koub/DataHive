# 🧠 DataHive — Framework d’Analyse de Données Structuré

**DataHive** est un framework modulaire et scalable conçu pour les Data Analysts, Data Engineers ou Chefs de Projet SI souhaitant structurer un pipeline complet de traitement et d’analyse de données. Il s’appuie sur **Streamlit**, **Jupyter**, **PostgreSQL** et une architecture logicielle claire inspirée des bonnes pratiques du développement logiciel..

---

## 🚀 Objectifs

- Fournir un cadre réplicable pour les projets data
- Faciliter la collaboration entre Data Analysts, Data Scientists et Développeurs
- Proposer des composants réutilisables pour la transformation digitale des données

---

## 🧱 Architecture du projet

```bash
├── config/               # Fichiers de configuration (routes, logs, paramètres)
├── data/                 # Données organisées par niveau
│   ├── raw/              # Données brutes
│   ├── processed/        # Données nettoyées
│   ├── logs/             # Logs d'exécution
├── docker-compose.yml    # Déploiement multi-service
├── Dockerfile            # Conteneurisation de l’app
├── interactive/          # Espace pour scripts exploratoires
├── notebooks/            # Jupyter Notebooks pour exploration
├── public/app.py         # Point d'entrée Streamlit
├── reports/              # Rapports automatiques
├── src/automate/         # Exemple Pipeline spécifique : analyse d’automates
│   ├── ingestion/        # Chargement des données
│   ├── preparation/      # Nettoyage et pré-traitement
│   ├── analysis/         # Analyses descriptives/statistiques
│   ├── modeling/         # Modélisation machine learning
│   └── utils/            # Fonctions utilitaires
├── tests/                # Tests unitaires
├── vendor/dataHive/      # Composants core réutilisables
└── visualization/        # UI Streamlit
```

## 🚀 Fonctionnalités
    🔄 Ingestion & nettoyage automatisé des données

    📊 Visualisation géographique et analytique avec Streamlit & Folium

    ⚙️ Architecture modulaire Python (ingestion, préparation, analyse, modélisation)

    🧪 Notebooks Jupyter pour les tests et l’exploration

    🛢️ Base de données PostgreSQL intégrée

    📥 Interface PGAdmin pour la gestion des données
---

## 🐳 **Services Docker**

Le projet embarque plusieurs services orchestrés via Docker :
Service	Description
app	Application Streamlit (localhost:8501) — interface principale d’analyse.
jupyter	JupyterLab (localhost:8888) — prototypage et exploration libre.
db	PostgreSQL 15 Alpine — base de données relationnelle pour la data.
pgadmin	PGAdmin 4 (localhost:5050) — interface graphique pour PostgreSQL.
---

⚙️ Installation & Exécution
Prérequis

    Docker
    Docker Compose
    Python 3.11 (si utilisation en local sans Docker)

Lancer le framework avec Docker

    docker compose build --no-cache
    docker compose up -w

Accéder ensuite aux interfaces :

    📈 Streamlit : http://localhost:8501

    📓 JupyterLab : http://localhost:8888

    🗃️ PGAdmin : http://localhost:5050

🧪 Exécution en local (hors Docker)

    pip install --no-cache-dir  -e .
    streamlit run public/app.py

✅ Bonnes pratiques intégrées

    Structure modulaire : ngestion ➝ Préparation ➝ Analyse ➝ Visualisation

    Logging, routing YAML, gestion centralisée des paramètres

    Testabilité et extensibilité

    Organisation inspirée du cookiecutter data science

📢 Contribution

Les contributions sont les bienvenues ! Que ce soit pour améliorer les modules, corriger des bugs ou proposer des idées, ouvrez une issue ou une pull request.
