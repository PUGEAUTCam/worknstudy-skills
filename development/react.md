# Titre de la compétence

## 🎓 J'ai compris et je peux expliquer

-  l'état (_state_) pour contrôler l'affichage d'un composant / ✔️
   L'état (state) est un concept fondamental dans la programmation de composants. Il représente les données internes à un composant qui peuvent être modifiées au fil du temps. En utilisant l'état, on peut contrôler l'affichage d'un composant en réagissant aux changements de cet état. Lorsque l'état change, le composant se met à jour et peut rendre une nouvelle interface utilisateur en conséquence.
-  les composants enfants et les _props_ qu'on leur passe / ✔️
   Les composants enfants sont des composants imbriqués à l'intérieur d'un autre composant. Les props (propriétés) sont utilisées pour passer des données d'un composant parent à ses composants enfants. Les props permettent de configurer et de personnaliser les composants enfants en leur fournissant des valeurs ou des fonctions spécifiques via des paramètres.
-  le déclenchement d'instructions en fonction des actions de l'utilisateur / ✔️
   Dans une application interactive, il est courant de déclencher des instructions en fonction des actions de l'utilisateur, telles que des clics de souris, des saisies clavier, des soumissions de formulaires, etc. En écoutant les événements associés à ces actions, on peut exécuter du code spécifique en réponse à ces événements, par exemple mettre à jour l'état du composant ou effectuer des appels à des API externes.
-  le déclenchement d'instructions en fonction de l'étape du cycle de vie du composant ou du changement de valeur de ses props / ✔️
   Les composants ont un cycle de vie qui se compose de différentes étapes, comme leur création, leur mise à jour et leur destruction. À chaque étape du cycle de vie, il est possible de déclencher des instructions spécifiques en utilisant des méthodes de cycle de vie appropriées. De plus, lorsque les props d'un composant changent, on peut réagir à ces changements en exécutant du code spécifique pour mettre à jour l'affichage ou effectuer d'autres actions nécessaires.
-  l'usage d'un reducer (_useReducer_) pour gérer un état composé dans un composant
   Le reducer (useReducer) est un hook de gestion de l'état dans React. Il permet de gérer un état composé qui peut avoir des transitions complexes. En utilisant useReducer, on peut définir des actions qui décrivent les changements de l'état, et le reducer se charge de mettre à jour l'état en fonction de ces actions. Cela offre une alternative à l'utilisation de useState pour la gestion de l'état plus complexe.
-  l'état stocké dans un composant avec un _context provider_ et accessible dans ses descendants via `useContext` / ✔️
   Le context provider est un mécanisme de React permettant de stocker un état partagé au niveau d'un composant parent et de le rendre accessible à tous ses composants descendants, quel que soit leur niveau de profondeur. Le context provider contient l'état et fournit une interface pour y accéder via useContext dans les composants descendants qui en ont besoin.

## 💻 J'utilise

### Un exemple personnel commenté / ✔️

fonction qui permet de recuperer via Axios et une API de films une liste de films en fonction d'une categorie et d'une page seletionne
const getMovies = (isRadio) => {
axios
.get(`https://api.themoviedb.org/3/movie/${selectedRadio}?api_key=cf0710105c7cebaf3b51cf0e45affb42&page=${page}`)
.then((res) => {
if (isRadio) {
setData(res.data.results)
setPage(1);
} else {
setData([...data, ...res.data.results])
setPage(page + 1);
}
})
}

    //ensuite il faut cloisonner la fonction getMovies dans le hooks useEffect pour que le get se fasse uniquement au montage du composant
    useEffect(() => {
        getMovies()
    }, []);

### Utilisation dans un projet / ✔️

https://github.com/PUGEAUTCam/DW_P7_V2_PUGEAUT_Camille/tree/main

Description : This is the front end and back end server for Project 7 of the Web Developer path OpenCLassrooms in november 2022.

Technologies used
Front-end : React, axios, redux toolkit, dayjs, infiniteScrool and styled components.
Back-end : NodeJS, Express and for the database MongoDB with this framework Mongoose.
Mon gros projet de fin de formation chew Open CLassroom, creation d'un reseau social avec diverses fonctionnalites. Realisation du front et du back. Projet de 4 mois.

### Utilisation en production si applicable / ✔️

https://github.com/PUGEAUTCam/DW_P7_V2_PUGEAUT_Camille/tree/main

Description : This is the front end and back end server for Project 7 of the Web Developer path OpenCLassrooms in november 2022.

Technologies used
Front-end : React, axios, redux toolkit, dayjs, infiniteScrool and styled components.
Back-end : NodeJS, Express and for the database MongoDB with this framework Mongoose.
Mon gros projet de fin de formation chew Open CLassroom, creation d'un reseau social avec diverses fonctionnalites. Realisation du front et du back. Projet de 4 mois que j'ai mis en ligne pendant quelques temps pour montrer au cours d'entretien technique.

### Utilisation en environement professionnel ❌ / ✔️

NON. J'utilise VueJS et pas react

## 🌐 J'utilise des ressources

### Titre

https://react.dev/blog/2023/03/16/introducing-react-dev
Documentation de react

https://www.youtube.com/watch?v=h2a0cSC1Vz8&t=3425s&ab_channel=ViDev
Tuto 1h incroyable, bien explique et avec les bonnes pratiques.

https://www.youtube.com/watch?v=7KC8QQXXN1M&t=6450s&ab_channel=codeconcept

https://stackoverflow.com/
Communaute entraide

## 🚧 Je franchis les obstacles

### Point de blocage / ✔️

Description: Je pratique peu react car je suis en Vue JS dans mon entrerpise

Plan d'action : (à valider par le formateur)

-  action 1 / ✔️ Bien travailler sur le projet de la WCS pour garder un niveau en react
-  action 2 / ✔️Creer des petits projets perso a cote pour ne pas perdre de niveau ni les avancees.
-  ...

Résolution :

## 📽️ J'en fais la démonstration

-  J'ai ecrit un [tutoriel](...) ❌ / ✔️
-  J'ai fait une [présentation](...) ❌ / ✔️
