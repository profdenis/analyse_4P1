# Dénormalisation

La **dénormalisation** est le processus de réintroduction de la redondance dans une base de données relationnelle
normalisée, généralement pour améliorer les performances en réduisant le nombre de jointures nécessaires pour extraire
les données.

Voici quelques raisons pour lesquelles vous pourriez envisager une dénormalisation :

1. **Amélioration de la performance des requêtes de lecture** : Si votre application a pour objectif des performances de
   lecture rapides et nécessite moins d'écritures, la dénormalisation peut aider à accélérer vos requêtes de lecture en
   réduisant le nombre de jointures nécessaires et en permettant un accès plus direct aux données.

2. **Réduction de la complexité** : Même si la normalisation réduit la redondance et améliore la logique du stockage des
   données, elle peut rendre certains types de requêtes ou d'analyses plus complexes. Parfois, une certaine redondance (
   comme le stockage pré-calculé d'un total) peut rendre une requête beaucoup plus simple.

3. **Compatibilité avec des non-SGBD** : Pour interagir avec certains systèmes ou services qui ne sont pas des SGBD,
   comme les systèmes de recherche en texte intégral, vous pouvez avoir besoin de données dénormalisées.

4. **Optimisation pour les systèmes de bases de données distribuées (par ex. NoSQL)** : De nombreux systèmes de bases de
   données distribuées favorisent les modèles de données dénormalisées en raison de la façon dont ils répartissent les
   données sur le réseau.

Il convient cependant de noter que la dénormalisation n'est généralement pas la première méthode d'optimisation à
envisager et qu'elle doit être utilisée avec prudence. Elle peut en effet introduire des anomalies de données, augmenter
la complexité des écritures de données et occuper plus d'espace de stockage. Avant de dénormaliser, il convient
d'examiner les autres options d'optimisation et de bien comprendre les conséquences de la dénormalisation.

## Exemple

Comment pourrait-on dénormaliser la BD suivante ?

![](pagila.png)