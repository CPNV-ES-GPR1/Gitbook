# Les commits

* [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)

## Introduction

La spécification Conventional Commits est <mark style="color:orange;">une convention légère</mark> qui s'applique aux messages de commit. Elle fournit un ensemble de règles simples pour créer un historique de commit explicite, ce qui facilite l'écriture d'outils automatisés. Cette convention s'aligne sur SemVer, en décrivant les fonctionnalités, les corrections et les changements majeurs apportés dans les messages de commit.

Le message de commit doit être structuré comme suit :

```git
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

## Les préfixes

Le commit contient les éléments structurels suivants, afin de communiquer l'intention aux utilisateurs de vos sources :

<table><thead><tr><th width="197.08331298828125">Préfixes</th><th>Explication</th></tr></thead><tbody><tr><td>fix</td><td>un commit de type fix corrige un bug dans votre base de code (ceci correspond à PATCH dans le versionnement sémantique).</td></tr><tr><td>feat</td><td>un commit de type feat introduit une nouvelle fonctionnalité dans la base de code (ceci correspond à MINOR dans le versionnement sémantique).</td></tr><tr><td>BREAKING CHANGE</td><td>un commit qui comporte le pied de page BREAKING CHANGE: ou qui ajoute un ! après le type/la portée introduit une modification majeure de l'API (correspondant à MAJOR dans le versionnement sémantique). Un BREAKING CHANGE peut faire partie de commits de tout type.</td></tr></tbody></table>

Les autres types de préfixes sont également autorisés (basé sur la convention Angular):

<table><thead><tr><th width="201.66668701171875">Préfixes</th><th>Explication</th></tr></thead><tbody><tr><td>build</td><td></td></tr><tr><td>chore</td><td></td></tr><tr><td>ci</td><td></td></tr><tr><td>docs</td><td></td></tr><tr><td>style</td><td></td></tr><tr><td>refactor</td><td></td></tr><tr><td>perf</td><td></td></tr><tr><td>test</td><td></td></tr></tbody></table>

Des pieds de page autres que BREAKING CHANGE: peuvent être fournis et suivre une convention similaire au format git trailer.
