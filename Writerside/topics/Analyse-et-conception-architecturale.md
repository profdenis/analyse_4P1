# Analyse et conception architecturale

## UML

### Qu'est-ce que l'UML ?

L'**UML** (**Unified Modeling Language**), littéralement en français par _Langage de Modélisation Unifié_,
est un langage de modélisation graphique à base de pictogrammes conçu pour fournir une méthode normalisée pour
visualiser la conception d'un système. Il est largement utilisé dans la modélisation de systèmes et de processus
d'entreprise.

Il facilite la communication entre les membres d'une équipe de développement en fournissant une visualisation commune
des processus et de l'architecture du système. Étant un langage standard, il est compréhensible par tous les
développeurs, quel que soit le langage de programmation utilisé pour mettre en œuvre le système.

L'UML soutient une variété de diagrammes, y compris les diagrammes de classe, d'objets, de composants, de déploiement,
d'activités, d'état-transitions et de séquences. Chacun de ces diagrammes offre une perspective différente de la
conception du système, et ensemble, ils fournissent un aperçu complet et cohérent du système. Certains de ces diagrammes
sont utilisés lors de la _conception architecture_, d'autres lors de la _conception détaillée_.

### Qu'est-ce que l'UML n'est pas ?

L'UML n'est pas :

- **Un langage de programmation** : UML est un **langage de modélisation**, pas un langage de programmation.

- **Un processus de développement de logiciels** : Bien que UML puisse être utilisé dans le cadre de différents
  processus de développement de logiciels, il **ne prescrit pas un processus spécifique**. Des méthodologies comme le
  _Processus Unifié Rational_ (RUP) utilisent UML comme outil, mais UML en lui-même n'est pas un processus.

- **Une garantie de succès du logiciel** : UML est un outil de modélisation qui peut aider les équipes à penser à
  travers les problèmes et à communiquer des solutions. Cependant, il ne garantit pas que le logiciel développé sera
  réussi ou sans défaut.

- **Complet** : Bien que UML fournisse une grande variété de diagrammes pour la modélisation de nombreux aspects d'un
  système, il y a certaines choses qu'il ne peut pas modéliser ou qu'il ne modélise pas bien. Par exemple, il ne fournit
  pas une bonne représentation des interfaces utilisateur.

- **Strictement nécessaire** : Pour certains projets, en particulier ceux qui sont plus petits ou moins complexes,
  utiliser UML peut être plus une question de préférence que de nécessité. Certaines équipes peuvent trouver que
  l'utilisation d'UML améliore leur processus, tandis que d'autres peuvent réussir sans lui.

## Diagrammes pour la conception architecturale

Pour la conception de haut niveau d'un logiciel (aussi appelée architecture logicielle), les diagrammes UML suivants
sont particulièrement utiles :

1. **Diagrammes de cas d'utilisation :** Ils sont utilisés pour représenter l'interaction utilisateur-système à un
   haut niveau en présentant les fonctionnalités clés que le système doit avoir et comment divers utilisateurs
   ou rôles interagissent avec ces fonctionnalités. [PlantUML](https://plantuml.com/en/use-case-diagram)

2. **Diagrammes de composants :** Ils présentent une vue de haut niveau de la façon dont les différents composants ou
   modules d'un système interagissent entre eux, illustrant la structure générale du
   système. [PlantUML](https://plantuml.com/en/component-diagram)

3. **Diagrammes de déploiement :** Ils montrent la disposition physique et la communication entre le matériel, le
   logiciel et les connexions réseau. Ils sont essentiels pour la conception de haut niveau, car ils indiquent où les
   composants logiciels seront déployés. [PlantUML](https://plantuml.com/en/deployment-diagram)

Ces diagrammes fournissent une vue abstraite de haut niveau du système en cours de développement et sont essentiels pour
comprendre comment le système sera construit et comment il interagira avec ses utilisateurs.

## Références

[Cours d'UML](https://laurent-audibert.developpez.com/Cours-UML/)
[PlantUML](https://plantuml.com/en/)