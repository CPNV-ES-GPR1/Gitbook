# Versioning

## Introduction

Le **versionning** est un système de gestion des versions, permettant de <mark style="color:orange;">suivre les modifications</mark> d’un projet au fil du temps, de <mark style="color:orange;">collaborer efficacement en équipe</mark>, et de <mark style="color:orange;">revenir à des versions antérieures</mark> si nécessaire.

## **Débuts des systèmes de contrôle de version**

* <mark style="color:orange;">**1960s-1980s**</mark> : Les premiers systèmes de contrôle de version sont apparus sur des mainframes et servaient principalement pour des projets internes aux entreprises. Ils étaient souvent rudimentaires et peu adaptés à la collaboration.
* <mark style="color:orange;">**SCCS**</mark>**&#x20;(Source Code Control System, 1972)** : Le SCCS, développé par Bell Labs, est considéré comme l'un des premiers systèmes de gestion de versions. Il permettait de <mark style="color:orange;">stocker les versions successives de fichiers</mark>.
* <mark style="color:orange;">**RCS**</mark>**&#x20;(Revision Control System, 1982)** : L'une des premières évolutions du SCCS, RCS permettait de gérer les versions de fichiers individuels, mais ne facilitait pas encore la gestion de projets complexes.

## **CVS (Concurrent Versions System, 1986)**

* **CVS** est l’un des premiers systèmes à proposer un <mark style="color:orange;">contrôle de version distribué</mark>, permettant à <mark style="color:orange;">plusieurs développeurs de travailler sur un projet en parallèle</mark>. CVS a été largement utilisé dans les projets open source durant les années 1990. Cependant, il avait des limitations, notamment des <mark style="color:orange;">conflits difficiles à gérer</mark> et une <mark style="color:orange;">gestion centralisée des dépôts</mark>.

## **Subversion (SVN, 2000)**

* **SVN** a été développé pour corriger certaines des faiblesses de CVS. Subversion a introduit plusieurs améliorations comme <mark style="color:orange;">la gestion atomique des commits (ce qui signifie que toutes les modifications réussissent ou échouent ensemble)</mark>, une meilleure gestion des renominations de fichiers, et un modèle centralisé plus robuste. SVN est encore utilisé aujourd'hui dans certains projets, mais il est progressivement remplacé par des systèmes distribués comme Git.

## **Mercurial (2005)**

* **Mercurial** est un système de contrôle de version distribué, lancé en 2005 par Matt Mackall. Conçu pour être à la fois <mark style="color:orange;">rapide et léger</mark>, il vise à faciliter la gestion de projets logiciels de grande envergure. Mercurial se distingue par sa simplicité d'utilisation, tout en offrant des fonctionnalités puissantes comme la gestion distribuée. <mark style="color:orange;">Il a été utilisé par des entreprises comme Mozilla</mark>.

## **Git (2005)**

* <mark style="color:orange;">**Git**</mark> <mark style="color:orange;"></mark><mark style="color:orange;">a été créé par</mark> <mark style="color:orange;"></mark><mark style="color:orange;">**Linus Torvalds**</mark> <mark style="color:orange;"></mark><mark style="color:orange;">pour le développement du noyau Linux</mark>, suite à un différend avec un autre système de contrôle de version. Git a transformé la manière dont les projets sont gérés en introduisant un <mark style="color:orange;">modèle totalement distribué</mark>. Chaque développeur possède une copie complète du dépôt, ce qui permet de travailler hors ligne. Git est particulièrement <mark style="color:orange;">puissant pour la gestion des branches et des fusions</mark>, et est devenu de facto le standard pour le développement logiciel open source et commercial.

### **Popularisation avec GitHub (2008)**

* **GitHub** est une plateforme de collaboration en ligne basée sur Git, lancée en 2008. Elle a grandement contribué à populariser Git, <mark style="color:orange;">en ajoutant une interface conviviale et des fonctionnalités sociales pour faciliter le partage de projets open source</mark>. D'autres plateformes similaires, comme <mark style="color:orange;">GitLab</mark> et <mark style="color:orange;">Bitbucket</mark>, se sont également développées.

### **Évolution récente et adoption massive**

* Aujourd'hui, **Git** domine largement l'écosystème des outils de versionnement, tant pour les projets open source que pour les entreprises. D’autres systèmes comme **Mercurial** et **SVN** sont encore utilisés, mais dans une moindre mesure.
* Des outils modernes comme **GitLab**, **Bitbucket**, et **Azure DevOps** fournissent <mark style="color:orange;">des intégrations continues (CI/CD), la gestion des tickets et d'autres fonctionnalités autour de Git, rendant le versionnement encore plus central dans les processus de développement</mark>.

## Conclusion

Le versionning a évolué <mark style="color:orange;">d’un simple outil de gestion de versions à un système collaboratif</mark> central au processus de développement logiciel moderne. Git et Mercurial ont marqué un tournant en passant à des modèles distribués, tandis que GitHub et autres plateformes similaires ont facilité l’adoption massive du versionnement dans le monde entier.
