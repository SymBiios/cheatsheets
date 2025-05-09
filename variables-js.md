# Variables en JavaScript

## Introduction

En JavaScript, une **variable** est un conteneur permettant de stocker une valeur (nombre, chaîne, objet, fonction, etc.). Depuis ES6 (ECMAScript 2015), on dispose de trois mots-clés pour déclarer des variables : `var`, `let` et `const`. Chacun possède des caractéristiques propres de portée et de mutabilité.

---

## 1. Déclaration et initialisation

```js
// Déclaration sans initialisation
let age;

// Initialisation (déclaration + affectation)
age = 30;

// Déclaration et initialisation en une ligne
const nom = "Alice";

// Déclaration de plusieurs variables

let a = 1, b = 2, c = 3;

// Déclaration de plusieurs variables avec la même valeur

let x = y = z = 0; // x, y et z sont tous initialisés à 0
```