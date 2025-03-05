# Déploiement d'une Application Node.js avec Docker et GitHub Actions

## Description

Ce projet consiste à déployer une application Node.js utilisant le framework **Express.js** et se connectant à une base de données **MySQL**. Le processus de construction de l'image Docker est automatisé à l'aide de **GitHub Actions**, et le déploiement de l'application se fait sur un cluster Docker Swarm.

L'application récupère les informations de connexion à la base de données depuis des variables d'environnement sécurisées, et expose une route `/check-db` pour vérifier la connectivité à la base de données.

## Fonctionnement de l'application

L'application expose un endpoint **`/check-db`** qui vérifie si la connexion à la base de données est établie correctement.

### Variables d'environnement nécessaires :
- `DB_HOST`: L'adresse de la base de données (nom d'hôte ou adresse IP).
- `DB_USER`: Le nom d'utilisateur pour se connecter à la base de données.
- `DB_PASSWORD`: beugre.
- `DB_NAME`: test.

Le port de connexion de la base de données est fixé par défaut à **3306**, et l'application écoute sur le port **3000**.

## Prérequis

Avant de commencer, assurez-vous d'avoir les éléments suivants installés sur votre machine locale :

- **Docker** : Pour créer des conteneurs et gérer un cluster Docker.
- **Docker Compose** : Pour la gestion des services en local avant de passer en mode Swarm.
- **Git** : Pour la gestion des versions de votre projet.
- **GitHub** : Pour héberger votre projet et utiliser GitHub Actions.
- **Docker Hub** : Pour stocker et partager les images Docker.

## Installation et Configuration

### 1. Cloner le dépôt

Clonez ce dépôt sur votre machine locale :

```bash
git clone https://github.com/beugre-em/express-app-devops
cd express-app-devops
