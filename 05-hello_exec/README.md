# Atelier PostgreSQL avec Docker 🐳

Bienvenue ! Tu vas découvrir comment lancer une instance PostgreSQL dans un conteneur Docker.

## Objectif 🎯

Ton objectif aujourd'hui est simple:

1. Préparer un `Dockerfile`.
2. Lancer un conteneur PostgreSQL.
3. Te connecter à ce conteneur en mode interactif.
4. Trouver par tes propres moyens le nombre de personnes de plus de 30 ans grâce à `psql`.

## Étape 1 : Préparons le `Dockerfile` 🛠️

Commence par créer un fichier nommé `Dockerfile`. Tu vas devoir y définir les paramètres nécessaires pour construire ton image PostgreSQL.

## Étape 2 : Construisons et lançons notre conteneur 🚢

Maintenant que ton `Dockerfile` est prêt, il est temps de le transformer en une image Docker

## Étape 3 : Connectons-nous à PostgreSQL 🖥️

Une fois le conteneur en marche, tu devras t'y connecter. Utilise `docker exec` pour démarrer une session interactive avec `psql`. N'oublie pas la doc ^^

## Étape 4 : À toi de jouer avec SQL 🔍

Te voilà à l'intérieur de la base de données. C'est le moment de tester tes connaissances en SQL.

Trouver le nombre de personnes de plus de 30 ans.

```
PS : merci d'utiliser ton cerveau et non ChatGPT.
```

Commande :
docker build -t exo-05 .
docker run -d -p 5433:5432 --name exo-05-container exo-05
docker logs exo-05-container

Pour rentrer dans le bash :
docker exec -it exo-05-container bash
psql -U postgres

postgres=# Select count(\*) from personnes where age > 30;

Ressources :
https://docs.docker.com/engine/reference/commandline/exec/
https://www.commandprompt.com/education/how-to-useexecute-postgresql-query-in-docker-container/

Note :

- create bridge : docker network create exo06
- docker network ls
- docker network connect exo06 exo-05-container
