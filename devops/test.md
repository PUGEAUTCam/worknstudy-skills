# Tester son application

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

-  les tests unitaires / ✔️
   Ce sont des tests qui évaluent le fonctionnement de composants individuels (ou "unités") du code de manière isolée. Le but est de s'assurer que chaque unité fonctionne correctement en tant qu'élément séparé.
-  les mocks / ✔️
   Ce sont des objets ou des fonctions simulées qui reproduisent le comportement d'autres parties du code qui ne font pas partie du test en cours. Ils sont utilisés pour créer des conditions de test contrôlées et éviter les dépendances externes lors de l'exécution des tests unitaires.
-  les tests d'integration / ✔️
   Ils visent à tester les interactions entre différentes unités de code pour s'assurer qu'elles fonctionnent ensemble comme prévu. C'est une étape intermédiaire entre les tests unitaires et les tests de bout en bout.
   Les tests de bout en bout (end-to-end) : Ces tests simulent des scénarios d'utilisation réels en exécutant une application complète, souvent dans un environnement qui imite la production. L'objectif est de vérifier que le système dans son ensemble fonctionne comme attendu.

Le TDD (Test-Driven Development) : C'est une méthode de développement logiciel dans laquelle les spécifications et les exigences sont converties en tests spécifiques avant que le code ne soit écrit. Le développement est ensuite guidé par l'évolution des tests, le code étant amélioré jusqu'à ce que tous les tests passent.

Les tests par snapshot : Ils capturent l'état d'un rendu de composant ou d'une structure de données et le comparent à une "instantané" (snapshot) précédemment enregistrée. Si l'état actuel diffère de l'instantané, le test échoue. Cela est souvent utilisé dans le développement front-end pour s'assurer que les changements dans le code ne produisent pas de résultats inattendus dans l'interface utilisateur.

## 💻 J'utilise

### Un exemple personnel commenté / ✔️

// Import the necessary modules from Jest for testing and from Apollo Client for making GraphQL queries
import { test, expect } from '@jest/globals';
import { ApolloClient, InMemoryCache } from '@apollo/client';

// Import the GraphQL queries from a local module (not shown in this snippet)
import \* as GQL from '../src/graphql';

// Initialize the ApolloClient with the URI of the GraphQL server and set up the in-memory cache
const client = new ApolloClient({
uri: 'http://localhost:4000/graphql',
cache: new InMemoryCache(),
});

// Describe a block of tests. This block does not use mock data for GraphQL requests.
describe('GraphQL without mock data', () => {
// A test to check if the database is initially empty
test('Is database empty', async () => {
// Perform a GraphQL query to get all domains
const r = await client.query({
query: GQL.GET_ALL_DOMAINS,
});

        // Expect no errors in the response
        expect(r.error).toBeUndefined();
        // Expect the list of all domains to be empty (length of 0)
        expect(r.data.getAllDomains).toHaveLength(0);
    });

    // A test to create mock data in the database
    test('CreateMockData', async () => {
        // Perform a GraphQL mutation to create mock data
        const r = await client.query({
            query: GQL.CREATE_MOCK_DATA,
        });

        // Expect no errors in the response
        expect(r.error).toBeUndefined();
        // Expect the mutation to return a success message indicating mock data was created
        expect(r.data.CreateMockData).toBe('Mock data created !');
    });

    // A test to check if the database is filled after creating mock data
    test('Is database filled', async () => {
        // Perform a GraphQL query to get all users
        const r = await client.query({
            query: GQL.GET_ALL_USERS,
        });

        // Expect no errors in the response
        expect(r.error).toBeUndefined();
        // Expect there to be users present in the database (length greater than 0)
        expect(r.data.getAllUsers.length).toBeGreaterThan(0);
    });

});

### Utilisation dans un projet / ✔️

[https://github.com/Snoupix/UpOrDawn](projet de WCS)

### Utilisation en production si applicable❌ / ✔️

[https://github.com/Snoupix/UpOrDawn](projet de WCS)

### Utilisation en environement professionnel ❌ / ✔️

Description : Pas de test en front dans mon entreprise

## 🌐 J'utilise des ressources

### Titre

https://www.youtube.com/watch?v=Jv2uxzhPFl4&ab_channel=Fireship

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
