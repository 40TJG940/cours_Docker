# Commandes d'installation des charts Helm

## Installation de NGINX Ingress Controller

```bash
helm repo add bitnami https://charts.bitnami.com/bitnami
helm repo update
helm install nginx-ingress bitnami/nginx-ingress-controller
```
## Installation de Kubecost

```bash
helm repo add mesosphere-stable https://mesosphere.github.io/charts/stable
helm repo update
helm install kubecost mesosphere-stable/kubecost --namespace kubecost --create-namespace
```

Ces fichiers contiennent les informations essentielles pour votre projet :
- Le fichier requirements.txt liste les dépendances Python nécessaires pour l'application Flask
- Le README.md fournit une documentation générale du projet
- Le fichier helm.md contient les commandes pour installer les charts Helm requis (NGINX Ingress Co)