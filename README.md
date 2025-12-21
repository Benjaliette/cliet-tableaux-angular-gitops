# 🚀 GitOps Infrastructure - K3s sur Raspberry Pi 4

Repo pour déployer et gérer le site web www.cliet-tableaux.fr sur un cluster K3s avec ArgoCD, Traefik, et cert-manager.

## 🏗️ Architecture
Internet → Box (Port Forwarding 80/443)
    ↓
Raspberry Pi 4
    ↓
K3s Cluster
    ├── Traefik (Ingress Controller)
    ├── cert-manager (Let's Encrypt SSL)
    └── ArgoCD (GitOps)
        └── Applications (déployées depuis ce repo)
