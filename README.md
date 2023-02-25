# Containers_communication
Dans ce projet j'ai effectué une communication entre trois docker containers:


- le premier contient l'image de l'application 1 qui a pour but de passer les informations d'un formulaire vers l'application2 avec la methode "post" sachant bien que les deux application sont dans deux different project et deux different ports.


- Le deuxième container contient l'image d'app2, son objectif est de recevoir les donnes envoyer par l'app1 anis que se connecter avec la DB mongo avec l'URL "mongodb://mongocontainer:27017/mydatabase" et comme vous remarquer ce n'est pas localhost .


- Le troisième container contient une image de mongo






********** pour la communication entre ces trois containers, j'ai créé  un network par la commande :"docker network create my-network


Chaque fois, j'exécute un des containers, je mentionne dans la commande le network que j'ai créé.


Par exemple pour le container 3 : docker run --name mongocontainer --network mynetwork -p 27018:27017 -d mongo:latest mongod


Pour pouvoir visionner ma base de donne du terminal de docker, j'ai installé "MongoDB Shell"
