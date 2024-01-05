# Sécurité dans le développement Web

## 🎓 J'ai compris et je peux expliquer

Le rôle de l'OWASP (✔️):

L'OWASP (Open Web Application Security Project) est une organisation à but non lucratif qui travaille à améliorer la sécurité des logiciels.
Son rôle principal est de fournir des conseils, des ressources, des outils, et des formations pour aider les organisations à identifier et à corriger les failles de sécurité dans leurs applications web.
L'un des outils les plus connus de l'OWASP est le Top 10, une liste des dix vulnérabilités de sécurité les plus critiques dans les applications web.

Les injections SQL (✔️):

Les injections SQL sont un type d'attaque de sécurité dans lequel un attaquant insère ou "injecte" une requête SQL malveillante via l'interface d'entrée de l'application, en exploitant une vulnérabilité dans le logiciel.
Cette technique peut permettre à l'attaquant de lire, modifier, ou supprimer des données dans la base de données sous-jacente, compromettant ainsi la sécurité de l'application.
Prévenir les injections SQL implique de valider et de nettoyer correctement toutes les entrées utilisateur et d'utiliser des requêtes paramétrées.

XSS (Cross-Site Scripting) (✔️):

Le XSS est une vulnérabilité qui permet à un attaquant d'injecter du code JavaScript malveillant dans les pages web vues par d'autres utilisateurs.
Ce type d'attaque peut être utilisé pour voler des informations, comme des cookies de session, ou pour modifier l'apparence du site web pour l'utilisateur affecté.
La prévention du XSS passe par l'échappement des entrées utilisateur et l'utilisation de politiques de sécurité du contenu (CSP).

CSRF (Cross-Site Request Forgery) (✔️):

Le CSRF est une attaque qui force un utilisateur connecté à envoyer des requêtes non désirées à une application web sur laquelle il est déjà authentifié.
Ces attaques exploitent la confiance qu'une application a dans l'identité de l'utilisateur.
Pour se protéger contre le CSRF, on utilise souvent des jetons anti-CSRF dans les formulaires, qui assurent que chaque requête soumise provient bien du site web lui-même et non d'un site tiers.

## 💻 J'utilise

### Un exemple personnel commenté / ✔️

tirer de la quete sur odyssey pour une injection sql

Maintenant que nous avons cette information nous pouvons détourner la requête pour afficher plus d'informations que prévues par l'application.

Fais en sorte de faire effectuer cette requête à l'application:

SELECT name,id FROM Users WHERE login='' union select password, null from Users where login="..."#'
Remplace... par un login que tu as créé.

Il faut saisir ' union select password, null from Users where login="..."#' dans le champ login.

Le mot clé union permet d'effectuer une seconde requête accédant à une information normalement non accessible.

On ajoute null pour obtenir le même nombre de champs à notre résultat de requête afin de ne pas provoquer d'erreur serveur.

### Utilisation dans un projet ❌ / ✔️

[lien github](...)

Description :

### Utilisation en production si applicable❌ / ✔️

[lien du projet](...)

Description :

### Utilisation en environement professionnel ❌ / ✔️

Description :

## 🌐 J'utilise des ressources

### Titre

-  lien
-  description

## 🚧 Je franchis les obstacles

### Point de blocage ❌ / ✔️

Description:

Plan d'action : (à valider par le formateur)

-  action 1 ❌ / ✔️
-  action 2 ❌ / ✔️
-  ...

Résolution :

## 📽️ J'en fais la démonstration

-  J'ai ecrit un [tutoriel](...) ❌ / ✔️
-  J'ai fait une [présentation](...) ❌ / ✔️
