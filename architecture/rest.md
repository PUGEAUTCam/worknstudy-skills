# REST API

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

-  les verbes HTTP / ✔️
   Les verbes HTTP sont utilisés pour indiquer l'action à effectuer sur une ressource lors d'une requête HTTP. Les verbes les plus couramment utilisés sont :
   GET : récupère une ressource.
   POST : crée une nouvelle ressource.
   PUT : met à jour une ressource existante.
   DELETE : supprime une ressource.
   PATCH : effectue une mise à jour partielle d'une ressource.
-  les statuts HTTP / ✔️
   Les statuts HTTP sont des codes numériques renvoyés par le serveur pour indiquer le résultat d'une requête HTTP. Ils fournissent des informations sur le succès, l'échec ou l'état de la requête. Quelques exemples de statuts HTTP courants sont :
   200 OK : la requête a réussi.
   404 Not Found : la ressource demandée n'a pas été trouvée.
   500 Internal Server Error : une erreur interne s'est produite du côté du serveur.
-  les endpoints / ✔️
   Les endpoints sont des points d'accès spécifiques sur un serveur ou une API qui permettent d'interagir avec des ressources. Chaque endpoint est associé à une URL unique et est généralement utilisé pour effectuer des opérations spécifiques sur une ressource, comme obtenir, créer, mettre à jour ou supprimer des données.
-  CORS / ✔️
   CORS (Cross-Origin Resource Sharing) est un mécanisme de sécurité qui contrôle les requêtes HTTP effectuées entre des domaines différents. Il permet aux ressources d'une page web d'être chargées à partir d'un domaine différent de celui de la page elle-même. CORS est une mesure de sécurité pour protéger les utilisateurs contre les attaques potentielles de scripts malveillants.
-  la nomenclature recommandée pour les routes / ✔️
   La nomenclature recommandée pour les routes, également connue sous le nom de convention de dénomination des endpoints, est une pratique courante pour nommer de manière cohérente les endpoints d'une API. Elle permet une meilleure compréhension et une plus grande facilité de maintenance. Quelques recommandations courantes incluent l'utilisation de noms de ressources pluriels, l'utilisation de verbes dans les noms d'endpoint pour indiquer l'action, et l'utilisation de paramètres pour identifier des ressources spécifiques.

## 💻 J'utilise

### Un exemple personnel commenté / ✔️

Exemple de routes pour un users en back end pour un projet de reseau social
//Import Controllers
const userCtrl = require('../controllers/user');
const multer = require('../middlewares/multer-config');
const auth = require('../middlewares/auth');

// CRUD
router.post('/signup', passwordValidator, userCtrl.signup);
router.post('/login', userCtrl.login);
router.get('/me', auth, userCtrl.me);
router.get('/:id', userCtrl.getOneUser);

router.patch('/profileUpdate', auth, userCtrl.profileUpdate);
router.post("/uploadCoverImg", multer, auth, userCtrl.uploadCoverImg);
router.post("/uploadAvatarImg", multer, auth, userCtrl.uploadAvatarImg);

### Utilisation dans un projet / ✔️

https://github.com/PUGEAUTCam/DW_P7_V2_PUGEAUT_Camille/tree/main

Description : This is the front end and back end server for Project 7 of the Web Developer path OpenCLassrooms in november 2022.

Technologies used
Front-end : React, axios, redux toolkit, dayjs, infiniteScrool and styled components.
Back-end : NodeJS, Express and for the database MongoDB with this framework Mongoose.
Mon gros projet de fin de formation chew Open CLassroom, creation d'un reseau social avec diverses fonctionnalites. Realisation du front et du back. Projet de 4 mois.

### Utilisation en production si applicable/ ✔️

https://github.com/PUGEAUTCam/DW_P7_V2_PUGEAUT_Camille/tree/main

Description : This is the front end and back end server for Project 7 of the Web Developer path OpenCLassrooms in november 2022.

Technologies used
Front-end : React, axios, redux toolkit, dayjs, infiniteScrool and styled components.
Back-end : NodeJS, Express and for the database MongoDB with this framework Mongoose.
Mon gros projet de fin de formation chew Open CLassroom, creation d'un reseau social avec diverses fonctionnalites. Realisation du front et du back. Projet de 4 mois.
Mis en ligne pour quelaues semaines pour les entretiens techniques avant l'alternance

### Utilisation en environement professionnel / ✔️

https://github.com/Interencheres

Description : Mon projet en entreprise qui utilise NodeJS en back

## 🌐 J'utilise des ressources

### Titre

https://www.youtube.com/watch?v=SC4sEiBje1Q&ab_channel=Kodaps-apprendre%C3%A0coder
Pour definir

## 🚧 Je franchis les obstacles

### Point de blocage / ✔️

Description: Parfois du mal a manipuler les token, autorisations

Plan d'action : (à valider par le formateur)

-  action 1 ❌ / ✔️
-  action 2 ❌ / ✔️
-  ...

Résolution :

## 📽️ J'en fais la démonstration

-  J'ai ecrit un [tutoriel](...) ❌ / ✔️
-  J'ai fait une [présentation](...) ❌ / ✔️
