# Cloud Infrastructure Setup

## Description
Configuration d'infrastructure cloud automatisée avec Ansible et Docker Compose. Déploiement de services containerisés sur serveurs distants avec playbooks de provisioning et de déploiement.

## Services déployés
- **Web applications** conteneurisées
- **Base de données** PostgreSQL/MySQL
- **Reverse proxy** Nginx/Traefik
- **Monitoring** avec Prometheus/Grafana
- **Backup automatisé** des données
- **SSL/TLS** avec Let's Encrypt

## Technologies utilisées
- **Ansible** pour l'automation
- **Docker & Docker Compose** pour la containerisation
- **Nginx** comme reverse proxy
- **Ubuntu/Debian** servers
- **SSH** pour l'accès distant

## Structure du projet
```
cloud-1/
├── inventory.ini      # Inventaire des serveurs
├── playbook.yml      # Playbook principal Ansible
├── docker-compose.yml # Services containerisés  
├── clean.sh          # Script de nettoyage
└── README.md         # Documentation
```

## Installation et configuration

### Prérequis
- Ansible installé localement
- Accès SSH aux serveurs cibles
- Docker disponible sur les serveurs

### Configuration
1. Modifier `inventory.ini` avec vos serveurs
2. Configurer les clés SSH
3. Adapter `docker-compose.yml` selon besoins

### Déploiement
```bash
# Test de connectivité
ansible all -i inventory.ini -m ping

# Déploiement complet
ansible-playbook -i inventory.ini playbook.yml

# Nettoyage
./clean.sh
```

## Playbook Ansible
- **Setup** des dépendances système
- **Installation** de Docker et Docker Compose
- **Configuration** des services
- **Déploiement** des applications
- **Configuration** du firewall et sécurité

## Services configurés
- Applications web en haute disponibilité
- Base de données avec réplication
- Monitoring et alerting
- Backups automatiques
- Certificats SSL automatiques

## Sécurité
- **Firewall** configuré (ufw)
- **SSH** sécurisé avec clés
- **Utilisateurs** non-root pour services
- **Secrets** gérés avec Ansible Vault
- **Updates** automatiques du système

## Monitoring
- Métriques système avec node-exporter
- Logs centralisés
- Alertes par email/Slack
- Dashboard Grafana

## Compétences développées
- Infrastructure as Code (IaC)
- Automation avec Ansible
- DevOps et containerisation
- Administration système Linux
- Sécurité des serveurs

## Auteur
Alexandre Pommier (kinou-p)