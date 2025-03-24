# Jour-06

## 🚀 Le Principe d'une Pull Request (PR)

### 📌 Qu'est-ce qu'une Pull Request ?
Une **Pull Request (PR)** est une demande de fusion de modifications entre deux branches d'un dépôt Git, souvent depuis une branche de fonctionnalité (`feature-branch`) vers la branche principale (`main` ou `develop`).

Elle permet :
- Une **relecture du code** par d'autres développeurs.
- Une **validation avant intégration** pour éviter les bugs.
- Un **historique clair des modifications**.

---

## Comprendre `git rebase` et `git merge` dans Git

### Qu'est-ce que `git rebase` ?

`git rebase` est une commande qui permet de **réécrire l'historique d'une branche** en déplaçant la base de cette branche vers un autre commit. Cela permet de rendre l'historique plus linéaire et plus facile à lire, car il évite de créer des commits de fusion qui peuvent encombrer l'historique.

En d'autres termes, **le rebase rejoue les commits de ta branche au-dessus d'une autre branche**. Cela fait en sorte que l'historique semble comme si les changements étaient faits dans un ordre linéaire, plutôt que d'être fusionnés.

## Fonctionnement de `git rebase`

### Exemple typique :
Imaginons deux branches : `main` et `feature`.

- Sur la branche `main`, tu as plusieurs commits : `A`, `B`, `C`.
- Sur la branche `feature`, tu as quelques commits : `D`, `E`.

        A---B---C (main)
        D---E (feature)

Lorsque tu fais un **rebase** de la branche `feature` sur `main`, Git va prendre les commits `D` et `E` et les réappliquer après le commit `C` de `main`.


        A---B---C---D'---E' (feature)

### Quand utiliser `git rebase` ?

- Avant de fusionner une branche dans main ou develop :

    Utiliser rebase avant de fusionner ta branche de fonctionnalité dans la branche principale rend l'historique plus propre et plus facile à suivre.
    Cela permet aussi d'éviter d'ajouter des commits de fusion dans l'historique principal.

- Lorsqu'il n'y a pas de travail partagé avec d'autres :

    **rebase** réécrit l'historique, donc il est plus sûr de l'utiliser sur des branches locales avant qu'elles ne soient partagées avec d'autres utilisateurs. Si la branche a été poussée sur un dépôt distant et utilisée par d'autres, cela peut entraîner des conflits et des pertes de données.

---

## Différence entre `git switch` et `git checkout`

### 1. **`git checkout`**

La commande **`git checkout`** est plus ancienne et sert à plusieurs choses dans Git :
- **Changer de branche** : `git checkout <nom_de_branche>`
- **Restaurer des fichiers** à partir d'un commit spécifique : `git checkout <commit_id> -- <fichier>`
- **Créer et basculer sur une nouvelle branche** : `git checkout -b <nom_de_nouvelle_branche>`

#### Inconvénient :
- **Polyvalente mais ambiguë** : Elle peut être utilisée pour différentes opérations, ce qui la rend parfois déroutante pour les débutants.

### 2. **`git switch`**

La commande **`git switch`** a été introduite dans Git 2.23 (2019) pour simplifier l'action de changer de branche. Elle se concentre uniquement sur cette tâche spécifique.

- **Changer de branche** : `git switch <nom_de_branche>`
- **Créer et basculer sur une nouvelle branche** : `git switch -c <nom_de_nouvelle_branche>`

#### Avantage :
- **Plus simple et plus claire** : Cette commande est spécifique au changement de branche, ce qui la rend plus intuitive et facile à utiliser.

### Comparaison

| **Fonctionnalité**               | **`git checkout`**                       | **`git switch`**                     |
|----------------------------------|------------------------------------------|--------------------------------------|
| **Changer de branche**           | Oui (`git checkout <nom_de_branche>`)    | Oui (`git switch <nom_de_branche>`)  |
| **Créer une nouvelle branche**   | Oui (`git checkout -b <nom_de_branche>`) | Oui (`git switch -c <nom_de_branche>`) |
| **Restaurer des fichiers**       | Oui (`git checkout <commit_id> -- <fichier>`) | Non                                  |
| **Clarté et simplicité**         | Moins claire (polyvalente)               | Plus claire et spécifique au changement de branche |

### Conclusion

- **Utiliser `git switch`** pour changer de branche ou en créer une nouvelle, c'est plus simple et plus clair.
- **Utiliser `git checkout`** pour des fonctionnalités plus avancées, comme restaurer des fichiers à partir d'un commit.

## Le Fast Forward Merge dans Git

### Qu'est-ce que le Fast Forward ?

Le **fast forward** est un type de fusion dans Git qui se produit lorsqu'une branche peut être avancée sans qu'un commit de fusion soit nécessaire. Cela arrive lorsque la branche cible n'a pas de nouveaux commits depuis le dernier point de divergence, et la branche source est simplement une extension de la branche cible.

### Quand se produit un Fast Forward ?
Un **fast forward merge** se produit lorsque :
- La branche cible n'a pas de commits après le point de divergence avec la branche source.
- La branche source contient tous les commits nécessaires pour "rattraper" la branche cible.

Git avance simplement le pointeur de la branche cible pour inclure tous les commits de la branche source, sans créer de commit de fusion.



## `commit` et `merge commit`

- **Commit** :
    - Enregistre des changements dans les fichiers (modifications de code, ajout de fichiers, etc.).
    - A un seul parent.
    - Crée un historique linéaire.

- **Merge Commit** :
    - Crée un point de jonction entre deux ou plusieurs branches.
    - A deux ou plusieurs parents (les branches fusionnées).
    - N'enregistre pas de nouvelles modifications, mais marque la fusion dans l'historique du projet.

## Conclusion

Un **commit** est une unité de travail qui enregistre des modifications dans l'historique de la branche, tandis qu'un **merge commit** est un commit spécial qui enregistre une fusion de deux branches, avec plusieurs parents et un historique de fusion plus complexe.


## Commande `git fetch --prune`

### Qu'est-ce que `git fetch --prune` ?

La commande `git fetch --prune` est utilisée pour nettoyer les références distantes obsolètes dans ton dépôt local. Elle permet de supprimer les branches distantes qui ont été supprimées sur le serveur distant (par exemple, sur GitHub, GitLab, etc.).

### Fonctionnement

- **`git fetch`** : La commande `git fetch` récupère les dernières mises à jour du dépôt distant. Cela inclut les nouvelles branches, les tags et autres informations. Cependant, elle ne supprime pas automatiquement les branches distantes locales qui ont été supprimées sur le serveur distant.
  
- **`--prune`** : L'option `--prune` permet de nettoyer les références de branches distantes qui n'existent plus sur le serveur distant. Cela va supprimer localement les branches distantes obsolètes, c'est-à-dire celles qui ont été supprimées du dépôt distant.

## `.gitignore` Global ou Local ?

### Qu'est-ce qu'un `.gitignore` ?

Un fichier `.gitignore` permet de spécifier les fichiers et dossiers que Git doit ignorer. Cela permet de ne pas suivre certains fichiers dans le contrôle de version (ex. : fichiers temporaires, logs, dépendances, etc.).

### `.gitignore` Global vs Local

- **.gitignore Local** : C'est un fichier `.gitignore` spécifique à un projet. Il est situé dans le répertoire racine du dépôt et contient les règles d'ignorance pour ce projet en particulier. Chaque projet peut avoir son propre fichier `.gitignore` pour s'assurer qu'il ignore les fichiers ou dossiers non pertinents pour ce projet.
  
- **.gitignore Global** : Un fichier `.gitignore` global est utilisé pour ignorer des fichiers spécifiques à l'utilisateur à travers tous les projets Git de cet utilisateur. Cela est utile pour ignorer des fichiers qui sont générés par l'IDE, des fichiers de configuration ou des fichiers temporaires qui peuvent apparaître dans plusieurs projets. Par exemple, si tu utilises un éditeur de code qui crée toujours un fichier `.vscode/` ou `.idea/`, tu peux les ajouter à un `.gitignore` global pour ne pas les ajouter dans chaque projet.

### Comment configurer un `.gitignore` global ?

1. Crée un fichier `.gitignore` global (par exemple, `~/.gitignore_global`).
2. Ajoute des règles pour ignorer des fichiers ou des dossiers communs dans tous les projets.
3. Configure Git pour utiliser ce fichier global avec la commande :

   ```bash
   git config --global core.excludesfile ~/.gitignore_global

    *.log
    *.swp
    .vscode/
    .idea/

