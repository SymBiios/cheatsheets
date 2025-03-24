# Commandes de base pour Zsh avec plugins installés

## Commandes générales

- `cd [dir]` : Naviguer dans un répertoire
- `ls` : Lister le contenu d'un répertoire
- `pwd` : Afficher le chemin du répertoire courant
- `mkdir [dir]` : Créer un répertoire
- `rm [file]` : Supprimer un fichier
- `rm -r [dir]` : Supprimer un répertoire et son contenu
- `touch [file]` : Créer un fichier vide
- `cp [source] [destination]` : Copier un fichier
- `mv [source] [destination]` : Déplacer ou renommer un fichier
- `find [dir] -name [file]` : Trouver un fichier par nom
- `cat [file]` : Afficher le contenu d'un fichier
- `grep [pattern] [file]` : Chercher un motif dans un fichier

## Gestion des processus

- `ps` : Lister les processus en cours
- `top` : Afficher les processus en temps réel
- `kill [pid]` : Terminer un processus
- `htop` : Version plus interactive de `top` (si installé)

## Historique de commandes

- `history` : Afficher l'historique des commandes
- `!!` : Réexécuter la dernière commande
- `!<number>` : Exécuter une commande de l'historique par son numéro
- `!<command>` : Exécuter la dernière commande commençant par `<command>`
- **Recherche dans l'historique** : (Avec `zsh-history-substring-search`)
  - `Ctrl + R` : Recherche dans l'historique avec sous-chaîne (commence à taper pour rechercher dans l'historique)
  - `Ctrl + S` : Recherche dans l'historique en avant (après avoir fait `Ctrl + R`)

## Plugins de navigation et gestion de répertoires

- **Naviguer rapidement entre les répertoires** : (Avec `zsh-navigation-tools`)
  - `Ctrl + U` : Remonter à la ligne précédente
  - `Ctrl + D` : Remonter d'un répertoire
  - `Alt + →` et `Alt + ←` : Naviguer entre les mots dans la ligne de commande

## Recherche interactive et complétions

- **fzf** : Recherche interactive pour trouver rapidement des fichiers, des commandes, etc.
  - `fzf` : Ouvre un sélecteur interactif pour rechercher des fichiers ou d'autres éléments.
  - Utilisation avec `find` pour rechercher des fichiers de manière interactive :
    ```bash
    find . | fzf
    ```
  - Utilisation avec l'historique pour rechercher des commandes passées :
    ```bash
    history | fzf
    ```
  - Utilisation avec `git` pour rechercher dans l'historique des commits :
    ```bash
    git log --oneline | fzf
    ```

- **Complétions améliorées** : (Avec `zsh-completions`)
  - Ajoute des complétions pour une plus grande variété de commandes.
  - Ex : `git`, `docker`, `kubectl`, etc., auront des complétions supplémentaires.

## Éditeurs de texte

- `atom [file]` : Ouvre le fichier spécifié dans **Atom** (si installé)
- `nano [file]` : Ouvre le fichier spécifié dans **Nano**

## Autres commandes pratiques

- `clear` : Effacer l'écran du terminal
- `exit` : Quitter le terminal
- `man [command]` : Afficher la documentation d'une commande
- `echo [text]` : Afficher du texte dans le terminal
- `alias [name]='[command]'` : Créer un alias pour une commande
- `unalias [name]` : Supprimer un alias
- `source ~/.zshrc` : Recharger la configuration Zsh

## Raccourcis pratiques

- **Autocomplétion** :
  - `Tab` : Compléter le fichier ou la commande en cours (si disponible)
  
- **Navigation dans le terminal** :
  - `Ctrl + A` : Aller au début de la ligne
  - `Ctrl + E` : Aller à la fin de la ligne
  - `Ctrl + U` : Supprimer le texte avant le curseur
  - `Ctrl + K` : Supprimer le texte après le curseur
  - `Ctrl + W` : Supprimer le mot avant le curseur
  - `Ctrl + L` : Effacer l'écran du terminal
