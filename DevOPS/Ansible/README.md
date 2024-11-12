# ![ANSIBLE](https://img.shields.io/badge/ansible-%231A1918.svg?style=for-the-badge&logo=ansible&logoColor=white)



**Ansible est composé de trois concepts clés :**

- Inventaires : la liste des serveurs ou machines à gérer.
- Modules : des actions que l’on veut réaliser, comme installer un paquet, copier un fichier ou démarrer un service.
- Playbooks : des scripts qui orchestrent plusieurs modules pour accomplir une tâche complète.

*Ansible exécute des "instructions" appelées playbooks pour gérer ou configurer un ensemble de serveurs. Ces instructions sont écrites dans un langage clair (YAML), donc facile à lire, et elles sont structurées pour dire à Ansible quoi faire et sur quelles machines.*

## Les concepts principaux :

- Inventaire : L’inventaire est un fichier où l’on liste les machines cibles sur lesquelles Ansible va travailler. Chaque machine ou groupe de machines est associé à un nom (par exemple, web_servers pour tous les serveurs Web). L'inventaire par défaut se trouve dans /etc/ansible/hosts, mais vous pouvez créer un fichier d’inventaire personnalisé.

- Modules : Ce sont les “outils” qu’Ansible utilise pour exécuter des actions. Par exemple, un module d'installation de logiciel comme apt (pour les serveurs Ubuntu/Debian) installe des paquets, un module service démarre des services, etc. Ansible propose des centaines de modules pour gérer toutes sortes de tâches.

- Playbooks : Un playbook est un fichier YAML où l’on définit une série d'actions (ou tâches) pour configurer ou gérer les machines. C'est ici que l'on orchestre les modules pour réaliser des opérations précises.

![HowAnsibleWorks](https://github.com/NicolasW-7/AIS-DevOPS/blob/main/Images/HowAnsibleWorks.jpg)

# Comment installer ![ANSIBLE](https://img.shields.io/badge/ansible-%231A1918.svg?style=for-the-badge&logo=ansible&logoColor=white)

*Ansible est inclus dans les dépôts officiels, donc vous pouvez l’installer directement :*

```bash
sudo apt update
sudo apt install -y ansible
```
Exemple simple de playbook :

```yaml
Copier le code
- name: Configurer les serveurs web
  hosts: web_servers
  become: yes

  tasks:
    - name: Installer nginx
      apt:
        name: nginx
        state: present
```

## Comment exécuter un playbook

**Pour exécuter un playbook, on utilise la commande suivante :**

```bash
Copier le code
ansible-playbook -i <inventory_file> <playbook_file.yml>
```
-i : Spécifie le fichier d'inventaire.
playbook_file.yml : C’est le fichier contenant les tâches à exécuter.

## Les avantages d’Ansible
- Simplicité : Pas besoin d'installer de logiciel sur les machines gérées. Il suffit d’avoir accès en SSH.
- Facilité de lecture et d'écriture : Les fichiers YAML sont simples à lire et à comprendre, même pour les débutants.
- Automatisation sans agent : Contrairement à d'autres outils, Ansible ne nécessite aucun agent spécial sur les machines cibles, ce qui réduit la complexité de gestion.

## Exemple concret : installer et démarrer un service web

Supposons que vous vouliez installer et démarrer Nginx sur plusieurs serveurs. Voici un exemple de playbook Ansible pour y parvenir :

```yaml
---
- name: Installer et démarrer Nginx
  hosts: web_servers
  become: true  # Permet d'utiliser sudo

  tasks:
    - name: Installer Nginx
      apt:
        name: nginx
        state: present

    - name: Démarrer Nginx
      service:
        name: nginx
        state: started
```
*Lorsque vous lancez ce playbook, Ansible se connecte à tous les serveurs listés sous web_servers dans votre fichier d'inventaire, installe Nginx (s’il ne l’est pas déjà), et s’assure que le service est démarré.*

## Conclusion
**Ansible est un outil puissant pour l'automatisation IT. Avec un seul fichier d’inventaire et des playbooks bien conçus, vous pouvez configurer, déployer et gérer des centaines de serveurs de manière uniforme, rapide et fiable. Il rend l’automatisation accessible même sans expertise avancée, ce qui en fait un choix très populaire dans l’administration système et le DevOps.**
