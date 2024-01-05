# Integration continue

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

-  les enjeux de l'integration continue / ✔️
   'intégration continue (CI, pour Continuous Integration) est une pratique de développement où les développeurs fusionnent les modifications de code dans un dépôt centralisé fréquemment, idéalement plusieurs fois par jour. Voici les principaux enjeux associés à la CI :

Réduction des conflits de code : Intégrer régulièrement réduit le risque de conflits de fusion complexes.
Détection précoce des erreurs : En testant chaque modification, les erreurs sont détectées et corrigées plus tôt, ce qui améliore la qualité du code.
Automatisation du processus de test : Automatiser les tests garantit que chaque intégration est vérifiée, évitant les erreurs humaines.
Livraison accélérée : En facilitant les déploiements fréquents, la CI permet une livraison de fonctionnalités plus rapide aux utilisateurs.
Feedback en continu : Les développeurs reçoivent un retour rapide sur l'état de leur code, améliorant la communication au sein de l'équipe.
Documentation de l'historique des builds : Une trace de chaque intégration est conservée, ce qui est utile pour les audits et les analyses.

-  la mise en place d'une github action / ✔️
   GitHub Actions est un outil d'automatisation qui permet de créer des workflows personnalisés directement dans votre dépôt GitHub. Voici les étapes de base pour mettre en place une GitHub Action :

Créer un fichier de workflow : Les workflows sont définis par un fichier YAML dans le dossier .github/workflows du dépôt.
Définir des événements déclencheurs : Chaque workflow est déclenché par un ou plusieurs événements, comme un push ou un pull request.
Configurer des jobs : Un workflow contient des jobs qui définissent un ensemble de tâches à exécuter.
Définir des étapes et des actions : Chaque job est constitué d'étapes qui utilisent des actions (des scripts ou des commandes prédéfinies) pour exécuter des tâches spécifiques.
Paramétrer des secrets et des variables d'environnement : Sécuriser les credentials et définir des variables pour les utiliser dans les actions.
Tester le workflow : Après avoir commis le fichier de workflow, GitHub Actions l'exécutera à chaque événement déclencheur défini.
Monitorer les résultats : Les résultats sont visibles dans l'onglet Actions de votre dépôt GitHub, où vous pouvez voir le succès ou l'échec des workflows.
En configurant correctement une GitHub Action, vous pouvez automatiser des tâches comme le déploiement, les tests, la linting et bien d'autres processus dans votre chaîne de développement logiciel.

## 💻 J'utilise

### Un exemple personnel commenté / ✔️

# This section defines the events that will trigger the workflow

on:
push: # When a push is made...
branches:

-  '\*ci' # ...to any branch that ends with 'ci'
   pull_request: # Or when a pull request is made...
   branches: - master # ...to the master branch

# This section defines the jobs that the workflow will run

jobs:
back: # This is the job identifier for the backend
runs-on: ubuntu-latest # The job will run on the latest Ubuntu runner
steps: # Steps that will be executed as part of this job - uses: actions/checkout@v4 # Checks out the repository code

      - name: Install Jest & ts-node  # Step for installing Jest and ts-node
        run: npm install -g jest ts-node  # The command to run

      - name: Change env var "DEFAULT_INTERVAL"  # Step to modify an environment variable
        run: |  # Multiple commands can be run using the pipe symbol
          cd back  # Changes directory to 'back'
          sed -i 's/DEFAULT_INTERVAL=300000/DEFAULT_INTERVAL=60000/g' .env  # Uses sed to replace DEFAULT_INTERVAL value in .env file

      - name: Build and run the containers  # Step to build and run Docker containers
        run: |  # Running multiple commands
          docker compose build  # Builds the Docker containers using docker-compose
          docker compose up -d  # Runs the Docker containers in detached mode

      - name: Run tests  # Step to execute tests
        run: |  # Running multiple commands
          cd back  # Changes directory to 'back'
          npm install  # Installs npm dependencies
          npm run test  # Runs tests defined in package.json

      - name: Stop containers  # Step to stop the Docker containers
        run: docker compose down  # Stops the running containers using docker-compose

front: # This is the job identifier for the frontend
runs-on: ubuntu-latest # The job will run on the latest Ubuntu runner
steps: # Steps that will be executed as part of this job - uses: actions/checkout@v4 # Checks out the repository code

      # The following steps are similar to the 'back' job but for the frontend
      - name: Install Jest & ts-node
        run: npm install -g jest ts-node

      - name: Build and run the containers
        run: |
          docker compose build
          docker compose up -d

      - name: Run tests
        run: |
          cd front
          npm install
          npm run test

      - name: Stop containers
        run: docker compose down

### Utilisation dans un projet / ✔️

[https://github.com/Snoupix/UpOrDawn](projet de WCS)

Description :

### Utilisation en production si applicable / ✔️

[https://github.com/Snoupix/UpOrDawn](projet de WCS)

Description :

### Utilisation en environement professionnel / ✔️

Description : NON je ne fais pas de CI dans mon entreprise

## 🌐 J'utilise des ressources

### Titre

-  lien https://www.youtube.com/watch?v=h9K1NnqwUvE&ab_channel=Simplilearn
   https://www.youtube.com/watch?v=R8_veQiYBjI&ab_channel=TechWorldwithNana
-  description Cours video sur la CI et github actions

## 🚧 Je franchis les obstacles

### Point de blocage / ✔️

Description: Pas assez travaille comem tout le reste dans cette alternance, survole

Plan d'action : (à valider par le formateur)

-  action 1 / s'entrainer
-  action 2 /
-  ...

Résolution :

## 📽️ J'en fais la démonstration

-  J'ai ecrit un [tutoriel](...) / ✔️
-  J'ai fait une [présentation](...) / ✔️
