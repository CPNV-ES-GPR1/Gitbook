# Stratégies de branches

Bibliographie:

* [Atlassian - Comparing Workflows](https://www.atlassian.com/git/tutorials/comparing-workflows)
* [Atlassian - Trunk-based development](https://www.atlassian.com/continuous-delivery/continuous-integration/trunk-based-development)

## Introduction

Git est essentiel dans un projet pour <mark style="color:orange;">gérer efficacement les versions</mark> du code et <mark style="color:orange;">faciliter la collaboration</mark> entre les développeurs.&#x20;

Il permet de <mark style="color:orange;">suivre les modifications</mark>, de revenir à des versions précédentes et d'intégrer du code sans conflits.&#x20;

<mark style="color:orange;">Choisir la bonne stratégie de branches est crucial</mark> pour structurer le développement et éviter le chaos dans la gestion des fonctionnalités.&#x20;

{% hint style="warning" %}
Une bonne stratégie assure un flux de travail fluide, réduit les risques d'erreurs et permet des livraisons plus organisées.
{% endhint %}

## Les différents Workflows

Git est le système de contrôle de version le plus utilisé aujourd'hui. Un Workflow Git est une recette ou une recommandation sur la façon d'utiliser Git pour accomplir un travail de manière cohérente et productive.&#x20;

Les Workflows Git encouragent les développeurs et les équipes DevOps à utiliser Git de manière efficace et cohérente. Git offre une grande flexibilité dans la manière dont les utilisateurs gèrent les changements.&#x20;

{% hint style="warning" %}
Compte tenu de l'accent mis par Git sur la flexibilité, il n'existe pas de processus standardisé sur la façon d'interagir avec Git.
{% endhint %}

Lorsque l'on travaille avec une équipe sur un projet géré par Git, <mark style="color:orange;">il est important de s'assurer que tous les membres de l'équipe sont d'accord sur la façon dont le flux de changements sera appliqué</mark>.&#x20;

Pour s'assurer que l'équipe est sur la même longueur d'onde (pratiques partagées), un workflow Git convenu doit être développé ou sélectionné. Il existe plusieurs Workflow Git publiés qui peuvent convenir à votre équipe.&#x20;

### Le Feature Branching

<mark style="color:orange;">Le Feature Branching est une extension logique du Workflow centralisé</mark>. L'idée de base du workflow Feature Branch est que tous les développements de fonctionnalités doivent avoir lieu dans une branche dédiée plutôt que dans la branche principale.&#x20;

Cette encapsulation permet à plusieurs développeurs de travailler sur une sur une fonctionnalité particulière sans perturber la base de code principale.

### Gitflow Worflow

Gitflow est un Workflow Git hérité qui était à l'origine une stratégie innovante pour la gestion des branches Git.&#x20;

Gitflow peut être utilisé pour <mark style="color:orange;">les projets qui ont un cycle de publication programmé</mark> et pour la meilleure pratique DevOps de livraison continue. Ce workflow n'ajoute pas de nouveaux concepts ou commandes au-delà de ce qui est requis pour le workflow Feature Branch. En revanche, <mark style="color:orange;">il attribue des rôles très spécifiques aux différentes branches et définit comment et quand elles doivent interagir</mark>. En plus des branches de fonctionnalités, il utilise des branches individuelles pour la préparation, la maintenance et l'enregistrement des versions. Bien entendu, vous bénéficiez également de tous les avantages du Feature Branch Workflow : demandes d'extraction, expériences isolées et collaboration plus efficace.

{% hint style="info" %}
Gitflow a perdu en popularité au profit des Workflows basés sur les trunk-based workflows, qui sont maintenant considérés comme les meilleures pratiques pour le développement continu de logiciels modernes et les pratiques DevOps.&#x20;
{% endhint %}

### Trunk-based vs Gitflow

Gitflow a plus de <mark style="color:orange;">branches à durée de vie longue</mark> et <mark style="color:orange;">des commits plus importants</mark> que le développement trunk-based.

Dans ce modèle, les développeurs créent une branche de fonctionnalité et <mark style="color:orange;">retardent sa fusion avec la branche principale jusqu'à ce que la fonctionnalité soit terminée</mark>. Ces branches de fonctionnalités à longue durée de vie nécessitent <mark style="color:orange;">une plus grande collaboration pour les fusionner</mark> car elles présentent un risque plus élevé de s'écarter de la branche principale et d'introduire des mises à jour conflictuelles.

<mark style="color:orange;">Gitflow dispose également de branches primaires distinctes pour le développement, les correctifs, les fonctionnalités et les versions. Il existe différentes stratégies pour fusionner les commits entre ces branches</mark>. Comme il y a plus de branches à jongler et à gérer, il y a souvent plus de complexité qui nécessite des sessions de planification et de révision supplémentaires de la part de l'équipe.

<mark style="color:orange;">Le développement trunk-based est beaucoup plus simplifié</mark> puisqu'il se concentre sur la branche principale en tant que source de corrections et de versions.

{% hint style="info" %}
&#x20;Dans le cadre du développement trunked-base, la branche principale est supposée être toujours stable, sans problème et prête à être déployée.
{% endhint %}

### Forking Workflow

Gitflow a plus de branches à durée de vie longue et des commits&#x20;

Le flux de travail Forking est fondamentalement différent des autres flux de travail Git populaires. <mark style="color:orange;">Au lieu d'utiliser un seul dépôt côté serveur pour agir comme la base de code « centrale », il donne à chaque développeur son propre dépôt côté serveur</mark>.&#x20;

Cela signifie que chaque contributeur ne dispose pas d'un, mais de deux dépôts Git : un dépôt local privé et un dépôt public côté serveur. Le processus de bifurcation est le plus souvent utilisé dans les projets open source publics.





