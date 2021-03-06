--- `v.fr`

# Starter Kit pour projet simple
Petit entraînement perso sur du CSS !

## HTML
`<head>` et `<body>` configurés pour charger script et styles.

## CSS / SCSS
Style sheet avec quelques classes fournies pour mettre en page rapidement un design responsive (+ comptabilité navigateur).

le CSS seul peut suffire, possibilité d'utiliser un préprocesseur sass avec `npm install` 
- vous devez avoir node installé !
- compiler avec le script node : `npm run scss`.

## JavaScript
Javascript vanilla avec fonctionnalités ES6 (attention : pas de polyfills ou de babel).


--- `v.en`

# Starter Kit for simple project
A small self training project to learn css and theming !

## HTML
Configuration `<head>` et `<body>` for loading scripts and stylesheets properly.

## CSS / SCSS
Style Sheet with some classes provided for quick responsive page design (with browser compatibility).

CSS only will works but you can add preprocessor with `npm install`.
- you must have node installed before !
- run node script with `npm run scss `.

## JavaScript
Vanilla JavaScript with ES6 features (bad : no polyfills or babel configured yet).  

-------------------------------------------------------------------------------------------------

--- `v.fr`

# Guide
Comparé à Bootstrap, la feuille de style principale est utilisée comme support et est destinée à être modifiée. Les classes pré construites permettent de gagner du temps mais tout est custimisable rapidement.

Tous les éléments sont connectés entre eux via la classe container, il faut donc impérativement déclarer un contenu ou bloc de contenu dans un container pous assurer le responsive et maintenir un comportement harmonieux de la page.

Un fichier HTML est fournit dans le repôt pour voir une situation d'exemple.


## Mise en page
Comme Bootstrap on gère le contenu dans des blocs container. `.container` pour un container qui prend 100% de la largeur :

```html
<section class="container">...</section>
```

On peut contraindre le container a une taille spécifique (définie dans une variable scss, 80% de la largeur par défaut)

```html
<section class="container custom">...</section>
```

Si un container est full-size mais que d'autres sont custom, on peut harmoniser les marges en rajoutant une classe sur le container full size :

```html
<header class="container content-custom">...</header> <!-- 100% largeur mais marges redéfinies à 80% largeur -->
<main class="container custom">...</main> <!-- 80% largeur par défaut -->
```


### Le container peut être sticky (avec ou sans custom size).
On peut fixer les containers avec `.sticky`, par défaut en fixed top (décale automatiquement le prochain container adjacent). Etant donné que ce sont souvent les barres de navigation qui sont fixées, la hauteur d'un container sticky est définie par la hauteur de la navbar (par défaut à 75px) :

```html
<header class="container content-custom sticky">...</header> <!-- si height = 75px -->
<main class="container custom">...</main> <!--  alors margin-top = 75px -->
```

Si on veut une position fixée autrement que top :

```html
<footer class="container content-custom sticky bottom">...</footer> 
```

On peut fixer le container en sidebar. Le container suivant s'adaptera à ce comportement en se placant sur la portion de l'écran restante. (la sidebar est remplacée par un container fixed top en responsive mobile):

```html
<section class="container sticky left">...</section> 
```


## Navbar
On déclare une barre de navigation avec la classe flex `.navbar`. Si le container parent est fixé top ou left, le comportement de la navbar s'adaptera automatiquement en fonction.

On peut modifier la positions des enfants de la navbar avec `d-[position]` : `d-center`, `d-between`...

```html
<nav class="navbar d-end">...</nav>
```

On peut intégrer un menu de liste dans la navbar, par défaut les items sont alignés sur x :

```html
<ul class="navbar-menu">...</ul>
```

On peut créer un menu vertical :

```html
<ul class="navbar-menu list-col">...</ul>
```