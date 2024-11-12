# PKI

Une PKI (Public Key Infrastructure), ou Infrastructure à Clé Publique, est un ensemble de technologies, de politiques et de procédures utilisées pour gérer et sécuriser l'utilisation des clés cryptographiques dans un système de communication ou de stockage sécurisé.

![PKI](https://github.com/NicolasW-7/AIS-DevOPS/blob/main/Images/PKI.jpg)

- *Image from : https://medium.com/@signmycode/what-is-code-signing-with-public-key-infrastructure-pki-3c60843c559e*

La PKI repose principalement sur l'utilisation de la cryptographie asymétrique (également appelée cryptographie à clé publique), dans laquelle chaque utilisateur ou entité dispose de deux clés :

- Une clé publique, qui peut être partagée librement.
- Une clé privée, qui doit rester secrète.

## Les éléments principaux d'une PKI

### 1. Clés publiques et privées :

- Clé publique : Cette clé est utilisée pour chiffrer les données ou pour vérifier une signature numérique. Elle est partagée publiquement.
- Clé privée : Cette clé est utilisée pour déchiffrer les données chiffrées avec la clé publique ou pour signer des données, garantissant ainsi leur authenticité et intégrité. Elle doit être gardée secrète.

### 2. Certificat numérique : 

Un certificat est un fichier électronique qui associe une clé publique à une entité (comme une personne, une organisation, un serveur, etc.). Le certificat contient des informations importantes telles que :

- La clé publique.
- Les informations sur l'entité (par exemple, son nom, son adresse, etc.).
- La date de validité du certificat.
- L'Autorité de Certification (CA) qui a signé le certificat.

### 3. Autorité de Certification (CA) : 
L'Autorité de Certification (CA) est une entité de confiance chargée de délivrer et de gérer les certificats numériques. Elle valide l'identité de l'entité avant de lui délivrer un certificat. L'AC utilise sa propre clé privée pour signer les certificats qu'elle délivre, et cette signature peut être vérifiée avec la clé publique de l'AC.

### 4. Registre des certificats (CRL - Certificate Revocation List) :
La CRL est une liste maintenue par l'Autorité de Certification, qui contient des certificats révoqués avant leur date d'expiration. Cela permet aux systèmes d'éviter d'accepter des certificats invalides ou compromis.

### 5. Protocoles :

- SSL/TLS : Utilisé pour sécuriser les communications entre un client (par exemple, un navigateur) et un serveur web.
- S/MIME : Utilisé pour sécuriser les e-mails en garantissant leur confidentialité et leur intégrité.
- VPN : Utilise des certificats pour sécuriser les connexions entre des utilisateurs distants et un réseau privé.

## Fonctionnement de la PKI

### 1. Génération de clés: 
L'utilisateur ou l'entité génère une paire de clés, une publique et une privée. La clé publique est envoyée à une Autorité de Certification (CA) pour être intégrée dans un certificat numérique.

### 2. Délivrance du certificat:
La CA vérifie l'identité de l'entité demandant un certificat. Une fois l'identité validée, la CA émet un certificat numérique en signant la clé publique de l'entité avec sa propre clé privée.

### 3. Utilisation du certificat: 
Les utilisateurs peuvent maintenant échanger des données en toute sécurité :

- Pour envoyer des données sécurisées, l'expéditeur chiffre les données avec la clé publique du destinataire.
- Le destinataire utilise sa clé privée pour déchiffrer les données.

De plus, les signatures numériques sont utilisées pour garantir que les données proviennent bien de l'entité signataire et n'ont pas été modifiées.

## Applications de la PKI
- Sécurisation des sites web : Le protocole HTTPS (qui repose sur SSL/TLS) utilise la PKI pour sécuriser les échanges entre le serveur web et le navigateur.
- Signature numérique : Les documents électroniques, les transactions et les e-mails peuvent être signés numériquement pour en garantir l'authenticité et l'intégrité.
- Authentification des utilisateurs : Les certificats numériques sont souvent utilisés pour prouver l'identité d'un utilisateur lors de la connexion à un service ou à un réseau (par exemple, dans le cas des VPNs).
- Chiffrement des données sensibles : La PKI permet de chiffrer les communications et les fichiers afin de les protéger contre l'accès non autorisé.

## Avantages de la PKI
- Sécurité : La PKI fournit des mécanismes de sécurité forts pour protéger les informations sensibles (par exemple, via le chiffrement, l'authentification et les signatures numériques).
- Non-répudiation : Grâce aux signatures numériques, une entité ne peut pas nier l'avoir effectuée, car seule la clé privée correspondante peut signer un message.
- Gestion centralisée : La gestion des clés et des certificats est facilitée par l'infrastructure centralisée de la PKI.

## Conclusion
En résumé, une PKI (Public Key Infrastructure) est une infrastructure cryptographique qui permet de gérer de manière sécurisée l'échange de données à l'aide de la cryptographie asymétrique. Elle permet notamment d'authentifier les entités, de garantir la confidentialité des échanges et de vérifier l'intégrité des données par l'utilisation de clés publiques et privées, de certificats numériques et d'Autorités de Certification.
