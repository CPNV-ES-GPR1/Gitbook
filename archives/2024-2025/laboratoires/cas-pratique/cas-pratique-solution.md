# Cas pratique - Solution

## Stratégie - Approche à favoriser

* [ ] Produire, après une ou deux lectures, un résumé de la situation.
* [ ] Mettre en évidence les informations utiles par catégorie (travail collaboratif, pratique de développement, gestion des versions). Un tableau ou un schéma.
* [ ] Proposer un plan d'action et des actions concrètes.

### Résumé

Il s'agit d'une situation a priori saine. Les changements qui sont demandés découlent de futurs changements impactant tous les axes d'étude demandés.

Les développeurs sont expérimentés, mais on également de nombreuses habitudes spécifiques à leur projet.

Le changement risque de déstabiliser -temporairement- l'équilibre de l'équipe et certains la stabilité du produit.

L'intégration de nouvelle technologie ainsi que de nouveaux collaborateurs sont les éléments clés à traiter.

### Tableau - Informations utiles



<table data-full-width="true"><thead><tr><th>Informations</th><th>Impacts - travail collaboratif</th><th>Impacts - Versioning</th><th>Impacts - Pratiques</th></tr></thead><tbody><tr><td>Réécriture d'une application desktop en web</td><td>-</td><td>Comment faire cohabiter ancienne et nouvelle version ?<br><br>Une branche unique est d'office impossible.<br><br>Plusieurs dépôts, plusieurs branches ?</td><td>Apprentissage d'une nouvelle technologie pour les développeurs.</td></tr><tr><td>Changement du rythme de release (annuel vs mensuel)</td><td>Le cycle plus court de livrables va déstabiliser le rythme actuel des équipes.</td><td>Augmentation du nombre de release, de version.<br><br>Une stratégie de release doit être mise en place.<br></td><td>Pratiques du code en lien avec les tests automatique et le déploiement automatique (CI/CD/CD)<br><br>Le type de déploiement sera également totalement différent. (desktop -> chaque poste, web -> 1 serveur web + incompatiblité navigateurs)</td></tr><tr><td>Travail à distance et équipe décentralisée</td><td>Le board physique doit être numérisé pour pouvoir le consulter et le modifier à distance.<br><br>Une solution de communication à distance doit être envisagée.</td><td>Comment discuter sur un même code, à distance ?</td><td>-</td></tr><tr><td>Plusieurs équipes, plusieurs produits.</td><td>Des ressources seront allouées au maintient de la solution actuelle.<br><br>Des ressources seront allouées aussi bien pour le FE que pour le BE.<br><br>Rythme de travail désyncrhonisé entre les équipes.</td><td>Trois système de version nécesssaire pour l'ancien app, le FE et le BE.</td><td>Comment faire cohabiter les nouvelles pratiques avec les anciennes ?</td></tr></tbody></table>



## Décisions et plan d'action

### Travail collaboratif

Un plan d'action détaillé ne fait pas de sens car les inconnues sont trop nombreuses. Il s'agit donc de prioriser les premières étapes uniquement (condition pour du Waterwall ne sont pas présentes). Une approche Kanban, qui semble une approche déjà mise en place “naturellement”, ne pourra pas être maintenue en l’état car nous avons un cycle de livrable plus court et imposé.&#x20;

Un modèle Scrum semble devoir être favorisé pour itérer au rythme voulu par le client. Je favorise donc une transition des pratiques collaboratives en partant des habitudes actuelles (flux continue de travail) en ajoutant l'itération, le sprint. Ceci que pour la nouvelle application uniquement.&#x20;

Je préconise également d'informer le client que durant le premier sprint (que je dimensionnerai à 4 semaines vu le nombre de pratique à changer), nous serons sur une phase de formation et que la plus-value métier ne sera pas au rendez-vous. Je sensibiliserai également le client qu’un deuxième sprint zéro pourra certainement être nécessaire. On le saura après avoir recruté et entraîné les équipes pendant 4 semaines.

Pour l'intégration des nouveaux collaborateurs, je préconise de recruter des profils qui sont familiarisés avec les technologies et les nouvelles pratiques que l'on désire mettre en oeuvre. Ainsi nous pourrons engager une collaboration croisée au sein de laquelle les "anciens" dév réaliseront le transfert de compétence métier et en retour seront formés sur les nouvelles technologies.&#x20;

Itération après itération cela réduira ainsi les différences de compétences et nous tendrons vers un principe Scum important, l'interdisciplinarité. Chacun sera ainsi valorisé sur ces compétences car il ne s’agit pas de perdre les développeurs actuels.

J'intégrerai ainsi progressivement des cérémonies. Le Daily doit être planifié. Il s'ajoute aux rencontres spontanées déjà présentes dans la culture de l'entreprise. Et viendront ensuite le sprint planning, la review et la retrospective, mais ceci uniquement pour le nouveau projet.&#x20;

La rédaction du backlog devra se faire en équipe entre les anciens et les nouveaux développeurs. Les nouveaux développeurs connaissant les pratiques Scrum, et les anciens le métier.&#x20;

Tant que nous n'aurons pas de nouvelles fonctionnalités, l'implication du client doit rester sur l'ancienne applicaiton. Les premiers meetings ne vont certainement ne rien apporter au client, mais la porte reste ouverte.

### Gestion de version

La situation actuelle semble fonctionner pour l'application desktop. Je ne vois pas l'intérêt de modifier les pratiques. D'autant plus qu'il s'agit de notre version en production, sensible. Les end-users ne doivent pas être impactés, stressés par nos changements internes.

Pour ce qui est de la nouvelle application ainsi que des nouveaux collaborateurs, je préconise dès le début de la réécriture du code d'appliquer les pratiques de branches, de commit, et d'écriture de tests. J'y reviendrai dans la partie "pratique de développement".

Pour ce qui est du modèle de branches, je favorise git flow tout en sachant que dans un premier temps le modèle sera plus simple. Aucun hotfix par exemple.&#x20;

Cela étant, dit je garderai la porte ouverte à un modèle plus souple car l'équipe est petite et la mise en place des tests et de la CI/CD/CD risque d’être freinés par trop de branches.&#x20;

Je ne négocierai par contre pas sur le fait que nous devons avoir trois versions distinctes. L'application actuelle, et un projet consitué de soit de deux dépôts, un pour FE et BE soit une approche mono-repo (que nous n'avons pas encore vue) qui est également bien vu étant donné le niveau de dépendance forte entre notre FE et notre BE.&#x20;

Si le BE devait ensuite devenir un produit à part entière, chacun avec son cycle de vie, alors des dépôts séparés seraient justifiés pleinement entre FE et BE.

### Pratique de développement

Comme mentionné précédemment, je ne changerai rien aux pratiques sur l'ancien projet. Aucune plus-value pour les end-users avec un risque de déstabiliser des processus qui sont en place et qui ont fait leur preuve.

Pour la nouvelle application, j'investirai dès le début beaucoup d'énergie sur la mise en place des tests pour garantir que lors du passage en production de la première version, nous grantissant la même couverture fonctionnelle que l'application desktop.

J’impliquerai les anciens développeurs dans la validation des classes et scénarios de tests pour qu’ils puissent faire le lien entre la rédaction du backlog et le résultat obtenu grâce aux nouvelles pratiques.

### En plus

Je ne traite pas le décommissionnement de l'ancienne application, même si je tenterai de faire un passage "d'un coup". Laissant l'ancienne version en consultation, mais bloquant la modification dès la mise en place de la nouvelle application.

Pour la mise en place de l'infrastructure, il est bien trop tôt pour en parler. Mais nous devrons revoir les responsabilités concernant l'infrastructure hébergeant l'application web.

Il sera également important d'intégrer au bon moment les end-users. Mais il est trop tôt pour en parler.\
