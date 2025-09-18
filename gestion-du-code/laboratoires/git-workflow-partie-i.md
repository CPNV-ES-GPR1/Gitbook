# Git Workflow - Partie I

## Préambule

### Main ou master ?

Source : [TheServerSide](https://www.theserverside.com/feature/Why-GitHub-renamed-its-master-branch-to-main)

Afin de respecter la sensibilité "historique" que porte l'utilisation des termes "master and slave", très répandu dans le domaine informatique, Github a pris des mesures sur les conseils du "Software Freedom Conservancy" afin de favoriser l'utilisation d'une branche "main" au lieu de "master.

Dans ce gitbook, nous gardons l'image original représentant le gitflow (qui mentionnne master). Le texte d'accompagnement a été mis à jour afin d'utiliser main. Il s'agit, d'un point de vue gitflow, de considérer main et master comme ayant le même rôle.

## A successful Git Workflow

Source : [NVIE](https://nvie.com/posts/a-successful-git-branching-model/)

{% embed url="https://nvie.com/img/git-model@2x.png" %}

## Questions d'analyse

* [ ] Quelles sont les branches qui sont persistentes ?
* [ ] Pourquoi injecter aussi bien du contenu en develop et en main lors de publication d'un hotfix ?
* [ ] L'intérêt de la branche develop ?
* [ ] Planifier une release alors que certaines features sont encore ouvertes... à quoi doit-on s'attendre lors de la prochaine release ?
* [ ] Quelle la branche "d'origine" de toutes les branches "feature" ?
* [ ] A quel instant du gitflow, les features vont-elles recevoir un éventuel hotfix ?

## Et si on regardait un peu les commandes ?

{% embed url="https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow" %}

## Dépôt d'entrainement

{% embed url="https://github.com/CPNV-ES-GPR1/Eval-Gitflow-Specs" %}
