# Propriétés et leurs valeurs Flexbox

- `display` : Définit un conteneur flex.
  - `flex` : Conteneur flex.
  - `inline-flex` : Conteneur flex en ligne.

- `flex-direction` : Définit la direction des éléments dans le conteneur.
  - `row` : Alignement horizontal (gauche à droite).
  - `row-reverse` : Alignement horizontal inverse (droite à gauche).
  - `column` : Alignement vertical (haut en bas).
  - `column-reverse` : Alignement vertical inverse (bas en haut).

- `flex-wrap` : Définit si les éléments doivent être répartis sur plusieurs lignes.
  - `nowrap` : Pas de retour à la ligne.
  - `wrap` : Retour à la ligne.
  - `wrap-reverse` : Retour à la ligne, mais ordre inversé.

- `flex-flow` : Combinaison de `flex-direction` et `flex-wrap`.
  - `row wrap` : Par défaut, avec retour à la ligne.
  - `column nowrap` : Alignement vertical sans retour à la ligne.

- `justify-content` : Aligne les éléments sur l'axe principal (horizontal ou vertical selon `flex-direction`).
  - `flex-start` : Aligner au début.
  - `flex-end` : Aligner à la fin.
  - `center` : Aligner au centre.
  - `space-between` : Espacement égal entre les éléments.
  - `space-around` : Espacement égal autour des éléments.
  - `space-evenly` : Espacement égal entre, avant et après les éléments.

- `align-items` : Aligne les éléments sur l'axe transversal (perpendiculaire à l'axe principal).
  - `flex-start` : Aligner au début.
  - `flex-end` : Aligner à la fin.
  - `center` : Aligner au centre.
  - `baseline` : Aligner selon la ligne de base du texte.
  - `stretch` : Étendre les éléments pour remplir le conteneur (par défaut).

- `align-self` : Permet de spécifier l'alignement d'un élément individuel sur l'axe transversal.
  - `auto` : Valeur par défaut.
  - `flex-start` : Aligner au début.
  - `flex-end` : Aligner à la fin.
  - `center` : Aligner au centre.
  - `baseline` : Aligner selon la ligne de base du texte.
  - `stretch` : Étendre l'élément pour remplir le conteneur.

- `align-content` : Aligne plusieurs lignes d'éléments sur l'axe transversal.
  - `flex-start` : Aligner au début.
  - `flex-end` : Aligner à la fin.
  - `center` : Aligner au centre.
  - `space-between` : Espacement égal entre les lignes.
  - `space-around` : Espacement égal autour des lignes.
  - `stretch` : Étendre les lignes pour remplir le conteneur.

- `order` : Modifie l'ordre des éléments flex.
  - Valeur numérique : L'ordre des éléments est défini par un nombre (par défaut 0).
  
- `flex-grow` : Définit la capacité d'un élément à croître pour occuper l'espace supplémentaire.
  - Valeur numérique : Par défaut `0`, cela définit combien un élément peut croître.

- `flex-shrink` : Définit la capacité d'un élément à rétrécir si l'espace est insuffisant.
  - Valeur numérique : Par défaut `1`, cela définit combien un élément peut rétrécir.

- `flex-basis` : Définit la taille initiale d'un élément avant qu'il ne soit étendu ou rétréci.
  - `auto` : Taille par défaut.
  - Valeur en pixels, em, %, etc. : Taille spécifique de l'élément.
