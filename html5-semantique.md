# 🌐 HTML5 Sémantique - Liste des Balises Essentielles  

- **`<header>`** : Contient l'en-tête d'une page ou d'une section, incluant souvent le titre et la navigation. 
    ```html
        <header>
            <h1>Mon Site Web</h1>
            <nav>
                <ul>
                    <li><a href="#">Accueil</a></li>
                <li><a href="#">Services</a></li>
            </ul>
            </nav>
        </header> 
    
- **`<nav>`** : Définit un bloc de navigation contenant des liens internes au site.
    ```html  
        <nav>
            <ul>
                <li><a href="#">Accueil</a></li>
                <li><a href="#">Blog</a></li>
            </ul>
        </nav>

- **`<main>`** : Regroupe le contenu principal d'une page, ne doit pas inclure d'éléments répétitifs comme le menu ou le pied de page.

    ```html
        <section>
            <h2>Nos Services</h2>
            <p>Description des services proposés.</p>
        </section>

- **`<section>`** : Utilisé pour structurer une page en différentes sections thématiques.  

    ```html
        <section>
            <h2>Nos Services</h2>
            <p>Description des services proposés.</p>
        </section>

- **`<article>`** : Contenu indépendant comme un article de blog, une news ou un post.

    ```html
        <article>
            <h2>Titre de l'article</h2>
            <p>Contenu détaillé de l'article.</p>
        </article>

- **`<aside>`** : Zone contenant du contenu annexe, comme une barre latérale, des liens connexes ou des publicités.

    ```html
        <aside>
            <h3>Articles récents</h3>
            <ul>
                <li><a href="#">Article 1</a></li>
                <li><a href="#">Article 2</a></li>
            </ul>
        </aside>

- **`<footer>`** : Pied de page contenant des informations complémentaires comme des contacts, des liens légaux ou des crédits.

    ```html
        <footer>
            <p>&copy; 2025 Mon Site Web - Tous droits réservés.</p>
        </footer>

- **`<figure>`** : Conteneur pour une image accompagnée d'une légende, souvent utilisé avec `<figcaption>`.
    ```html
        <figure>
            <img src="image.jpg" alt="Description de l'image">
            <figcaption>Une belle image illustrant notre sujet.</figcaption>
        </figure>

- **`<figcaption>`** : Fournit une légende pour un élément `<figure>`. 

    ```html
       <figcaption>Légende pour l'image ci-dessus.</figcaption>

- **`<mark>`** : Met en surbrillance un texte important.

    ```html
        <p>Ceci est un <mark>texte mis en évidence</mark>.</p>

- **`<time>`** : Représente une date ou une heure, utile pour les événements ou les articles.

    ```html
        <p>Événement prévu le <time datetime="2025-06-15">15 juin 2025</time>.</p>

- **`<address>`** : Contient des informations de contact (adresse postale, email, téléphone).

    ```html
        <address>
            123 Rue Exemple, Paris, France  
            Email : contact@monsite.com
        </address>

- **`<details>`** : Permet d'afficher un contenu replié/déplié par l'utilisateur.

    ```html
        <details>
            <summary>Plus d'infos</summary>
            <p>Voici plus d'informations détaillées.</p>
        </details>

- **`<summary>`** : Définit un titre pour un élément `<details>`.
    
    ```html
        <summary>Afficher plus</summary>

- **`<dialog>`** : Crée une boîte de dialogue native en HTML5.

    ```html
        <dialog open>
            <p>Message important.</p>
        </dialog>

- **`<cite>`** : Utilisé pour citer une œuvre (livre, film, site web).

    ```html
        <p>Un grand livre : <cite>1984</cite> de George Orwell.</p>

- **`<code>`** : Affiche du texte sous forme de code source.

    ```html
        <p>Voici un exemple de code : <code>&lt;h1&gt;Titre&lt;/h1&gt;</code></p>

- **`<kbd>`** : Définit une saisie au clavier, utile pour indiquer des raccourcis clavier.

    ```html
        <p>Appuyez sur <kbd>Ctrl</kbd> + <kbd>C</kbd> pour copier.</p>

- **`<samp>`** : Représente la sortie d’un programme ou d’un script.

    ```html
        <p>Sortie du programme : <samp>Erreur 404</samp></p>

- **`<abbr>`** : Indique une abréviation avec une info au survol (via l'attribut `title`).

    ```html
        <p>L'abréviation de "HyperText Markup Language" est <abbr title="HyperText Markup Language">HTML</abbr>.</p>