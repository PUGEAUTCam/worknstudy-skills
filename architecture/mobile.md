# Technologies d'applications mobiles

## 🎓 J'ai compris et je peux expliquer

Différences entre les webapps, les applications hybrides et natives (✔️):

Webapps : Ce sont des applications qui fonctionnent dans un navigateur web. Elles ne sont pas installées sur l'appareil de l'utilisateur et sont généralement développées en HTML, CSS et JavaScript. Elles sont accessibles via une URL et dépendent d'une connexion Internet.
Applications Hybrides : Ces applications sont une combinaison d'éléments de webapps et d'applications natives. Elles sont développées en utilisant des technologies web (HTML, CSS, JavaScript), mais sont encapsulées dans un conteneur natif, leur permettant ainsi d'accéder aux fonctionnalités de l'appareil (comme la caméra, le GPS, etc.). Exemples : Cordova, Ionic.
Applications Natives : Développées spécifiquement pour un système d'exploitation particulier (iOS, Android) en utilisant les langages et outils préconisés par la plateforme (Swift pour iOS, Kotlin/Java pour Android). Ces applications peuvent pleinement exploiter les capacités de l'appareil et offrent généralement une meilleure performance et une expérience utilisateur plus fluide.

Fonctionnement d'une app React Native (✔️):

React Native est un framework pour développer des applications mobiles en utilisant JavaScript et React.
Ce qui est produit : L'application créée est un mélange de composants JavaScript et natifs. React Native compile les composants en éléments natifs, offrant une expérience similaire à celle d'une application native.
Communication JS-Natif : React Native utilise un "pont" pour permettre la communication entre le JavaScript et le code natif. Cela permet aux développeurs d'écrire du code JavaScript qui interagit avec les fonctionnalités natives de l'appareil.

Différentes technologies (frameworks) pour développer des apps mobiles (✔️):

React Native : Permet de développer des applications mobiles en utilisant JavaScript et React.
Flutter : Un framework de Google pour créer des applications mobiles avec le langage Dart.
Xamarin : Utilise C# pour développer des applications qui peuvent s'exécuter sur plusieurs plateformes.
Ionic : Basé sur des technologies web pour créer des applications hybrides.
Swift (pour iOS) et Kotlin/Java (pour Android) : Pour le développement d'applications natives.

Principaux points d'attention entre le développement d'une app mobile ou desktop (✔️):

Interface Utilisateur : Les interfaces mobiles sont généralement plus simplifiées et conçues pour les écrans tactiles, tandis que les applications de bureau peuvent avoir des interfaces plus complexes et sont conçues pour le clavier et la souris.
Performance et Optimisation : Les applications mobiles doivent être optimisées pour des ressources limitées (CPU, mémoire), alors que les applications de bureau peuvent généralement compter sur des ressources plus abondantes.
Taille de l'écran et Résolution : Les applications mobiles doivent être conçues pour une variété de tailles d'écran et de résolutions, tandis que les applications de bureau ont généralement des contraintes moins strictes.
Fonctionnalités de l'Appareil : Les applications mobiles peuvent avoir besoin d'intégrer des fonctionnalités spécifiques à l'appareil, telles que les capteurs de mouvement, la caméra, ou le GPS.
Distribution : Les applications mobiles sont généralement distribuées via des app stores (App Store pour iOS, Google Play pour Android), tandis que les applications de bureau peuvent être téléchargées directement ou distribuées via des plateformes comme Steam ou le Microsoft Store.

## 💻 J'utilise

### Un exemple personnel commenté / ✔️

import React from 'react';
import { createStackNavigator } from '@react-navigation/stack';
import { headerOptions } from '../App';
import Ionicons from '@expo/vector-icons/Ionicons';
import MyAccount from '../screens/MyAccount';
import Signup from '../screens/Signup';

const Stack = createStackNavigator();

const AuthNavigator = () => {
return (
<Stack.Navigator
screenOptions={({ route }) => ({
...headerOptions,
})}>
<Stack.Screen name="MyAccount" component={MyAccount} options={{ title: 'Account' }} />
<Stack.Screen
name="Signup"
component={Signup}
options={({ navigation }) => ({
title: 'Sign Up !',
headerLeft: (props) => (
<Ionicons
name="ios-arrow-back"
size={28}
color="orange"
style={{ paddingLeft: 10 }}
onPress={() => navigation.goBack()}
/>
),
})}
/>
</Stack.Navigator>
);
};

export default AuthNavigator;

Ce code est un exemple d'un composant en React utilisant la bibliothèque @react-navigation/stack pour la navigation dans une application mobile développée avec React Native. Voici une explication rapide de ses principales parties :

Importations :

React : Importation de base de React.
createStackNavigator : Importe la fonction pour créer un navigateur de pile (stack navigator), qui permet de naviguer entre les écrans par empilement.
headerOptions : Importe probablement des options de style personnalisées pour les en-têtes de navigation.
Ionicons : Importe des icônes de la bibliothèque @expo/vector-icons.
MyAccount et Signup : Importe deux composants d'écran, probablement pour le compte utilisateur et l'inscription.
Création d'un Stack Navigator :

const Stack = createStackNavigator(); : Crée une nouvelle instance de stack navigator.
Composant AuthNavigator :

Le composant fonctionnel AuthNavigator est défini ici. Il retourne un navigateur de pile avec deux écrans configurés.
<Stack.Navigator> : Définit le conteneur pour les écrans de navigation. Il utilise screenOptions pour appliquer des options de style communes à tous les écrans (dans ce cas, en utilisant headerOptions).
<Stack.Screen> pour MyAccount : Définit un écran dans le navigateur de pile. name est l'identifiant de l'écran, et component spécifie le composant à rendre (ici, MyAccount). options définit les options spécifiques pour cet écran, comme le titre de l'en-tête.
<Stack.Screen> pour Signup : De même, définit un autre écran pour l'inscription. En plus du titre, il personnalise l'icône de retour (headerLeft) avec un composant Ionicons, qui, lorsqu'il est pressé, renvoie l'utilisateur à l'écran précédent.
Exportation du Composant :

export default AuthNavigator; : Exporte le composant AuthNavigator pour une utilisation dans d'autres parties de l'application.
En résumé, ce code configure un système de navigation pour une application mobile, avec deux écrans (MyAccount et Signup) et des options de navigation personnalisées, notamment une icône de retour personnalisée pour l'écran Signup.

### Utilisation dans un projet / ✔️

[https://github.com/Snoupix/UpOrDawn/tree/master/mobile](projet de WCS)

Description : Projet de la WCS en mode mobile avec react native

### Utilisation en production si applicable / ✔️

[https://github.com/Snoupix/UpOrDawn/tree/master/mobile](projet de WCS)

Description : Projet de la WCS en mode mobile avec react native

### Utilisation en environement professionnel / ✔️

Pas de mobile en pro chez Interencheres

## 🌐 J'utilise des ressources

### Titre

-  https://reactnative.dev/
-  Site de react native avec tuto

https://www.youtube.com/watch?v=mJ3bGvy0WAY&t=509s&ab_channel=JavaScriptMastery

## 🚧 Je franchis les obstacles

### Point de blocage / ✔️

Description: Pas assez pratique

Plan d'action : (à valider par le formateur)

-  action 1 / ✔️ Realiser un autre projet en react native
-  action 2 / ✔️
-  ...

Résolution :

## 📽️ J'en fais la démonstration

-  J'ai ecrit un [tutoriel](...) ❌ / ✔️
-  J'ai ecrit un [article](...) ❌ / ✔️
-  J'ai fait une [présentation](...) ❌ / ✔️
