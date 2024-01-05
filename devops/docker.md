# Docker

## 🎓 J'ai compris et je peux expliquer

La création d'une image Docker (✔️):
La création d'une image Docker se fait généralement à l'aide d'un fichier nommé Dockerfile. Ce fichier contient une série d'instructions qui indiquent comment construire l'image.
Pour créer une image, on utilise la commande docker build. Cette commande lit le Dockerfile, exécute les instructions qu'il contient, et crée une image Docker pouvant être utilisée pour lancer des conteneurs.

L'exécution d'un container (✔️):
L'exécution d'un container se fait à l'aide de la commande docker run. Cette commande prend une image Docker (que vous avez créée ou téléchargée depuis un registre d'images comme Docker Hub) et crée un conteneur à partir de cette image.
Le conteneur est une instance en cours d'exécution de l'image, isolée avec ses propres processus, réseau, et ensemble de ressources système.

L'orchestration de containers avec Docker Compose (✔️):
Docker Compose est un outil pour définir et gérer des applications multi-conteneurs avec Docker.
On utilise un fichier YAML pour configurer les services de l'application. Ce fichier, généralement nommé docker-compose.yml, définit les images à utiliser, les ports à ouvrir, les volumes à partager, et d'autres paramètres.
Ensuite, on utilise la commande docker-compose up pour lancer l'application avec tous ses services associés. Cela permet de démarrer et de relier plusieurs conteneurs de manière cohérente et facile à gérer.

## 💻 J'utilise

### Un exemple personnel commenté / ✔️

Dockerfile
FROM node:21-alpine3.17

WORKDIR /app

COPY package\*.json ./

COPY . .

RUN npm install

EXPOSE 3021

CMD ["npm", "run", "dev"]

docker-compose.yml

version: "3.8"

services:
back-padawan:
build: ./
depends_on: - db-padawan
volumes: - ./:/app
environment:
PORT: 3021
POSTGRES_USER: postgres
POSTGRES_HOST: db-padawan
POSTGRES_DB: db-padawan
POSTGRES_PASSWORD: padawan-backend
POSTGRES_PORT: 5432
ports: - 3021:3021
networks: - cpm-padawan-network

db-padawan:
image: postgres:latest
restart: always
environment:
POSTGRES_USER: postgres
POSTGRES_DB: db-padawan
POSTGRES_PASSWORD: padawan-backend
POSTGRES_PORT: 5432
ports: - "5432:5432"
networks: - cpm-padawan-network
volumes: - data:/var/lib/postgresql/data

networks:
cpm-padawan-network:
volumes:
data: {}

Ici mon Dockerfile qui donne les commandes a executer pour cette image personnalise qui est mon projet padawan-back>

Puis le docker-compose qui agit comme un chef d'orchestre pour les differentes images, ici mon image et une image officiel de postgres.

### Utilisation dans un projet / ✔️

https://github.com/Interencheres/cpm-padawan-fullstack2/tree/main

Description : Projet realise lors de mon alternance pour ameliorer mon niveau en back

### Utilisation en production si applicable / ✔️

https://github.com/Interencheres/indb-atlas-front

Description : Projet front cote client de mon alternance en vueJS

### Utilisation en environement professionnel / ✔️

Description : utilisation dans l'integralite de nos projets, nous tournons a environ 15 projets en simultanee qui tournent sur Docker-compose et une surcouche realisee par les dev ops.

Chacun des projets se lance en fonction du projet principal que l'on lance, il n'y a qu'une commande a lancer pour que l'intgralite des projets se lancent en simultannee.

## 🌐 J'utilise des ressources

### Titre

-  https://www.youtube.com/results?search_query=docker+cours
   https://www.youtube.com/watch?v=SXB6KJ4u5vg&list=PL8SZiccjllt1jz9DsD4MPYbbiGOR_FYHu&ab_channel=cocadmin
-  Cours docker sur youtube pour debuter avec cette techno, bien explique et simple. Permet de mettre en place rapidement un container rapidement

## 🚧 Je franchis les obstacles

### Point de blocage / ✔️

Description: Encore le Dockerfile que j'ai du mal a comprendre

Plan d'action : (à valider par le formateur)

-  action 1 / ✔️ Refaire un projet meme hypothetique pour mettre en place un back et un front avec docker
-  action 2 / ✔️
-  ...

Résolution :

## 📽️ J'en fais la démonstration

-  J'ai ecrit un [tutoriel](...) ❌ / ✔️
-  J'ai fait une [présentation](...) ❌ / ✔️
