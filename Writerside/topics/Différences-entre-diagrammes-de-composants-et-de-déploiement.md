# Différences entre diagrammes de composants et de déploiement

Un **diagramme de composants** et un **diagramme de déploiement** sont deux types de diagrammes utilisés en modélisation
UML, mais ils servent à différents objectifs et représentent différents aspects d'un système.

## Diagramme de composants

Un diagramme de composants est principalement axé sur le système logiciel et ses composants. Il sert à visualiser,
spécifier et documenter les éléments logiciels de haut niveau d'un système, leurs interrelations et leurs dépendances.
Les composants peuvent être des parties de code (comme les classes ou les modules), des bases de données, des interfaces
utilisateur, des composants tiers, etc. Une relation entre composants pourrait être une dépendance (un composant a
besoin d'un autre pour fonctionner correctement) ou une interaction (un composant envoie/reçoit des données à un autre).

## Diagramme de déploiement

Un diagramme de déploiement se concentre sur l'aspect matériel et sur la façon dont le logiciel est déployé sur le
matériel. Il montre le **où** du système. Il illustre la configuration physique de l'infrastructure matérielle (nœuds),
ainsi que la façon dont les composants du logiciel sont répartis sur ces nœuds et comment ils interagissent entre eux.
Les nœuds peuvent être des serveurs, des ordinateurs, des terminaux mobiles, des appareils IoT, etc, et leurs relations
peuvent comprendre des aspects comme le réseau, la communication, le protocole utilisé, etc.

En conclusion, alors que le diagramme de composants décrit le 'quoi' (les composants) et le 'comment' (leurs relations)
du système, le diagramme de déploiement décrit le **où** (la disposition des composants logiciels sur l'infrastructure
matérielle) et le **comment** (comment ils interagissent à ce niveau).
