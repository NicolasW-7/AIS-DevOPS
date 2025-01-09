# ![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
Docker est une plateforme qui permet de créer, déployer et exécuter des applications à l’intérieur de containers. Un container est une unité standardisée de logiciel qui emballe le code et toutes ses dépendances, de sorte que l’application puisse s'exécuter de manière rapide et fiable d'un environnement à un autre.

![Docker](https://github.com/NicolasW-7/AIS-DevOPS/blob/main/Images/Docker.jpg)

## Fonctionnement de Docker :

- Images Docker :  Une image est un modèle statique contenant tout ce dont une application a besoin pour fonctionner (code, bibliothèques, dépendances). Les images Docker sont créées à partir d'un fichier de configuration appelé Dockerfile, qui définit la structure de l'image.

- Containers Docker : Un container est une instance exécutable d’une image. Lorsqu'une image est lancée, Docker crée un container qui isole l’application de l’environnement sous-jacent tout en permettant à celle-ci de fonctionner normalement. Plusieurs containers peuvent être exécutés à partir de la même image.

- Docker Daemon : C’est le processus principal qui gère les containers Docker. Il écoute les requêtes Docker et exécute les instructions pour créer, démarrer, arrêter ou supprimer des containers.

- Docker CLI : La ligne de commande Docker (CLI) permet à l’utilisateur de communiquer avec le daemon Docker pour exécuter des commandes comme docker run, docker build, docker ps, etc.

## Commandes principales :

- docker build : Crée une image à partir d'un Dockerfile.
- docker run : Lance un container à partir d’une image.
- docker ps : Affiche les containers en cours d’exécution.
- docker stop : Arrête un container.
- docker exec : Exécute des commandes dans un container en cours d'exécution.

# Docker Compose

![Docker](https://github.com/NicolasW-7/AIS-DevOPS/blob/main/Images/Docker%20Compose.png)

Docker Compose est un outil qui permet de définir et gérer des applications multi-containers. Il utilise un fichier YAML (docker-compose.yml) pour décrire les services, réseaux et volumes nécessaires à l'application.

## Fonctionnement de Docker Compose :

- Fichier docker-compose.yml : Il contient la définition des services (containers), volumes et réseaux nécessaires pour faire fonctionner une application. Chaque service peut être une image Docker différente, avec des paramètres spécifiques comme les ports, volumes partagés, variables d’environnement, etc.

- Déploiement multi-containers : Avec Docker Compose, on peut définir plusieurs services qui s’exécutent ensemble. Par exemple, une application web peut avoir un service pour le serveur web (comme Nginx), un autre pour la base de données (comme MySQL), etc. Compose gère les interactions entre ces services.

## Commandes principales de Docker Compose :

- docker-compose up : Démarre les containers définis dans le fichier docker-compose.yml.
- docker-compose down : Arrête et supprime les containers, réseaux et volumes.
- docker-compose build : Reconstruit les images à partir des configurations.
- docker-compose logs : Affiche les logs des services.
  
Exemple de fichier docker-compose.yml :

https://github.com/NicolasW-7/AIS-DevOPS/blob/main/DevOPS/Docker/docker-compose.yml


## Résumé des différences :
- Docker : Permet de gérer des containers individuels.
- Docker Compose : Permet de gérer plusieurs containers en tant qu'application, avec un fichier de configuration unique.
