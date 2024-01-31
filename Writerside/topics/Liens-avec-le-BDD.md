# Liens avec le BDD

Le BDD (_Behavior-Driven Development_, ou développement piloté par le comportement) est une pratique de développement de
logiciels qui encourage la collaboration entre développeurs, QA et non-techniciens ou parties prenantes commerciales
dans un projet logiciel. Il se concentre sur la réalisation de l'objectif du comportement des fonctionnalités d'un
produit logiciel.

Les _user stories_ fournissent une description simple et compréhensible des exigences pour une fonctionnalité
particulière d'un produit logiciel du point de vue de l'utilisateur final.

Le lien entre les _user stories_ et BDD devient manifeste au niveau des scénarios d'acceptation. Ces scénarios reflètent
comment une fonctionnalité donnée devrait se comporter pour être considérée comme satisfaisante pour l'utilisateur
final. Ils aident à clarifier les exigences et font également souvent office de test d'acceptation.

Dans BDD, ces scénarios sont exprimés sous la spec BDD "Given, When, Then" format qui ressemble à ceci :

- **Étant donné (Given)** (état initial du système)
- **Quand (When)** (une action effectuée par l'utilisateur)
- **Alors (Then)** (le résultat attendu de l'action)

Par exemple, en utilisant la _user story_ précédente :

```
En tant que client, je veux pouvoir me connecter au site avec Facebook afin de faciliter le processus de connexion.
```

Un scenario BDD pour cela pourrait être formulé comme suit :

```
Étant donné  que je suis un client visitant la page de connexion
Quand        je clique sur l'option "Se connecter avec Facebook"
Alors        je devrais être redirigé vers la page de connexion Facebook
Et           après une connexion réussie, je devrais être redirigé vers le site et être connecté.
```

En résumé, les _user stories_ et BDD sont étroitement liés. **Les _user stories_ aident à définir la fonctionnalité et
les scénarios BDD déterminent le comportement attendu de cette fonctionnalité**.
