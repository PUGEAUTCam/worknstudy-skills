# TypeScript

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

-  l'intéret de TypeScript dans l'IDE / ✔️
   Permet une vérification statique des types, une autocomplétion améliorée, une meilleure documentation des objets et des fonctions, ainsi qu'une détection précoce des erreurs potentielles. Cela facilite le développement, réduit les bugs et améliore la productivité globale.
-  les types de bases / ✔️
   Les types de base incluent :

number pour les nombres (entiers et décimaux),
string pour les chaînes de caractères,
boolean pour les valeurs booléennes (true ou false),
array pour les tableaux,
object pour les objets,
null et undefined pour les valeurs spéciales représentant l'absence de valeur.

-  comment et pourquoi étendre une interface / ✔️
   En TypeScript, il est possible d'étendre une interface existante en ajoutant de nouvelles propriétés ou en redéfinissant les propriétés existantes. Pour étendre une interface, on utilise le mot-clé extends. L'extension d'une interface permet d'ajouter des fonctionnalités supplémentaires à un type existant sans avoir à le réécrire complètement. Cela favorise la réutilisabilité du code et permet de créer des hiérarchies de types plus spécifiques tout en maintenant la compatibilité avec les types parent.
-  les classes et les decorators / ✔️
   n TypeScript, les classes sont des structures de programmation qui permettent de créer des objets avec des propriétés et des méthodes associées. Les classes peuvent être utilisées pour modéliser des entités et créer des instances d'objets. Les decorators, quant à eux, sont des annotations qui peuvent être appliquées à des classes, des méthodes ou des propriétés. Ils permettent d'ajouter des fonctionnalités supplémentaires à ces éléments, tels que la journalisation, la validation des données, l'injection de dépendances, etc.

## 💻 J'utilise

### Un exemple personnel commenté / ✔️

interface PharmacieInfo {
id: number
name: string
address_city: string
address_country: string
address_line_1: string
address_zip_code: string
cip: string
} // Ici je creer une interfce pour les infos que je vais recuperer depuis l'API

const InfosLab = () => {
const [data, setData] = useState<PharmacieInfo>() // Ici je dis que les infos stockes dans mon state seront type selon mon interface, cela permet d'eviter les erreurs lorsque je vais recup mes infos

    useEffect(() => {
        getOnePharmacie(pharmacieId).then((res) => setData(res.data));
    }, [])

    return (
        <ContainerInfosPharma>
            <h2>{data?.name || "-"}</h2>
            <h3>Adresse</h3>
            <p>{data?.address_line_1 || "-"}</p>
            <p>{data?.address_zip_code || "-"}</p>
            <p>{data?.address_city || "-"}</p>
            <p>{data?.address_country || "-"}</p>
            <h3>CIP</h3>
            <p>{data?.cip || "-"}</p>
        </ContainerInfosPharma>
    ); // Ici j'affiches mes infos

};

export default InfosLab;

### Utilisation dans un projet / ✔️

https://github.com/PUGEAUTCam/Test_front_end

Description : Creation pour un test technique d'une interface front end pour une gestion de plaintes pour les pharmacies.
Technos utilisees : React et typescript, axios.
Creation d'une page qui regroupe toutes les plaintes, une page pour creer une nouvelle plainte, une pagep our rechercher les pharmacies avec pagination...

### Utilisation en production si applicable / ✔️

https://github.com/Interencheres

Description : Mon projet en entreprise

### Utilisation en environement professionnel / ✔️

Description : J'utilise au sein de mon entreprise le framework javascript VueJS avec typescript du cote front end.

## 🌐 J'utilise des ressources

### Titre

https://www.typescriptlang.org/docs/
La documentation de TypeScript fournit une référence complète de toutes les fonctionnalités, syntaxes et concepts du langage. Elle couvre en détail les différents types de données, les déclarations de variables, les fonctions, les classes, les modules, etc. Cette référence vous permet de consulter rapidement les informations nécessaires pour comprendre et utiliser correctement le langage TypeScript.
exemples de code pour illustrer l'utilisation des différentes fonctionnalités de TypeScript. Ces exemples sont accompagnés d'explications détaillées, ce qui facilite la compréhension et l'apprentissage. Les illustrations visuelles, comme les diagrammes et les schémas, aident également à mieux comprendre certains concepts plus complexes.
Guides et bonnes pratiques : La documentation inclut des guides et des bonnes pratiques pour le développement avec TypeScript.

https://www.youtube.com/watch?v=d56mG7DezGs&ab_channel=ProgrammingwithMosh
Video courte mais tres bien resume sur le sperincipes de base de Typescript

## 🚧 Je franchis les obstacles

### Point de blocage ❌ / ✔️

Description: Typescript est trop restrictif et cela fait perdre parfois un temps considerable pour peu de choses

Plan d'action : (à valider par le formateur)

-  action 1 ❌ / ✔️ Apprendre a apprecier Typescript
-  action 2 ❌ / ✔️ Se forcer a utilisre typescript
-  ...

Résolution :

## 📽️ J'en fais la démonstration

-  J'ai ecrit un [tutoriel](...) ❌ / ✔️
-  J'ai fait une [présentation](...) ❌ / ✔️
