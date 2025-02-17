<!-- # Documentation-SQL
SQL création d'une documentation collaborative -->

# Procédure d'installation de git clone

## Cloner le dépôt GitHub :

Ouvrez l'invite de commande <b>(cmd)</b> ou <b>Git Bash.</b><br><br>

Commencez par cloner le dépôt sur votre machine locale :<br>
Une fois le dépôt cloné, il est nécessaire d'installer les dépendances du projet.<br>
Pour ce faire, exécutez la commande suivante dans le terminal à la racine du projet :<br>

```bash
git clone https://github.com/Nanas63/Documentation-SQL.git
cd Documentation-
```

## 📂 Documentation-SQL
```bash
│── 📄 README.md         # Introduction et guide d'utilisation
```
<br><br>

# Introduction à SQL 🛠️
SQL (Structured Query Language) est un langage utilisé pour manipuler et gérer les bases de données relationnelles.
<br>

## Pourquoi apprendre SQL ?

* Interagir avec des bases de données efficacement.
* Extraire des informations utiles grâce à des requêtes.
* Utilisé dans de nombreux systèmes de gestion de bases de données (MySQL, PostgreSQL, SQLite...).

## Qu’est-ce qu’une base de données relationnelle ?
Une base de données relationnelle stocke des données sous forme de tables composées de lignes et de colonnes.
Chaque table possède une clé primaire qui identifie de manière unique chaque entrée.

<br><br>

---
👉 [Passer à l'installation de WAMP](installation-wamp.md)

## Installation et utilisation de WAMP sur Windows

## Qu'est-ce que WAMP ?
WAMP (Windows, Apache, MySQL, PHP) est un environnement de développement permettant d’exécuter un serveur web en local avec MySQL.

### Installation de WAMP

## Télécharger WAMP

* Rendez-vous sur le site officiel : [https://www.wampserver.com/](https://www.wampserver.com/)
* Téléchargez la version correspondant à votre système (32 ou 64 bits).
* Installez-le en suivant les instructions.
<br>
## Lancer WAMP

* Ouvrez WAMP et assurez-vous que l’icône devient verte (cela signifie que le serveur fonctionne).

<br><br>

# Interface web pour MySQL : phpMyAdmin

## Qu’est-ce que phpMyAdmin ?
phpMyAdmin est une interface web qui permet de gérer facilement les bases de données MySQL.
<br><br>

## Accéder à phpMyAdmin

1. Démarrer WAMP et vérifier que l’icône est verte. Click gauche sur l'icon verte pour accédez à phpMyAdmin via WAMP


2. Ouvrir un navigateur et entrer l’URL :

```bash
http://localhost/phpmyadmin/
```

3. Bienvenue dans phpMyAdmin


* Utilisateur : root

* Mot de passe : (laisser vide par défaut)

* Choix du serveur : MySql


## Comment créer sa base de données ?

* création via l'interface graphique
* création manuelle


Exemple d'une création manuelle :

1. Aller dans l'onglet SQL

2. Entrer la requête :

```bash
CREATE DATABASE (Nom de la base)
DEFAULT CHARACTER SET utf8
DEFAULT COLLATE utf8_general_ci;

```

3. Exécuter
<br><br>

## Comment créer une table ?

```bash
CREATE TABLE country(
id INT PRIMARY KEY AUTO_INCREMENT NOT NULL,
label VARCHAR(255) NOT NULL
    
)ENGINE=INNODB;
```







