
# OVA pour le développement et les tests d'applications PHP avec CodeIgniter 3.1.13

Cette OVA est configurée pour faciliter le développement et les tests d'applications PHP basées sur le framework CodeIgniter 3.1.13 dans des environnements locaux. La configuration est conçue pour être utilisée dans un environnement de développement et n'inclut pas de configurations VHOSTs, IPTables ou SSL afin d'éviter des complications inutiles dans ce contexte.

## Caractéristiques de l'OVA

- **Système d'exploitation :** Ubuntu 24.04 LTS
- **Serveur Web :** Apache 2.4.62
- **Langage de programmation :** PHP 8.3
- **Framework :** CodeIgniter 3.1.13
- **Base de données :** MySQL 8.3.9
- **Accès Session, SSH et MySQL :**
  - **Utilisateur :** `devadmin`
  - **Mot de passe :** `d3v4dm1n`

## Télécharger, accéder et utiliser

Tout d'abord, il est nécessaire de télécharger l'OVA. Pour ce faire, cliquez sur le lien suivant :
[Développement d'applications avec CI 3.1.13.ova](https://mega.nz/file/5oJCEYja#M6ICl_uhYz6b5lHPucNpQq7NyWLixTW-Eh0pOLeUcxI)

Pour utiliser cette OVA, vous devez l'importer dans Virtualbox ou VMware et configurer l'interface réseau comme NAT ou une autre option. Une fois la VM configurée et démarrée, vous devez y accéder avec les identifiants de session, et pour obtenir l'adresse IP de la machine, exécutez la commande

```bash
ip a
```

### SSH

Pour accéder à la machine virtuelle via SSH, utilisez les identifiants suivants :

- **Utilisateur :** `devadmin`
- **Mot de passe :** `d3v4dm1n`

```bash
ssh devadmin@<IP-de-l'OVA>
```

### MySQL

Pour accéder à MySQL :

```bash
mysql -u devadmin -p
```

### Environnement de travail

L'environnement de travail est situé dans le répertoire `/var/www/html`, qui est divisé en :

- `/var/www/html/sql` : pour le gestionnaire de base de données (PHPMyAdmin 5.2.1), accessible via l'URL : http://<IP-de-l'OVA>/sql/
- `/var/www/html/public` : pour CodeIgniter 3.1.13, accessible via l'URL : http://<IP-de-l'OVA>/public/

### Apache

Apache est configuré pour servir le projet depuis le répertoire `/var/www/html`. Il n'est pas nécessaire de modifier les configurations de VHOST pour l'environnement de développement.

### PHP

L'OVA inclut PHP 8.3 avec les extensions nécessaires pour exécuter CodeIgniter et d'autres applications web courantes. Si vous devez installer des extensions supplémentaires, vous pouvez le faire en utilisant `apt-get`.

```bash
sudo apt install php-<extension>
```

## Notes supplémentaires

- Cette OVA est configurée pour des environnements locaux et n'est pas recommandée pour une utilisation en production.
- Pour tout problème ou question, contactez-moi.

## Licence

Cette OVA est fournie telle quelle, sans aucune garantie. Utilisez-la à vos propres risques.
