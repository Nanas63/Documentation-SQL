<!-- # Documentation-SQL
SQL création d'une documentation collaborative -->

# Préalable à l'utilisation de Mysql
<br><br>

## Procédure d'installation de git clone

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

# Introduction à SQL <br>

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
<br>
### Installation de WAMP
<br>
### Télécharger WAMP
<br>
* Rendez-vous sur le site officiel : [https://www.wampserver.com/](https://www.wampserver.com/)
* Téléchargez la version correspondant à votre système (32 ou 64 bits).
* Installez-le en suivant les instructions.
<br>
### Lancer WAMP

* Ouvrez WAMP et assurez-vous que l’icône devient verte (cela signifie que le serveur fonctionne).

<br><br>

# Interface web pour MySQL : phpMyAdmin

## Qu’est-ce que phpMyAdmin ?
phpMyAdmin est une interface web qui permet de gérer facilement les bases de données MySQL.
<br><br>

## Accéder à phpMyAdmin
<br>
1. Démarrer WAMP et vérifier que l’icône est verte. Click gauche sur l'icon verte pour accédez à phpMyAdmin via WAMP


2. Ouvrir un navigateur et entrer l’URL :

```bash
    http://localhost/phpmyadmin/
```
<br>
3. Bienvenue dans phpMyAdmin

```bash
* Utilisateur : root

* Mot de passe : (laisser vide par défaut)

* Choix du serveur : MySql
```

<br>

## ⌨️ Quelques commandes SQL essentielles :
| Commande | Description |
|----------|------------|
| SELECT | Récupère les données d'une table |
| INSERT INTO | Ajoute de nouvelles données |
| UPDATE | Met à jour des données existantes |
| DELETE | Supprime des données |
<br>

## Comment créer sa base de données ?
<br>

* création via l'interface graphique
* création manuelle


Exemple d'une création manuelle :

1. Aller dans l'onglet SQL

2. Entrer la requête :

```bash
    CREATE DATABASE nom_de_la_base
    DEFAULT CHARACTER SET utf8
    DEFAULT COLLATE utf8_general_ci;

```

3. Exécuter
<br><br>

## Comment créer une table ?
<br>

1. Aller dans SQL
2. Entrer la requête : 

```bash
    CREATE TABLE nom_de_la_table (

    (+ rajouter le nombre de colonne souhaité)
    
id INT PRIMARY KEY AUTO_INCREMENT NOT NULL,                    ==> PRIMARY KEY    === Clé unique 
label VARCHAR(255) NOT NULL                                    ==> AUTO_INCREMENT === Ajout automatiquement un id '1,2,3' à chaque nouvelle
title VARCHAR(255) NOT NULL,                                                          ligne
first_name VARCHAR(255) NOT NULL,                              ==> NOT NULL       === Ne peut pas être vide
last_name VARCHAR(255) NOT NULL,
duration INT NULL,
lauch_at DATE NULL,
birth_at DATE NULL,
description TEXT NULL

)ENGINE=INNODB;
```

3. Dans l'onglet >Plus dérouler le Concepteur.

Le concepteur permet de visualiser et de modifier les relations entre les tables de la base de données de manière intuitive et graphique.
Il offre une vue d'ensemble des structures de tables et de leurs connexions, facilitant ainsi la gestion et l'optimisation des bases de données.



Exemples pratiques de requêtes SQL 📊

🔹 Sélectionner toutes les données d’une table

```bash
    SELECT * FROM utilisateurs;
```
<br>

🔹 Insérer un nouvel utilisateur

```bash
    INSERT INTO utilisateurs (nom, email) VALUES ('Alice', 'alice@example.com');
```
<br>

🔹 Modifier la structure d’une table avec ALTER TABLE

```bash
ALTER TABLE `nom_de_la_table`  
ADD COLUMN address_id INT NOT NULL,
ADD FOREIGN KEY fk_order_address (address_id) REFERENCES address(id);
```
<br>

🔹 Mettre à jour une donnée
```bash
    UPDATE utilisateurs SET email = 'nouveau@example.com' WHERE nom = 'Alice';
```
<br>

🔹 Supprimer un utilisateur

```bash
    DELETE FROM utilisateurs WHERE nom = 'Alice';
```
<br><br><br>


## Comment manipuler la requête SELECT ?
<br>
* Syntaxe de Base
La syntaxe de base d'une requête SELECT est la suivante :
<br>
```bash
    SQL
    SELECT colonne1, colonne2, ...
    FROM table
    WHERE condition;
```

<br>

Exemples pratiques de requêtes SQL 📊
<br>
🔹 Sélectionner toutes les données d’une table

```bash
    SELECT * FROM utilisateurs;
```
<br>

🔹 Sélectionner des colonnes spécifiques

```bash
    SELECT nom, email FROM utilisateurs;
```
<br>

🔹 Filtrer les résultats avec WHERE
```bash
    SELECT * FROM utilisateurs WHERE nom = 'Alice';
```
<br>

🔹 Trier les résultats avec ORDER BY

```bash
    SELECT * FROM utilisateurs ORDER BY nom ASC;
```
<br>
🔹 Limiter le nombre de résultats

```bash
    SELECT * FROM utilisateurs LIMIT 5;
```
<br>

🔹 Compter le nombre d’utilisateurs

```bash
    SELECT COUNT() FROM utilisateurs;
```
<br>

🔹 Calculer la moyenne d’une colonne

```bash
    SELECT AVG(age) FROM utilisateurs;
```
<br>
🔹 Trouver la valeur minimale et maximale d’une colonne

```bash
    SELECT MIN(age) FROM utilisateurs;
    SELECT MAX(age) FROM utilisateurs;
```
<br>
🔹 Filtrer avec LIKE

```bash
    SELECT FROM utilisateurs WHERE nom LIKE 'A%';
```
<br>

🔹 Utilisation de OR et AND

```bash
    SELECT * FROM utilisateurs WHERE nom = 'Alice' OR nom = 'Bob';
    SELECT * FROM utilisateurs WHERE nom = 'Alice' AND email LIKE '%@gmail.com';
```
<br>

🔹 Regrouper les résultats avec GROUP BY

```bash
    SELECT email, COUNT() FROM utilisateurs GROUP BY email;
```
<br>
🔹 Filtrer des groupes avec HAVING

```bash
    SELECT email, COUNT() FROM utilisateurs GROUP BY email HAVING COUNT(*) > 1;
```
<br>
🔹 Utiliser INNER JOIN pour lier des tables

```bash
    SELECT utilisateurs.nom, commandes.produit FROM utilisateurs
    INNER JOIN commandes ON utilisateurs.id = commandes.utilisateur_id;
```
<br>
🔹 Concatenation de colonnes avec CONCAT

```bash
    SELECT CONCAT(nom, ' ', email) AS nom_email FROM utilisateurs;
```
<br>

🔹 Insérer un nouvel utilisateur

```bash
    INSERT INTO utilisateurs (nom, email) VALUES ('Alice', 'alice@example.com');
```
<br>

🔹 Mettre à jour une donnée

```bash
    UPDATE utilisateurs SET email = 'nouveau@example.com' WHERE nom = 'Alice';
```
<br>

🔹 Supprimer un utilisateur
```bash
    DELETE FROM utilisateurs WHERE nom = 'Alice';
```


