# GraphQL

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

-  la différence entre REST et GraphQL / ✔️
   REST est une architecture qui fonctionne sur le principe d'avoir des points de terminaison distincts pour différentes données ou opérations. Elle utilise les méthodes HTTP (GET, POST, PUT, DELETE) pour lire et modifier les ressources sur le serveur. Les réponses en REST incluent souvent des données supplémentaires que le client n'a pas demandées, ce qui peut conduire à une sur- ou sous-demande de données.
   GraphQL est un langage de requête et un système d'exécution pour les API qui permet aux clients de demander précisément ce dont ils ont besoin. Il évite les problèmes de sur- et sous-demande de données en permettant aux clients de définir la structure de la réponse. Avec GraphQL, il y a généralement un seul point de terminaison qui gère toutes les requêtes.
-  les besoins auxquels répond GraphQL / ✔️
   GraphQL répond au besoin de flexibilité et d'efficacité dans le chargement de données pour les applications, surtout celles avec des structures de données complexes ou des interfaces utilisateurs dynamiques. Il permet aux clients de récupérer de multiples ressources en une seule requête, contrairement à REST, qui pourrait nécessiter plusieurs round trips pour obtenir la même quantité d'informations.
-  la définition d'un schéma
   Un schéma dans le contexte de GraphQL est une description du type de données que l'on peut interroger sur ce système. Il définit les types de données, les relations entre eux, ainsi que les opérations disponibles (queries et mutations). Le schéma est essentiellement un contrat entre le client et le serveur qui définit comment les données peuvent être échangées.
-  Query / ✔️
   Une Query dans GraphQL est utilisée pour lire ou récupérer des valeurs. Elle est comparable à une opération GET dans REST. Avec les queries, les clients peuvent spécifier exactement quelles données ils veulent et dans quel format, sans être contraints par les structures de données prédéfinies du serveur.
-  Mutation / ✔️
   Une Mutation est l'équivalent d'une écriture, modification ou suppression dans GraphQL. Si vous voulez créer, modifier, ou supprimer des données sur le serveur, vous utiliseriez une mutation. Elles sont analogues aux méthodes POST, PUT, DELETE en REST, mais comme les queries, elles permettent au client de spécifier exactement quelles données retourner après l'opération.
-  Subscription / ✔️
   Une Subscription est un type d'opération dans GraphQL qui permet au client de s'abonner à des événements en temps réel du serveur. Cela signifie que le serveur peut pousser des mises à jour au client lorsque certaines données changent, ce qui permet aux applications de rester synchronisées avec le serveur sans polling régulier.

## 💻 J'utilise

### Un exemple personnel commenté / ✔️

// Importation des décorateurs nécessaires depuis `type-graphql` et `typeorm`.
import { ObjectType, Field, ID } from 'type-graphql';
import { Column, Entity, ManyToMany, PrimaryGeneratedColumn } from 'typeorm';

// Importation de la classe Domain, qui représente une autre entité.
import Domain from './Domain';

// Décorateur ObjectType de type-graphql qui indique qu'il s'agit d'un type d'objet GraphQL.
@ObjectType()
// Décorateur Entity de typeorm qui indique qu'il s'agit d'une entité de base de données.
@Entity()
export default class User {
// Constructeur pour initialiser un utilisateur avec username, email, et password.
constructor(username: string, email: string, password: string) {
this.username = username;
this.email = email;
this.password = password;
}

    // Field decorator expose ce champ comme un champ GraphQL, et PrimaryGeneratedColumn l'identifie comme la PK auto-incrémentée.
    @Field(() => ID)
    @PrimaryGeneratedColumn({ type: 'int' })
    id: number;

    // Expose username comme un champ de type GraphQL et le marque comme une colonne de la table User dans la BD.
    @Field()
    @Column()
    username: string;

    // Déclare l'email comme champ unique de GraphQL et comme colonne dans la BD.
    @Field()
    @Column({ unique: true })
    email: string;

    // Expose le password dans GraphQL; pour des raisons de sécurité, cela ne devrait normalement pas être exposé.
    @Field()
    @Column()
    password: string;

    // Définit un champ GraphQL pour le statut premium et lui attribue une valeur par défaut de 'false' dans la BD.
    @Field()
    @Column({ default: false })
    isPremium: boolean;

    // Définit une relation plusieurs-à-plusieurs avec l'entité Domain, et initialise avec un tableau vide par défaut.
    @Field(() => [Domain], { defaultValue: [] })
    @ManyToMany(() => Domain, (domain) => domain.users)
    domains: Domain[];

}

### Utilisation dans un projet / ✔️

[https://github.com/Snoupix/UpOrDawn](projet de WCS)

Description :

### Utilisation en production si applicable / ✔️

[lien du projet](...)

Description :

### Utilisation en environement professionnel / ✔️

Description : NOn je ne fais pas de back

## 🌐 J'utilise des ressources

### Titre

-  lien https://graphql.org/
-  description Site de graphql

## 🚧 Je franchis les obstacles

### Point de blocage / ✔️

Description:

Plan d'action : (à valider par le formateur)

-  action 1 / ✔️
-  action 2 / ✔️
-  ...

Résolution :

## 📽️ J'en fais la démonstration

-  J'ai ecrit un [tutoriel](...) ❌ / ✔️
-  J'ai fait une [présentation](...) ❌ / ✔️
