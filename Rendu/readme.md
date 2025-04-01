# Application Flask DevOps

Cette application Flask simple affiche l'adresse IP et le User-Agent du visiteur.

## Structure du projet
    /rendu
    ├── src/                      # Code source de l'application
    ├── Dockerfile                # Configuration Docker
    ├── .github/workflows/        # Pipelines CI/CD GitHub Actions
    ├── helm/                     # Chart Helm pour le déploiement
    ├── requirements.txt          # Dépendances Python
    ├── README.md                 # Documentation
    └── helm.md                   # Commandes d'installation des charts Helm

## Fonctionnement

L'application Flask est dockerisée et déployée sur un cluster Kubernetes via Helm. Le pipeline CI vérifie le code avec Flake8 et Bandit, puis construit et pousse l'image Docker. Le pipeline CD déploie l'application sur Kubernetes.

## Utilisation locale

```bash
# Créer et activer un environnement virtuel
python -m venv venv
source venv/bin/activate

# Installer les dépendances
pip install -r requirements.txt

# Lancer l'application
python src/app.py
```

## Docker

```bash

# Construire l'image
docker build -t flaskapp:latest .

# Exécuter le conteneur
docker run -p 8080:8080 flaskapp:latest

```

## Kubernetes
Le déploiement sur Kubernetes est géré par le chart Helm et les pipelines CI/CD.


