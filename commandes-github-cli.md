# Commandes GitHub CLI et leurs fonctions

## Vérification de l’authentification

- `gh auth status`  
  Vérifie si vous êtes connecté à GitHub via GitHub CLI.

- `gh auth login`  
  Se connecte à GitHub à l'aide de GitHub CLI.

## Gestion des Dépôts

- `gh repo create <nom-du-repo> --public`  
  Crée un dépôt public sur GitHub.

- `gh repo create <nom-du-repo> --private`  
  Crée un dépôt privé sur GitHub.

- `gh repo clone <utilisateur>/<nom-du-repo>`  
  Clone un dépôt existant depuis GitHub vers votre machine locale.

- `gh repo list`  
  Liste tous les dépôts GitHub associés à votre compte.

- `gh repo view <nom-du-repo>`  
  Affiche les informations d'un dépôt spécifique.

## Gestion des Issues

- `gh issue create --title "<titre>" --body "<description>"`  
  Crée une nouvelle issue sur GitHub.

- `gh issue list`  
  Liste toutes les issues ouvertes sur le dépôt courant.

- `gh issue close <ID_DE_L_ISSUE>`  
  Ferme une issue spécifique.

- `gh issue view <ID_DE_L_ISSUE>`  
  Affiche les détails d'une issue spécifique.

## Gestion des Pull Requests (PR)

- `gh pr create --title "<titre>" --body "<description>"`  
  Crée une nouvelle pull request sur GitHub.

- `gh pr list`  
  Liste toutes les pull requests ouvertes sur le dépôt courant.

- `gh pr view <ID_DE_LA_PR>`  
  Affiche les détails d'une pull request spécifique.

- `gh pr merge <ID_DE_LA_PR> --merge`  
  Fusionne une pull request dans la branche cible.

- `gh pr close <ID_DE_LA_PR>`  
  Ferme une pull request sans la fusionner.

- `gh pr comment <ID_DE_LA_PR> --body "<commentaire>"`  
  Ajoute un commentaire à une pull request spécifique.

## Synchronisation avec GitHub

- `gh repo sync`  
  Synchronise un fork avec le dépôt principal (upstream).

- `gh repo sync <nom-de-la-branche>`  
  Synchronise une branche locale avec la branche distante.
