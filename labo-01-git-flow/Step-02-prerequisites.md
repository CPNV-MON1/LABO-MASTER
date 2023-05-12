# Prerequisites

## Setting up/updating the git environment and git flow

[Get the installer](https://git-scm.com/downloads)

{% hint style="info" %}
Git-flow library:\
For Windows, is natively integrated.\
For Mac, [here is the procedure](https://git-scm.com/download/mac).\
Pour Linux, [here is the procedure.](https://howtoinstall.co/en/git-flow)
{% endhint %}


## Environement Windows 11

```
[INPUT]
git flow version

[OUTPUT]
1.12.3 (AVH Edition)
```

* [ ] Confirm the installed version

```
[INPUT]
git flow version

[OUTPUT]
1.12.3 (AVH Edition)
```

* [ ] What do you think about this release?

```
une version mineure avec quelques corrections de bogues et améliorations incluses dans l'édition AVH de Git.
```

## What's git-flow, branches feature.

[Source](https://nvie.com/posts/a-successful-git-branching-model/)

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption><p>Source : A successful git branching model</p></figcaption></figure>

* [ ] Which branches are persistent and what do they contain?

```
master : le projet qui est en production
develop : le projet qui est en cours de dévelopement, ensuite il va dans une branche où il se fait tester. Si des bugs sont trouvés, il retourne en develop si tout fonctionne correctement il va en master (production)
```

* [ ] Why do we have to merge hotfix in both master and develop branches, but not into all active feature branches?

```
Parce ce que nous devons corriger les erreus des 2 côtés. Incorporé les correctifs dans develop et dans master. Pour pouvoir continuer à travailler sur le projet d'actualité avec les correctifs appliqués. Pour que les développement futur soient effectué sur la bonne version.
```

## Initialize git flow on an existing project

* [ ] What happens when you run the "git flow init" command on an existing local repository?

```
Lorsque vous exécutez la commande git flow init sur un dépôt local existant, Git Flow vous demande de spécifier les noms des branches à utiliser pour la branche principale de développement, les branches de fonctionnalités, les branches de versions et les branches de correctifs.
```

* [ ] When do we need to make this git command?

```
Afin de gérer les branches d'un projet existant.
```

## Practice the basic git commands

[Source](https://www.atlassian.com/git/glossary)

* [ ] What does this git command "git add -all" achieve (.gitignore impacts)?

```
La commande git add --all ajoute toutes les modifications au stockage, y compris les fichiers non suivis, les fichiers modifiés et les fichiers supprimés.
```

* [ ] What does this git command "git status" achieve?

```
La commande git status permet d'afficher l'état actuel du dépôt Git. Lorsque vous lancez la commande git status, Git affiche des informations sur les fichiers du dépôt, notamment les fichiers qui ont été modifiés, ceux qui sont en attente du prochain commit et ceux qui ne sont pas suivis par Git.
```

* [ ] What does this git command "git remote add upstream \<url>" achieve?

```
La commande git remote add upstream <url> est utilisée pour ajouter un nouveau dépôt distant à votre dépôt Git local. Le terme "upstream" est souvent utilisé pour faire référence au dépôt original à partir duquel votre dépôt local a été forké.
```
