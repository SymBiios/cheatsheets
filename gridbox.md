# Propriétés Gridbox et Valeurs.

- `display` : Définit un conteneur grid.
  - `grid` : Conteneur grid classique.
  - `inline-grid` : Conteneur grid en ligne.

- `grid-template-columns` : Définit la structure des colonnes dans un grid.
  - Valeurs : 
    - `auto` : La largeur des colonnes est automatiquement déterminée.
    - `px`, `em`, `%`, `fr` (fraction de l’espace disponible), etc. : Valeurs fixes ou fractionnées.
    - `repeat()` : Permet de répéter une structure de colonnes, par exemple `repeat(3, 1fr)` pour 3 colonnes égales.

- `grid-template-rows` : Définit la structure des lignes dans un grid.
  - Valeurs : 
    - `auto` : La hauteur des lignes est automatiquement déterminée.
    - `px`, `em`, `%`, `fr` (fraction de l’espace disponible), etc. : Valeurs fixes ou fractionnées.
    - `repeat()` : Permet de répéter une structure de lignes.

- `grid-template-areas` : Permet de nommer et disposer des zones dans un grid (basé sur des noms de lignes et de colonnes).
  - Valeurs : 
    - Chaîne de noms de zones, par exemple :
      ```css
      grid-template-areas: 
        "header header header"
        "sidebar content content"
        "footer footer footer";
      ```

- `grid-column` : Permet de définir la position d'un élément sur l'axe des colonnes.
  - Valeurs : 
    - `span` : Étend un élément sur plusieurs colonnes (ex : `span 2` pour 2 colonnes).
    - `start` et `end` : Définissent les lignes de départ et d’arrivée sur l’axe des colonnes (ex : `grid-column: 1 / 3`).

- `grid-row` : Permet de définir la position d'un élément sur l'axe des lignes.
  - Valeurs : 
    - `span` : Étend un élément sur plusieurs lignes (ex : `span 2` pour 2 lignes).
    - `start` et `end` : Définissent les lignes de départ et d’arrivée sur l’axe des lignes (ex : `grid-row: 1 / 3`).

- `grid-column-gap` : Définit l'espacement entre les colonnes.
  - Valeurs : 
    - `px`, `em`, `%`, etc. : Valeur spécifique pour l’espacement.
  
- `grid-row-gap` : Définit l'espacement entre les lignes.
  - Valeurs : 
    - `px`, `em`, `%`, etc. : Valeur spécifique pour l’espacement.
  
- `gap` : Définit à la fois l'espacement entre les colonnes et les lignes.
  - Valeurs : 
    - `px`, `em`, `%`, etc. : Espacement entre les colonnes et les lignes.
  
- `justify-items` : Aligne les éléments à l’intérieur de chaque cellule de grid sur l’axe horizontal.
  - Valeurs : 
    - `start` : Aligner au début.
    - `end` : Aligner à la fin.
    - `center` : Aligner au centre.
    - `stretch` : Étirer pour remplir l'espace disponible (valeur par défaut).

- `align-items` : Aligne les éléments à l’intérieur de chaque cellule de grid sur l’axe vertical.
  - Valeurs : 
    - `start` : Aligner au début.
    - `end` : Aligner à la fin.
    - `center` : Aligner au centre.
    - `stretch` : Étirer pour remplir l'espace disponible (valeur par défaut).

- `justify-content` : Aligne les éléments à l’intérieur du conteneur grid sur l’axe horizontal.
  - Valeurs : 
    - `start` : Aligner au début.
    - `end` : Aligner à la fin.
    - `center` : Aligner au centre.
    - `space-between` : Espacement égal entre les éléments.
    - `space-around` : Espacement égal autour des éléments.
    - `space-evenly` : Espacement égal entre, avant et après les éléments.

- `align-content` : Aligne les éléments à l’intérieur du conteneur grid sur l’axe vertical.
  - Valeurs : 
    - `start` : Aligner au début.
    - `end` : Aligner à la fin.
    - `center` : Aligner au centre.
    - `stretch` : Étendre pour remplir l’espace (valeur par défaut).
    - `space-between` : Espacement égal entre les lignes de grid.
    - `space-around` : Espacement égal autour des lignes de grid.
  
- `place-items` : Permet de définir à la fois `justify-items` et `align-items` en une seule déclaration.
  - Valeurs : 
    - `start`, `center`, `end`, `stretch`, etc.

- `place-content` : Permet de définir à la fois `justify-content` et `align-content` en une seule déclaration.
  - Valeurs : 
    - `start`, `center`, `end`, `stretch`, `space-between`, `space-around`, etc.

- `grid-auto-columns` : Définit la taille des colonnes qui seront créées automatiquement si nécessaire (lorsque les éléments dépassent les dimensions spécifiées dans `grid-template-columns`).
  - Valeurs : 
    - `auto` : Taille automatique.
    - `px`, `em`, `%`, etc.

- `grid-auto-rows` : Définit la taille des lignes qui seront créées automatiquement si nécessaire (lorsque les éléments dépassent les dimensions spécifiées dans `grid-template-rows`).
  - Valeurs : 
    - `auto` : Taille automatique.
    - `px`, `em`, `%`, etc.
