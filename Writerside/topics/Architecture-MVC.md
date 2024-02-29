# Architecture MVC

L'architecture Modèle-Vue-Contrôleur (MVC) est un modèle d'architecture logicielle très couramment utilisé pour la
conception d'applications, en particulier les applications web et mobiles.

Dans l'architecture MVC, une application est divisée en trois composants principaux : le Modèle, la Vue et le
Contrôleur.

1. **Le Modèle (Model)** gère les données et la logique métier de l'application. Il communique avec la base de données
   pour récupérer, insérer et mettre à jour les informations. En même temps, il implémente les règles et la logique
   métier qui conduisent les processus de traitement des données.

2. **La Vue (View)** est responsable de l'affichage des données à l'utilisateur, c'est-à-dire de la présentation des
   données. La vue prend les données du modèle et les affiche d'une manière que l'utilisateur peut comprendre. Cela peut
   inclure des tableaux, des diagrammes, du texte brut ou toute autre forme de visualisation de données.

3. **Le Contrôleur (Controller)** sert d'intermédiaire entre le Modèle et la Vue. Il gère les entrées de l'utilisateur (
   par exemple les clics de souris, les pressions de touches, les actions vocales) et les traduit en actions appropriées
   à exécuter dans le Modèle. Une fois que le Modèle a effectué les changements nécessaires aux données, le Contrôleur
   met à jour la Vue pour refléter ces nouveautés.

L'architecture MVC offre plusieurs avantages, comme la séparation des préoccupations (SoC) : chaque composant a une
responsabilité claire, ce qui rend l'application plus facile à développer, tester, et maintenir. De plus, il permet à
plusieurs vues d'utiliser le même modèle, ce qui facilite la réutilisation du code.

Cependant, pour des applications plus complexes, l'architecture MVC peut devenir difficile à gérer car le Contrôleur
peut finir par gérer beaucoup de logique d'affaires, ce qui l'entraine à devenir volumineux et difficile à maintenir.
