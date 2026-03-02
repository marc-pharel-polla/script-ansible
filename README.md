# 🐳 Docker Host Automator (Ansible)

Ce projet permet d'automatiser l'installation et la configuration complète de Docker sur des serveurs distants tournant sous Fedora. Plus besoin de se connecter manuellement sur chaque machine.

## 🚀 Ce que fait l'outil
- **Update** : Met à jour les paquets système.
- **Install** : Installe le moteur Docker et Docker Compose.
- **Config** : Active le service au démarrage et gère les permissions utilisateurs.
- **Security** : Configure `firewalld` pour autoriser le trafic nécessaire.

## 📋 Prérequis
- Avoir **Ansible** installé localement.
- Avoir accès SSH par clé aux machines distantes.

## 🛠️ Utilisation
1. Listez vos adresses IP dans `inventory.yml`.
2. Lancez le script :
   ```bash
   ansible-playbook -i inventory.yml main.yml --ask-become-pass