# Architecture 7-1 de Sass

L'architecture 7-1 de Sass est une manière de structurer les fichiers SCSS dans un projet pour qu'il soit modulaire, facile à maintenir et à étendre.

## Structure des dossiers

1. **`/abstracts`** - (Variables, Mixins, Functions)
   - Contient des fichiers pour les éléments réutilisables (variables, mixins, fonctions).
   
2. **`/base`** - (Styles de base)
   - Contient les styles de base du projet comme le reset, la typographie, etc.

3. **`/components`** - (Composants réutilisables)
   - Contient les styles pour les composants réutilisables comme les boutons, cartes, etc.

4. **`/layout`** - (Disposition)
   - Contient les styles de mise en page, comme la structure de la grille, la navigation, etc.

5. **`/pages`** - (Styles spécifiques aux pages)
   - Contient les styles qui sont spécifiques à certaines pages du projet.

6. **`/themes`** - (Thèmes)
   - Contient les styles pour différents thèmes (clair, sombre, etc.).

7. **`/vendors`** - (Bibliothèques externes)
   - Contient les styles provenant de bibliothèques tierces comme Bootstrap, FontAwesome, etc.

## Fichier principal

- **`main.scss`** - Fichier principal où tous les autres fichiers SCSS sont importés.
