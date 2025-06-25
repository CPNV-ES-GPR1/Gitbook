# Gitflow

## Intention

Ce laboratoire a pour intention de vous familiariser avec git-flow. L'idée n'étant pas ici de coder, mais bien de s'entraîner à la technique pure de git et de git-flow.

## Backlog

Réaliser à l'aide de git flow, l'arbre (tree) suivant:

<figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

## Aide

* Débuter avec git-flow

{% embed url="https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow" %}

* En savoir plus sur la convention des commits

{% embed url="https://www.conventionalcommits.org/en/v1.0.0/#summary" %}

* Comment valider l'arbre construit par les commandes git flow ?

```git
[INPUT]
git log --graph --oneline --decorate --all

[OUTPUT]
*   faf7121 (HEAD -> develop) Merge branch 'feature/f2' into develop
|\
| * 4e7623a (feature/f2) test
* | f2345f6 (feature/f1) test
|/
| * ebc5838 (main, hotfix) fix:
|/
* e3a8ed7 chore:
```
