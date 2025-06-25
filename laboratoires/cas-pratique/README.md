# Cas pratique

## Intention pédagogique

Dans ce dernier laboratoire, il s'agit de s'entraîner à l'analyse de situation. En faisant des liens avec les différents principes vus en cours, vous analysez la situation et proposez  des améliorations possibles.

Après une étude spécifique des différentes approches durant ce module, l'idée est de pouvoir appliquer cet ensemble de connaissances sur une même situation pratique.

## Objectifs

Le technicien est entraînée à:

* [ ] Analyser une situation décrivant une équipe et son environnement de travail
* [ ] Identifier les sources de conflits et de freins à la collaboration
* [ ] Identifier les sources d'améliorations possibles pour favoriser le travail au sein de l'équipe
* [ ] Proposer des solutions argumentées à l'aide de bonnes pratiques industrielles
* [ ] Appliquer sur un cas pratique les connaissances des domaines suivants:
  * [ ] Stratégie de branches et de commits (git flow /  conventional commit)
  * [ ] Approche collaboratives (Waterfall, Scrum, Kaban)
  * [ ] <mark style="color:orange;">(Update!)</mark> Adaptation des pratiques (écriture de test, mise en place d'un pipeline CI/CD/CD)

## Situation à étudier

> Il s'agit d'un projet de réécriture d'une application existante de type desktop développée dans un  langage qui ne sera plus maintenu au sein de votre entreprise.\
> \
> L'idée est de transformer cette application en application web pour répondre au besoin de mobilité des utilisateurs finaux.
>
> L'équipe de développement va devoir se familiariser avec le développement web, aussi bien au niveau des technologies que des bonnes pratiques. Le rythme des releases doit passer d'un livrable par année à un livrable par mois.
>
> Initialement l'équipe de développeurs était constituée de 4 membres qui codaient ensemble l'application desktop. Ils ont l'habitude de se renconter à chaque fois que cela est utile. Un tableau "physique" est utilisé pour gérer le travail en cours. 3 nouveaux développeurs vont être recrutés prochainement et l'intention est d'avoir deux équipes, l'une pour le front-end, et l'autre pour le back-end. Le télétravail va également être autorisé dès que le recrutement sera terminé.
>
> Git est bien connu de la part des développeurs, par contre l'habitude actuelle est de travailler tous sur la branche main.

## A faire

En analysant la situation actuelle et la situation future, mettez en évidence les différents challenges collaboratifs et impacts que cela va potentiellement engendrer.

Dresser un plan d'actions pour favoriser une transition (et changement de pratique) qui permettra non seulement d'assurer une maintenance minimale sur l'application actuelle (uniquement des hotfixes) et de progressivement développer la nouvelle application et de prendre les nouveaux besoins. Votre plan d'action doit s'étendre jusqu'au décomissionement d'applicatin Desktop prévu dans 12 mois.

Il est important de mettre en évidence tous les aspects collaboratifs et d'utiliser avec soin les outils et stratégies que nous avons vus en classe.

### Aide

Utiliser un tableau ou un schéma heuristique pourrait vous aider à structure vos idées.

Voici une première réflexion vous permettant de dénouer ce problème:

* Sites différents. Le board "physique" ne peut plus être une option. N'aurions-nous pas besoin de deux boards pour FE et BE. Comment faire pour synchroniser les développements afin de livrer des fonctionnalités "complètes" à notre client ?
* Versionning. Partons-nous sur deux dépôts (un FE, un BE). Peut-être que la structure de branches ne sera pas la même ? Mais comment avoir des versions compatibles en FE-BE ?
* Comment réaliser la transition sur les nouvelles technologies ? Former les nouveaux collaborateurs sur l'ancienne application, jusqu'à quel point ?
* Quel système de gestion d'équipe favoriser ? Laisser la liberté aux développeurs de s'organiser et ne prévoir que des cérémonies pour la mise en commun FE et BE ?
* Un seul interlocuteur avec le client ? Implications du clients durant la phase de migration ?

Temps : 15 minutes (aller à l'essentiel)&#x20;

\
