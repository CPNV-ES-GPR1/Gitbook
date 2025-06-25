# Gitflow - Solution

Voici une palette de commandes git vous permettant d'évaluer votre travail et de construire votre documentation pour l'évaluation et vos futurs projets.

Note : il existe de nombreuses documentations en lignes bien plus complètes et détaillées que cette simple page. Cette dernière n'est là que pour vous "lancer" et vous éviter le découragement des premières tentatives.

## Initalisation d'un dépôt local

```bash
git init
```

```
# Résultat attendu
* le répertoire .git est créé
drwxr-xr-x 1 197121 0 Sep 24 18:18 .git/
```

Note : il est également possible de directement réaliser un "git flow init" ce qui va initialiser le dépôt si besoin. Attention cependant, vous vous retrouverez sur la branche develop après cela.

## Intégrer le premier commit contenant le readme et le .gitignore

```bash
touch readme .gitignore
git add .
git commit -m "chore:"
```

```
# Résultat attendu
[main (root-commit) 7461a8c] chore:
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 .gitignore
 create mode 100644 readme

Exécuter la commande "git log" et valider que le "chore" est présent
```

{% hint style="info" %}
Le paramètre "all" de la commande "git add --all" est prioritaire sur un éventuel .gitignore. A utiliser avec grande prudence.
{% endhint %}

## Initialiser git flow

```
git flow init
```

```bash
# Git flow affiche les différentes settings possibles
Which branch should be used for bringing forth production releases?
   - main
Branch name for production releases: [main]
Branch name for "next release" development: [develop]

How to name your supporting branch prefixes?
Feature branches? [feature/]
Bugfix branches? [bugfix/]
Release branches? [release/]
Hotfix branches? [hotfix/]
Support branches? [support/]
Version tag prefix? []
Hooks and filters directory? [C:/Users/Glassey Nicolas/Desktop/tutoGit/.git/hooks]

# Je suis ensuite redirigé sur la branche develop
git branch
* develop
  main
```

## Gestion des branches

* [Documentation Atlassian pour Git Flow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow). Etudier avec soin les trois chapitres suivants:
  * Gestion d'une branche release
  * Gestion d'une branche hotfix
  * Gestion d'une branche feature

## Cas particuliers d'ajout de fichier

### Cas 1 - Renommer une branche

Il peut être nécessaire de renommer une branche, par exemple la branche master en main.

```bash
git branch -m main
```

{% code overflow="wrap" %}
```
# Résultat attendu
* en notant que nous étions sur la branche master pour paser la commande
En fonction de votre client cmd, vous aurez une annotion
mentionnant sur quelle branche vous vous situez.

Attention. Si votre dépôt est vide, la commande "git branch" ne retournera rien car il n'y a pour l'instant aucun commit.
```
{% endcode %}

### Cas 2 - Ajout d'un contenu par erreur en réalisant "git add ."

* Observer l'état du dépôt local

```bash
git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   BadFile      //le fichier à retirer
        new file:   GoodFile    //le fichier à garder
```

* Retirer le fichier "BadFile" du prochain commit (stage)

```
git restore --staged BadFile
```

* Valider que le résultat attendu

```
git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   GoodFile    //il est toujours là !

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        BadFile                 //il a bien été retiré du "stage"

```

## Conseils

* [ ] Favoriser l'utilisation de la ligne de commande pour entraîner git.
* [ ] Sur-utiliser sans gène la commande "git status" avant et après vos commandes pour valider/invalider le résultat.
* [ ] Avant de passer une commande, soyer au clair sur le résultat attendu.
