# Titre de la compétence

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

-  Comment développer en utilisant un système de _livereloading_ (`nodemon` par exemple) / ✔️
   Avoir node d'installer puis installer nodemon avec npm i nodemon.
   Ensuite inscrire dans package.json pour start : nodemon
   Uitlite : permet de détecter les modifications apportées à votre code pendant le développement et de recharger automatiquement l'application pour afficher les changements en temps réel. Nodemon est un outil populaire qui surveille les fichiers de votre projet et redémarre automatiquement l'application lorsque des modifications sont détectées. Cela vous évite de devoir redémarrer manuellement l'application à chaque fois que vous apportez des modifications.
-  La connexion de mon application à une base de données avec et sans ORM/ODM (avec `mongodb` puis `mongoose` par exemple) / ✔️
   Pour connecter votre application à une base de données, vous pouvez utiliser une bibliothèque ou un ORM/ODM (Object-Relational Mapping/Object-Document Mapping) pour faciliter l'interaction avec la base de données. Par exemple, si vous utilisez MongoDB comme base de données, vous pouvez utiliser la bibliothèque mongodb pour une connexion directe sans ORM/ODM, ou vous pouvez utiliser mongoose qui est un ODM populaire pour MongoDB. Mongoose facilite la création de schémas, de modèles et fournit des méthodes et des fonctionnalités supplémentaires pour interagir avec la base de données.
-  Le développement d'une API REST et GraphQL (avec les packages `express` et `graphql` par exemple) / ✔️
   Lors du développement d'une API, vous pouvez choisir entre une architecture REST ou GraphQL pour définir et gérer les endpoints de votre application. Pour une API REST, vous pouvez utiliser le package express, qui est un framework web populaire pour Node.js, pour créer vos routes, gérer les requêtes HTTP et envoyer les réponses appropriées. Pour une API GraphQL, vous pouvez utiliser le package graphql qui permet de définir un schéma, des types de données et de résoudre les requêtes GraphQL. Vous pouvez combiner express avec graphql pour créer une API GraphQL en utilisant les fonctionnalités de routage et de gestion des requêtes d'Express.
-  _Bonus : la manipulation des fichiers système avec `fs` et l'utilisation des streams en NodeJS_ / ✔️
   Le module fs (file system) de Node.js permet de manipuler les fichiers système, y compris la lecture, l'écriture, la suppression et la gestion des répertoires. Vous pouvez utiliser les différentes méthodes fournies par fs pour effectuer des opérations sur les fichiers, comme fs.readFile() pour lire un fichier ou fs.writeFile() pour écrire dans un fichier. L

## 💻 J'utilise

### Un exemple personnel commenté / ✔️

```javascript
// Fonction qui  permet d'update le profil d'un utilisateur
exports.profileUpdate = (req, res, next) => {
   const userInfo = req.body // Je recup le corps de ma requete dans une variable userIfo
   let userId = req.auth.userId // Ici l'id

   UserModel.updateOne({ _id: userId }, userInfo) // Je recupere ici dans mon userModel de ma BDD le bon user grace a l'id puis je lui donne les nouvelles infos a mettre a jour avec userInfo
      .then(() => res.status(200).json({ message: "Profil mis a jour" })) // J'envoie une reponse 200 si c;est ok avec un petit msg
      .catch((error) => res.status(400).json({ error })) // 400 erreur
}
```

### Utilisation dans un projet / ✔️

https://github.com/PUGEAUTCam/DW_P7_V2_PUGEAUT_Camille/tree/main

Description : This is the front end and back end server for Project 7 of the Web Developer path OpenCLassrooms in november 2022.

Technologies used
Front-end : React, axios, redux toolkit, dayjs, infiniteScrool and styled components.
Back-end : NodeJS, Express and for the database MongoDB with this framework Mongoose.
Mon gros projet de fin de formation chew Open CLassroom, creation d'un reseau social avec diverses fonctionnalites. Realisation du front et du back. Projet de 4 mois.

### Utilisation en production si applicable / ✔️

https://github.com/Interencheres

Description : Mon projet en entreprise qui utilise NodeJS en back

### Utilisation en environement professionnel / ✔️

Description : Mon entreprise utilise NodJS en back mais je ne fais pas de back. Je suis alternante en front.

## 🌐 J'utilise des ressources

### Titre

https://www.youtube.com/watch?v=TlB_eWDSMt4&ab_channel=ProgrammingwithMosh
Video rapide d'1h pour debuter NodeJs ou revoir des bases.
https://www.youtube.com/watch?v=NRxzvpdduvQ&t=4326s&ab_channel=SimonDieny-ReconversionFullstackJavaScript
Tutoriel de 8h pour realiser un projet.

https://nodejs.org/en/docs
Docuementation offciel de Node JS

https://stackoverflow.com/
Communaute entraide

## 🚧 Je franchis les obstacles

### Point de blocage ❌ / ✔️

Description: Je pratique peu le NodeJs depuis la fin de ma formation de 6 mois.

Plan d'action : (à valider par le formateur)

-  action 1 ❌ / ✔️ Realiser des cours ou petits projets

Résolution :

## 📽️ J'en fais la démonstration

-  J'ai ecrit un [tutoriel](...) ❌ / ✔️
-  J'ai fait une [présentation](...) ❌ / ✔️
