# Modèles de données

Les modèles de données servent à décrire comment les données sont structurées dans une base de données.

## Principaux modèles de données

1. **Modèle relationnel** : Les données sont organisées en tables (relations). Chaque tableau représente une entité et
   les relations entre les entités sont exprimées par rapport entre les tables. Les SGBD (systèmes de gestion de bases
   de données) relationnels sont très populaires.

2. **Modèle objet-relationnel** : Une extension du modèle relationnel qui permet aux développeurs d'intégrer leurs
   propres types de données, opérateurs et fonctions dans le SGBD, étendant ainsi les capacités du modèle de données
   relationnel. PostgreSQL est un exemple d'un SGBD qui supporte ce modèle.

3. **Modèle hiérarchique** : Les données sont organisées en arborescence, avec un nœud racine, des nœuds enfants et
   ainsi de suite. Chaque nœud correspond à une entité et chaque lien représente une relation entre deux entités.

4. **Modèle en réseau** : C'est une extension du modèle hiérarchique où chaque nœud peut avoir plusieurs parents. Cela
   permet une représentation plus complexe des relations entre données.

5. **Modèle orienté objet** : Les données sont organisées sous la forme d'objets, qui sont des instances de classes. Les
   relations entre les objets sont exprimées par des associations, de l'héritage et de la composition.

6. **Modèle de document** : Utilisé dans les bases de données NoSQL, les informations sont organisées en documents,
   généralement au format JSON.

7. **Modèle orienté graphe** : Les données sont conservées sous forme de graphes avec des nœuds, des arêtes
   et des propriétés.

## Principaux types de bases de données

1. **SQL** (Structured Query Language) ou **SGBD relationnel** ou **objet-relationnel** : Basées sur le modèle
   relationnel objet-relationnel des données. MySQL, PostgreSQL, Oracle, et SQL Server en sont quelques exemples.

2. **NoSQL**: Ils sont capables de gérer un grand volume de données réparties sur de nombreux serveurs. Ils comprennent
   les bases de données de documents comme MongoDB, les bases de données de graphes comme Neo4j, les bases de données de
   colonnes comme Cassandra, et les bases de données de clés-valeurs comme Redis.

3. **NewSQL** : Concilie les avantages des bases de données NoSQL pour le traitement des big data avec la garantie
   d'ACID (atomicité, cohérence, isolation, durabilité) dont bénéficient les bases de données SQL. Exemple : Voltdb,
   CockroachDB.

4. **Bases de données en mémoire** : Elles conservent l'ensemble de leurs données en RAM et sont donc extrêmement
   rapides. Exemple : Redis, Memcached.

