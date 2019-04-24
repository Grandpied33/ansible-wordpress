
# ansible-wordpress

Ce projet permet de lancer un script ansible qui va installer Wordpress, PHP 7.0, un serveur FTP, et MYSQL. Testé sur Ubuntu 16.04.

## Configurer vos VM :

Dans `host_vars` editer le fichier `vm1devops.yml`.
Il contient déjà une ligne : 

    ansible_host: ERTYerty1234@20.188.38.101

Remplacer `ERTYerty1234@20.188.38.101` par votre IP

/!\ Si vous vous connectez à la VM via une clé SSH conservez la forme suivante : `NomUtilisateur@IP` /!\

A la racine de votre projet éditez le 

    ansible.cfg

A la ligne 3 après `remote_user` , indiquez l’utilisateur de votre VM.

Pensez dans votre VM à ouvrir les ports 22 et 80.

**Configurer MySQL**

Dans `roles\mysql\defaults\main.yml` Mettez vos identifiants de base :

    wp_mysql_db: wordpress
    wp_mysql_user: ERTYerty1234
    wp_mysql_password: root
Indiquez vos identifiants souhaités.

**Lancer le script**

Pour lancer le script, vous devez vous rendre à la racine de votre projet : lancer la commande : 

    ansible-playbook -i invent ory playbook.yml

Si ansible n'est pas installé sur votre machine, [installez le](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html).

Une fois ces étapes réalisées votre le script va s’exécuter.
 
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  

