# Projet Vaultwarden

**Le Projet Vaultwarden:**

- Répond à un besoin d'élévation de sécurité
- Facilite la gestion des mots de passe partagés
- Sensibilise à la gestion des MDP et à l'utilisation futur d'un Bastion.

**Vaultwarden c'est :**

- Un gestionnaire de mots de passe
- Auto-Hébergé
- Solution gratuite similaire a Bitwarden
- Facile à déploiyer et a réinstaller

# **La Timeline du Projet**

- 24 Octobre 2023 :
  - Définition du projet
  - Recherche complétementaire
  - Solution
- 20 Novembre 2023 :
1 er test d'installation de Vaultwarden
2 solutions retenue :
  - *Docker* (retenu)
  - Installation brut
- 28 Novembre 2023 :
    Edition de la première procédure d'installation.
- 1 Novembre 2023 :
    Edition du premier document technique.
- 1 février 2024 :
    Approfondissement après mise en "stand by" du projet.
- 26 Février 2024 :
    Complément docs technique
- 13 Mai 2024 :
    Recherche sur script base de données
  - Envoi de mail
  - Collection et adapatabilité à notre cadre
- 12 Juin 2024: Complément d'information
- 14 Juin Point d'avancé sur :
  - Créations des groupes
  - Vérification du transfert des bases de données
  - Réplication
- 26 Juin 2024 :  Verification définitive de la docs Vaultwarden
- 28 Juin 2024 : Point d'étape sur :
  - Création du présentation powerpoint
  - Test de compatibilité vers Linux pour Yubiker + Fonctionnement des clés.
- 10 Juillet 2024 : Présentation du projet : Responsable des différents services + DSI + Tuteur de stage
- 16 Juillet 2024 : Utilisation d'un token Argon2
- 30 Octobre 2024 : 
  - Mise en production
  - Finalisation des documents

**Procédure VaultWarden**
- Installation [EN]: https://github.com/NicolasW-7/AIS-DevOPS/blob/main/AIS/Proc%C3%A9dure/Linux/Installation%20Procedure%20Vaultwarden%20on%20Docker%20%5BEN%5D.md
- Script export database : https://github.com/NicolasW-7/AIS-DevOPS/blob/main/DevOPS/rsync_db.sh
- Token Argon2 : https://github.com/NicolasW-7/AIS-DevOPS/blob/main/AIS/Proc%C3%A9dure/Linux/G%C3%A9n%C3%A9rer%20un%20Token%20Argon2.md
- More   : https://github.com/NicolasW-7/AIS-Brief-et-TIPS/blob/main/Projet/Vaultwarden/Vaultwarden/Gen%C3%A9rer%20Un%20Token%20Argon2.md   
- Fichier : 
            - docker-compose.yml https://github.com/NicolasW-7/AIS-DevOPS/blob/main/DevOPS/Docker/docker-compose.yml
            - rsync_db.sh : https://github.com/NicolasW-7/AIS-DevOPS/blob/main/DevOPS/rsync_db.sh
            - https://github.com/NicolasW-7/AIS-DevOPS/blob/main/DevOPS/Caddyfile
