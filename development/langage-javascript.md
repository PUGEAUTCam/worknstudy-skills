# Langage Javascript

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

-  les `structures` de base du langage / ✔️
   Les structures de base du langage se réfèrent aux éléments fondamentaux qui permettent de créer des programmes. Elles incluent des éléments tels que les variables, les types de données (comme les nombres et les chaînes de caractères), les opérateurs (comme l'addition et la soustraction), les conditions (comme les déclarations "if" et "else"), les boucles (comme les boucles "for" et "while"), et les fonctions. Ces structures de base constituent les briques de construction essentielles pour écrire des programmes dans un langage donné.
-  les normes `ecmascript` / ✔️
   ECMAScript est une norme qui spécifie les caractéristiques et le comportement du langage de programmation JavaScript. Cette norme est développée par l'organisation ECMA International. Les différentes versions d'ECMAScript définissent les nouvelles fonctionnalités, les améliorations et les modifications apportées à JavaScript. Les normes ECMAScript, telles que ECMAScript 5 (ES5), ECMAScript 6 (ES6) et ainsi de suite, fournissent des spécifications sur la syntaxe, les types de données, les objets intégrés, les fonctions et bien d'autres aspects du langage JavaScript.
-  l'utilisation de l'`asynchrone` / ✔️
   'asynchronisme est un concept important en programmation qui permet d'exécuter des tâches de manière non bloquante. Plutôt que d'attendre qu'une tâche se termine avant de passer à la suivante, l'asynchronisme permet d'initier plusieurs tâches en parallèle et de traiter leurs résultats lorsque disponibles. En JavaScript, cela est généralement réalisé à l'aide de fonctions asynchrones et de la gestion des promesses (promises), ou avec les mots-clés async/await introduits dans les versions plus récentes d'ECMAScript. Cette approche est particulièrement utile pour effectuer des opérations réseau, des appels à des API externes ou des traitements intensifs qui pourraient bloquer l'exécution du programme de manière synchrone.
-  les spécifités du mot-clef `this` / ✔️
   En JavaScript, le mot-clé "this" est utilisé pour faire référence à l'objet courant dans le contexte d'exécution. Sa valeur dépend de la façon dont une fonction est appelée. "this" peut faire référence à l'objet global (l'objet "window" dans un navigateur), à l'objet dans lequel la fonction est définie (dans le cas d'une méthode d'objet), à l'objet nouvellement créé (lorsqu'une fonction est utilisée en tant que constructeur), ou à un objet spécifique lorsqu'il est utilisé avec les appels de méthode explicites (par exemple, "obj.method()"). La valeur de "this" est résolue dynamiquement au moment de l'exécution, ce qui signifie qu'elle peut varier en fonction du contexte d'appel de la fonction.

## 💻 Je code en Javascript

### Un exemple de code commenté / ✔️

```javascript
// Déclaration fonction qui prend en entrée un tableau de nombres et renvoie la somme de tous les éléments du tableau.
const array = [1, 2, 3, 4, 5]

const sum = (array) => {
   return array.reduce((sum, currentValue) => sum + currentValue) // Ici la fonction reduce permet d'additionner dans sum chaque valeur du tableau qui passe dans Current Value
}
console.log(sum(array)) // J'appelle ma fonction et je console.log pour voir le resultat dans mon terminal
//deuxieme option
let sum = 0

const sumCount = (array) => {
   for (let i = 0; i < array.length; i++) {
      sum += array[i]
   }
   return sum
}
console.log(sumCount(array)) // Fonction qui donne le meme resultat mais ici je passe par une boucle for pour passer sur chaque nombre de mon tableau, que je rajoute a sum qui est une variable initialise a 0 au depart. A chaque tour de boucle, se rejoute a 0 le nombre du tableau. Puis je n'oublie pas de retourner le resultat
```

### Utilisation dans un projet / ✔️

https://github.com/PUGEAUTCam/DW_P5_V2_PUGEAUT_Camille

Description : Implementation du front end en javascript natif d'un site e-commerce pour un magasin de vente de canapes.
Utilisateur de fetch, fonction, locale storage et params.

### J'ai utilisé ce langage en production / ✔️

https://github.com/PUGEAUTCam/DW_P5_V2_PUGEAUT_Camille

Description : Implementation du front end en javascript natif d'un site e-commerce pour un magasin de vente de canapes.
Utilisateur de fetch, fonction, locale storage et params.

https://github.com/Interencheres

Description : Mon projet en entreprise

### J'ai utilisé ce langage en environement professionnel / ✔️

Description : J'utilise au sein de mon entreprise le framework javascript VueJS, du cote front end.

## 🌐 J'utilise des ressources

### Titre

https://developer.mozilla.org/fr/
La base. Documentation officiel pour le javascript avec des exemples.
Documentation complète : Mozilla Developer Network (MDN) offre une documentation complète et détaillée sur de nombreux sujets liés au développement web. Vous y trouverez des informations sur les langages de programmation, les API, les outils, les techniques de développement, etc. Cette documentation est maintenue par une communauté active de contributeurs et est régulièrement mise à jour pour refléter les dernières spécifications et pratiques recommandées.
Exemples de code : MDN propose de nombreux exemples de code qui illustrent l'utilisation des différentes fonctionnalités et API. Ces exemples sont souvent accompagnés d'explications détaillées, ce qui facilite la compréhension et l'apprentissage.

## 🚧 Je franchis les obstacles

### Point de blocage / ✔️

Description: Les algorithmes que je n'ai pas eu la chance de travailler et qu'on ne travaille pas non plus au cours de cette alternance.

Plan d'action : (à valider par le formateur)

-  action 1 / ✔️ Faire des algorithmes chaque semaine, y consacrer un peu de temps.
-  action 2 / ✔️ Le prendre comme un jeu.
-  ...

Résolution :

## 📽️ J'en fais la démonstration

Titre: Analyse des Scores d’un Tournoi avec Bonus et Classement

Description:
Vous allez créer un programme en JavaScript qui simule l'analyse des scores d'un tournoi de jeux vidéo. Les participants obtiennent des points en fonction de leur performance, et vous devez calculer et afficher diverses statistiques, y compris des points bonus et un classement.

Consignes:

1. Créez un tableau `scores` contenant des objets. Chaque objet représente un participant et contient trois propriétés : `nom` (string), `points` (number), et `bonus` (un tableau de numbers). Par exemple:

   ```javascript
   let scores = [
      { nom: "Alice", points: 87, bonus: [5, 10] },
      { nom: "Bob", points: 92, bonus: [3, 3, 3] },
      { nom: "Charlie", points: 85, bonus: [10] },
      { nom: "Diana", points: 95, bonus: [5, 5, 5] },
   ]
   ```

2. Créez une fonction `calculerMoyenne(scores)` qui prend en entrée le tableau de scores et renvoie la moyenne des points.

3. Créez une fonction `trouverGagnant(scores)` qui prend en entrée le tableau de scores et renvoie le nom du participant qui a le plus de points.

4. Créez une fonction `filtrerParSeuil(scores, seuil)` qui prend en entrée le tableau de scores et un seuil de points, et renvoie un nouveau tableau contenant seulement les participants dont les points sont supérieurs ou égaux au seuil donné.

5. Créez une fonction `appliquerBonus(scores)` qui prend en entrée le tableau de scores et met à jour les points de chaque joueur en ajoutant la somme de leurs points bonus à leurs points initiaux.

6. Créez une fonction `classerJoueurs(scores)` qui prend en entrée le tableau de scores et renvoie un nouveau tableau avec les joueurs triés par leur score total (points + bonus) en ordre décroissant.

7. Dans le programme principal (hors des fonctions), utilisez les fonctions ci-dessus pour afficher les résultats suivants dans le terminal :
   -  La moyenne des points sans bonus.
   -  Le nom du gagnant sans prendre en compte les points bonus.
   -  Une liste des participants qui ont obtenu 90 points ou plus sans prendre en compte les points bonus.
   -  Appliquez les points bonus.
   -  Affichez la liste des joueurs classés par leur score total (points + bonus).

Exemple de sortie attendue dans le terminal :

```
Moyenne des points sans bonus: 89.75
Le gagnant sans bonus est: Diana
Participants avec 90 points ou plus sans bonus: Bob, Diana
Liste des joueurs classés par score total (points + bonus) :
1. Diana - 110 points
2. Alice - 102 points
3. Bob - 101 points
4. Charlie - 95 points
```

Conseils :

-  Vous pouvez utiliser les méthodes `forEach`, `filter`, `reduce`, et `sort` sur les tableaux pour aider dans les calculs.

Objectifs d'apprentissage :

-  Manipulation de tableaux et d'objets en JavaScript.
-  Utilisation de fonctions pour structurer le code.
-  Calculs basiques et logique de filtrage.
-  Manipulation de tableaux imbriqués.
-  Tri d'un tableau d'objets basé sur une propriété spécifique.

Ma reponse (fait en une grosse apres midi)

let scores = [
{ name: "Alice", points: 98, bonus: [5, 10] },
{ name: "Bob", points: 92, bonus: [3, 3, 3] },
{ name: "Charlie", points: 85, bonus: [10] },
{ name: "Diana", points: 99, bonus: [5, 5, 5] },
]
const calculateMoyenne = () => {
const totalPoints = scores.reduce((acc, score) => acc + score.points, 0)
return `Moyenne des points sans bonus : ${totalPoints / scores.length}`
}
console.log(calculateMoyenne())

const findWinner = (scores) => {
const winner = scores.reduce((acc, score) => {
return acc.points > score.points ? acc : score
})
return `Le gagnant sans bonus est ${winner.name}`
}
console.log(findWinner(scores))

const filteredByLimit = (scores, limit) => {
let filteredPlayersByLimit = scores.filter((score) => score.points >= limit)
let participantNames = filteredPlayersByLimit.map((player) => player.name)

return `Participants avec ${limit} points ou plus sans bonus: ${participantNames.join(
      ", "
   )}`
}
console.log(filteredByLimit(scores, 90))

const applyBonus = (scores) => {
let finalArray = []
for (let i = 0; i < scores.length; i++) {
let bonus = scores[i].bonus.reduce((acc, bonus) => acc + bonus)
let finalScoreWithBonus = bonus + scores[i].points

      finalArray.push({
         name: scores[i].name,
         finalScore: finalScoreWithBonus,
      })

}
return finalArray
}
// console.log(applyBonus(scores))

const playersClassement = (scores) => {
let finalArray = applyBonus(scores)
.sort((a, b) => b.finalScore - a.finalScore)
.map(
(player, index) =>
`\n ${index + 1}. ${player.name} - ${player.finalScore} points`
)

return `Liste des joueurs classés par score total (points + bonus) : ${finalArray}`
}
console.log(playersClassement(scores))
