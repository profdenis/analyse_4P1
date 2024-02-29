# Architecture événementielle

L'architecture événementielle (Event-Driven, ou architecture pilotée par les événements), est un modèle d'architecture
logicielle où le flux du logiciel est déterminé par des événements tels que les actions de l'utilisateur, les
déclencheurs de capteurs ou les messages d'autres programmes. Ceci est particulièrement populaire dans les
environnements d'interface utilisateur moderne, les systèmes en temps réel et les environnements serveurs.

Dans une architecture pilotée par les événements, un morceau de logiciel (un "émetteur" d'événements) crée ou "émet" un
événement en réponse à un changement d'état spécifique, tel qu'une action de l'utilisateur ou un déclencheur de capteur.
Cet événement est ensuite reçu par un ou plusieurs "écouteurs d'événements", qui prennent des mesures en réponse.

Les avantages de ce type d'architecture incluent la faible couplage et la scalabilité. Comme les émetteurs et les
écouteurs d'événements sont généralement indépendants l'un de l'autre, des modifications peuvent être apportées à un
émetteur sans nécessairement affecter ses écouteurs, et vice versa. Cela facilite également l'ajout de nouvelles
fonctionnalités : un nouvel écouteur d'événements peut être ajouté sans modifier l'émetteur.

L'architecture pilotée par les événements est également très efficace pour gérer des charges de travail élevées, car
elle permet un traitement asynchrone des événements. Cela signifie que le système peut continuer à accepter et à traiter
d'autres événements pendant qu'un événement est en cours de traitement.

Cependant, cette architecture peut rendre le flux de contrôle plus difficile à comprendre et à gérer, car le traitement
est réparti entre de nombreux écouteurs d'événements, fonctionnant potentiellement de manière asynchrone.

En somme, l'architecture pilotée par les événements est idéale pour les applications qui doivent gérer un grand nombre
d'événements, particulièrement dans des situations où la réactivité et la performance sont importantes.

