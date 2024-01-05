# Titre de la compétence

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

-  les différences et points communs entre du code react et du code react native / ✔️
   Points communs :

Syntaxe JSX : React et React Native utilisent JSX, une syntaxe qui ressemble à du HTML pour définir la structure de l'interface utilisateur.
Composants : Les deux utilisent des composants pour construire l'UI, ce qui favorise la réutilisation du code et une meilleure organisation.
État et Props : La gestion de l'état et des props est identique, ce qui permet de passer des données et de gérer des interactions dynamiques de la même manière.
Différences :

Plateforme Cible : React est utilisé pour construire des applications web, tandis que React Native cible les applications mobiles (iOS et Android).
Éléments de l'interface : En React, on utilise des éléments HTML comme <div>, <span>, etc. En React Native, on utilise des composants spécifiques comme <View>, <Text>, qui sont traduits en composants natifs de la plateforme.
CSS : Le CSS n'est pas utilisé de la même manière ; React utilise des feuilles de style CSS standard, tandis que React Native utilise un système de style basé sur JavaScript avec une syntaxe similaire à CSS.

-  ce que devient et comment est interprêté le code javascript dans une application react native / ✔️
   Le code JavaScript dans une application React Native est exécuté dans un thread séparé appelé JavaScriptCore (sur iOS) ou sur le moteur JavaScript de l'appareil Android. Ce code est ensuite communiqué au thread principal natif via un pont. Les composants React Native sont mappés aux composants natifs correspondants, qui sont ensuite rendus sur l'écran du dispositif.
-  les avantages et inconvénients de react native / ✔️
   Avantages :

Cross-Platform : Code partagé entre iOS et Android, ce qui réduit le temps et le coût de développement.
Performance : Performances relativement élevées grâce à l'utilisation de composants natifs.
Communauté : Une large communauté et un écosystème d'outils et de bibliothèques.
Inconvénients :

Performances pour des opérations complexes : Peut être moins performant que le code natif pour des tâches très gourmandes en ressources.
Bridging : Le besoin de créer des ponts pour certaines fonctionnalités natives peut être complexe.
Mises à jour natives : Suivre les mises à jour et les changements dans les plateformes iOS et Android peut être exigeant.

-  la différence entre react native et expo / ✔️
   React Native est un framework de développement d'applications mobiles qui permet d'utiliser React pour construire des applications qui s'exécutent nativement sur les plateformes mobiles.

Expo est un ensemble d'outils et de services construits autour de React Native qui aide à démarrer rapidement avec le développement d'applications mobiles. Il fournit un ensemble de composants prêts à l'emploi et gère des aspects comme la compilation de l'application, la publication, et les mises à jour. Expo peut limiter l'accès à certaines fonctionnalités natives et est plus restrictif que React Native seul.

-  les principales briques qui composent react native (core components) / ✔️
   React Native propose une série de composants de base, tels que :

View : L'équivalent d'un div en HTML, pour l'organisation de l'UI.
Text : Pour afficher du texte.
Image : Pour afficher des images.
ScrollView : Pour permettre le défilement.
StyleSheet : Pour styliser les composants.
Button : Un composant simple pour créer un bouton.

-  comment écrire du style en react native / ✔️
   const styles = StyleSheet.create({
   container: {
   flex: 1,
   justifyContent: 'center',
   alignItems: 'center',
   backgroundColor: '#F5FCFF',
   },
   welcome: {
   fontSize: 20,
   textAlign: 'center',
   margin: 10,
   },
   });

-  comment est géré le layout en react native / ✔️
   Le layout en React Native est géré principalement par Flexbox. Les développeurs définissent le style de leurs composants en utilisant des propriétés telles que flexDirection, justifyContent, alignItems, pour organiser les éléments à l'écran. Cela permet une mise en page adaptative et réactive aux différentes tailles d'écran des appareils mobiles.

## 💻 J'utilise

### Un exemple personnel commenté / ✔️

// Import necessary React Native and React components.
import {
Text,
View,
StyleSheet,
FlatList,
TouchableOpacity,
ActivityIndicator,
} from 'react-native';
import { useEffect, useState } from 'react';
import { style } from '../styles';

// Apollo Client and GraphQL related imports for data fetching.
import { useQuery } from '@apollo/client';
import { GET_ALL_DOMAINS } from '../utils/graphql';

// Navigation hook from React Navigation to navigate between screens.
import { useNavigation } from '@react-navigation/native';

// Custom component to display gradient text.
import { GradientText } from '../components/GradientText';

// Utility function to calculate the average response time of requests.
import { calculateAverageResponseTime } from '../utils/calculateAverageResponseTime';

// Component that shows charts with the domains that have most views.
const MostViewsCharts = () => {
// GraphQL query hook to fetch domains data.
const { loading, error, data } = useQuery(GET_ALL_DOMAINS);
// Local state to store sorted domains based on views.
const [sortedDomains, setSortedDomains] = useState([]);
// Hook to access navigation functionality.
const navigation = useNavigation();

// Effect hook to sort domains by user request count after data is fetched.
useEffect(() => {
const sortDomain = () => {
if (data && data.getAllDomains && data.getAllDomains.length > 0) {
// Copy and sort the received domains data.
const sortedData = [...data.getAllDomains];
sortedData.sort((a, b) => b.userRequestCount - a.userRequestCount);
// Take the top 10 domains by user request count.
const topDomains = sortedData.slice(0, 10);
setSortedDomains(topDomains);
}
};
sortDomain();
}, [data]);

// Loading state UI.
if (loading) {
return (
<View style={style.containerGeneral}>
<ActivityIndicator size={'large'} color={'#b7623a'} />
</View>
);
}

// Error state UI.
if (error) return <Text>Error : {error.message}</Text>;

// No data state UI.
if (!data || !data.getAllDomains || data.getAllDomains.length === 0) {
return <Text style={style.text}>No data available</Text>;
}

// Main UI of the component.
return (
<View style={{ ...style.background, padding: 18 }}>
{/_ Display header text with gradient styling. _/}
<GradientText
        text="Our data is updated every 120 seconds"
        style={style.headerTitle}
      />
{/_ List of domains sorted by views. _/}
<FlatList
data={sortedDomains}
keyExtractor={(item) => item.id}
renderItem={({ item: domain }) => (
<TouchableOpacity
onPress={() => {
// Navigate to domain details when a list item is pressed.
navigation.navigate('DomainDetail', {
url: domain.url,
});
}} >
<View style={styles.container}>
<View style={styles.containerStatus}>
{/_ Display domain URL and the latest response status with color coding. _/}
<Text style={styles.head}>{domain.url}</Text>
<Text
style={{
                    color:
                      domain.requests[domain.requests.length - 1]
                        .responseStatus >= 200 &&
                      domain.requests[domain.requests.length - 1]
                        .responseStatus <= 299
                        ? '#64ff64'
                        : 'hsl(0, 100%, 54%)',
                  }} >
{
domain.requests[domain.requests.length - 1]
.responseStatus
}
</Text>
</View>

              <View>
                {/* Display latest and average response time. */}
                <Text style={style.text}>
                  Response time (ms) :{' '}
                  {
                    domain.requests[domain.requests?.length - 1]
                      .responseTime
                  }{' '}
                </Text>
                <Text style={style.text}>
                  Average response time (ms) :{' '}
                  {calculateAverageResponseTime(domain.requests)}
                </Text>
              </View>
            </View>
          </TouchableOpacity>
        )}
      />
    </View>

);
};

// Styles specific to this component.
const styles = StyleSheet.create({
head: {
color: 'rgb(226, 226, 226)',
fontWeight: 'bold',
marginBottom: 6,
},
container: {
paddingVertical: 10,
borderBottomWidth: 1,
borderBottomColor: 'rgba(226, 226, 226, 0.249)',
borderBottomStyle: 'solid',
},
containerStatus: {
flexDirection: 'row',
justifyContent: 'space-between',
},
});

//

### Utilisation dans un projet / ✔️

[https://github.com/Snoupix/UpOrDawn](projet de WCS)

Description : Projet WCS

### Utilisation en production si applicable / ✔️

[https://github.com/Snoupix/UpOrDawn](projet de WCS)

Description : Projet WCS

### Utilisation en environement professionnel / ✔️

Description : NON je n'utilise pas react native dans mon entreprise

## 🌐 J'utilise des ressources

### Titre

-  lien https://reactnative.dev/
-  description Site de react native

## 🚧 Je franchis les obstacles

### Point de blocage / ✔️

Description: Pas assez pratique

Plan d'action : (à valider par le formateur)

-  action 1 / ✔️ Faire un autre projet sur mobile
-  action 2 / ✔️
-  ...

Résolution :

## 📽️ J'en fais la démonstration

-  J'ai ecrit un [tutoriel](...) / ✔️
-  J'ai fait une [présentation](...) / ✔️
