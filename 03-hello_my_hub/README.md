🐳 # Publie ton Image sur Docker Hub

Tu vois l'image que tu as faite dans l'exo 2 ? Maintenant, il faut la publier sur le hub, et je ne veux pas entendre : 'Monsieur, je n'y arrive pas.' Ça prend trois minutes sur Google pour trouver la réponse.

Commande :
docker build -t dealexandra/exo-02 .
docker run -d -p 8002:80 --name exo-02-container dealexandra/exo-02
docker push dealexandra/exo-02

Lien : https://hub.docker.com/repository/docker/dealexandra/exo-02/general
