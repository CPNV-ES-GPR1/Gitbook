# Pipeline CI-CD-CD

Bibliographie:

* [Pipeline CI/CD/CD - REDHAT](https://www.redhat.com/en/topics/devops/what-is-ci-cd)
* [Automatisation - REDHAT](https://www.redhat.com/en/topics/automation?cicd=32h281b)
* [DEVOPS - Atlassian](https://www.atlassian.com/devops)

## Introduction

Le pipeline CI-CD-CD <mark style="color:orange;">automatise</mark> la création, les tests et la livraison des logiciels, tout en facilitant la collaboration entre les équipes de développement et d'opérations (DEVOPS).&#x20;

Il vérifie le code pour détecter des erreurs et déploie les modifications <mark style="color:orange;">sans intervention manuelle</mark>.&#x20;

Grâce à cette automatisation, <mark style="color:orange;">les équipes collaborent plus efficacement, accélérant les livraisons tout en réduisant les risques d'erreurs humaines</mark>.&#x20;

Le processus assure ainsi une intégration fluide et continue des modifications tout en [<mark style="color:orange;">accélérant le cycle de vie</mark>](#user-content-fn-1)[^1][ ](#user-content-fn-1)[^1]du développement des logiciels.



{% hint style="info" %}
Quels sont les facteurs qui influencent le cycle de vie d'un logiciel ?
{% endhint %}

## Vue d'ensemble

La pratique de l'intégration continue ([CI - Continous Integration](pipeline-ci-cd-cd.md#continous-integration)) consiste à intégrer  automatiquement et régulièrement les modifications de code dans un référentiel de code source partagé.

La distribution et/ou le déploiement continus ([CD - Continous Delivery + CD - Continous Deployment](pipeline-ci-cd-cd.md#continous-delivery) ) désignent quant à eux un processus en deux volets qui englobe:

* l'intégration, les tests et,
* la distribution des modifications apportées au code.

La distribution continue se limite au déploiement automatique dans les environnements de production, alors que le déploiement continu publie automatiquement les mises à jour dans ces environnements.

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption><p>Source : <a href="https://www.redhat.com/en/topics/devops/what-is-ci-cd">RedHat</a></p></figcaption></figure>

Ensemble, ces pratiques sont souvent désignées par l'expression « pipeline CI/CD » et elles reposent sur une collaboration agile entre les équipes de développement et d'exploitation, que ce soit dans le cadre d'une approche [DevOps](https://www.redhat.com/fr/topics/devops?cicd=32h281b) ou d'[ingénierie de la fiabilité des sites (SRE)](https://www.redhat.com/fr/topics/devops/what-is-sre?cicd=32h281b).

{% embed url="https://www.atlassian.com/devops" %}

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption><p>Source :<a href="https://www.atlassian.com/fr/devops"> Atlassian</a></p></figcaption></figure>

{% embed url="https://www.redhat.com/en/topics/devops/what-is-sre?cicd=32h281b" %}

{% embed url="https://www.redhat.com/en/topics/devops/what-is-sre?cicd=32h281b#devops-vs-sre" %}

{% hint style="info" %}
Ces systèmes, aussi bien le devops que le SRE, ne sont-ils pas pertinents uniquement pour des entreprises de tailles internationales ?
{% endhint %}

### Importance du Pipeline CI/CD/CD

À mesure que les applications évoluent, <mark style="color:orange;">les fonctions de CI/CD peuvent réduire la complexité, accroître l'efficacité et rationaliser les flux de travail</mark>.

Grâce à l'automatisation des interventions manuelles généralement nécessaires à la mise en production d'un nouveau code, <mark style="color:orange;">les temps d'arrêt sont limités</mark> et les publications de code sont plus rapides. Par ailleurs, en accélérant l'intégration des mises à jour et des modifications du code, <mark style="color:orange;">vous accélérez également celle des commentaires des utilisateurs</mark>.&#x20;

{% hint style="info" %}
Quelle est la condition -sine qua non- pour une adoption d'un pipeline CI/CD/CD par vos équipes ?
{% endhint %}

### Continous Integration

Dans l'acronyme CI/CD/CD, le terme « CI » désigne toujours l'intégration continue. Ce processus d'automatisation destiné aux équipes de développement facilite la fusion plus fréquente des modifications de code <mark style="color:orange;">vers une branche partagée</mark>.&#x20;

Au fur et à mesure de ces mises à jour, <mark style="color:orange;">des phases de tests automatisés</mark> se lancent afin de garantir la fiabilité des modifications du code fusionné.

Le concept de développement d'applications modernes consiste à faire <mark style="color:orange;">travailler plusieurs développeurs simultanément sur différentes fonctions d'une même application</mark>.&#x20;

Une intégration continue est <mark style="color:orange;">efficace quand les modifications apportées à une application sont validées par la compilation automatique de l'application et l'exécution de différents niveaux de tests automatisés</mark>. Il s'agit de s'assurer que les modifications n'ont pas compromis l'application, notamment au moyen de <mark style="color:orange;">tests unitaires et d'intégration</mark>.&#x20;

<mark style="color:orange;">Il faut donc tout tester</mark>, des classes aux fonctions, en passant par les différents modules qui composent l'application. Si les tests automatisés révèlent un conflit entre le nouveau code et le code existant, l'intégration continue accélère la correction de ces bogues, à une fréquence plus régulière.

### Continous Delivery (Distribution continue)

La distribution continue automatise la publication du code validé dans un référentiel suite à l'automatisation des versions et des tests unitaires et d'intégration dans le cadre de l'intégration continue. Ainsi, pour obtenir un processus de distribution continue efficace, <mark style="color:orange;">il est essentiel de l'intégrer dès le départ dans votre pipeline de développement.</mark>

La distribution continue <mark style="color:orange;">implique une automatisation des tests et des publications de code à chaque étape</mark>, du fusionnement des modifications de code à la distribution des versions prêtes pour la production.&#x20;

À l'issue de ce processus, l'équipe d'exploitation est à même de déployer rapidement une application en production.

### Continous Deployment

Le déploiement continu constitue la dernière étape d'un pipeline CI/CD mature. Prolongement de la distribution continue, il peut désigner le transfert automatique des modifications depuis le référentiel vers l'environnement de production, où elles peuvent être utilisées par les clients.

{% hint style="info" %}
Dans ce contexte, voyez-vous la plus value de la virtualisation, notamment la conteneurisation ?
{% endhint %}

<mark style="color:orange;">Le déploiement continu traite le problème de la surcharge des équipes d'exploitation par des processus manuels qui ralentissent la distribution des applications</mark>. Il s'appuie sur les bénéfices de la distribution continue pour automatiser l'étape suivante du pipeline.

Dans la pratique, dans le cadre du déploiement continu, une modification apportée à une application cloud pourrait être publiée quelques minutes seulement après la rédaction du code en question (en supposant qu'elle passe les tests automatisés).

En revanche, comme aucun contrôle manuel n'intervient à l'étape qui précède la mise en production, <mark style="color:orange;">le déploiement continu mise en grande partie sur une automatisation bien pensée des tests</mark>.&#x20;

{% hint style="warning" %}
En conclusion, cette pratique peut exiger un investissement initial conséquent, puisqu'elle implique l'élaboration de tests automatisés pour différentes étapes de test et de mise en production au sein du pipeline CI/CD.
{% endhint %}





[^1]: 
