# Git Workflow - Partie II

Source : [NVIE - Vincent Driessen](https://nvie.com/posts/a-successful-git-branching-model/)

## Stratégie de merge

Par défaut git utilise une stratégie qui ne va pas maintenir dans l'historique une vision globale des différentes features branches, supprimant ainsi une partie de l'historique de construction des releases tout comme des hotfixes.

Voici la séquence de commandes réalisées par Git-flow lorsque l'on termine une branche feature

```bash
git flow feature finish <featureName>
```

```bash
$ git checkout develop
Switched to branch 'develop'
$ git merge --no-ff myfeature
Updating ea1b82a..05e9557
(Summary of changes)
$ git branch -d myfeature
Deleted branch myfeature (was 05e9557).
$ git push origin develop
```



> The `--no-ff` flag causes the merge to always create a new commit object, even if the merge could be performed with a fast-forward. This avoids losing information about the historical existence of a feature branch and groups together all commits that together added the feature.

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption><p>Comparaison entre le comportement de la méthode merge (plain vs --no--ff)</p></figcaption></figure>

## Les branches Main et Develop

### Rôles des branches

Dans ce gitflow proposé, deux branches sont particulièrement cruciales pour l'historique global du projet.



| Branche | Rôle                                                                                                                                                                                |
| ------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Main    | Est considérée comme la branche contenant la version "production -ready"                                                                                                            |
|         |                                                                                                                                                                                     |
| Develop | Est considérée comme la branche la plus à jour (HEAD), on la nomme ainsi "integration branch" dans le but de mentionner qu'elle contient les dernières mises à jour fonctionnelles. |

### Mise à jour des branches

Lorsque le code source de la branche develop atteint un point stable et est prêt à être publié, toutes les modifications doivent être fusionnées dans la branche main d'une manière ou d'une autre, puis étiquetées avec un numéro de version.&#x20;

Par conséquent, chaque fois que des changements sont réintégrés dans main, il s'agit par définition d'une nouvelle version de production.&#x20;

En appliquant ces principes de manière rigoureuse nous pourrions utiliser un script Git hook pour construire et déployer automatiquement notre logiciel sur nos serveurs de production à chaque fois qu'il y a un commit sur main.
