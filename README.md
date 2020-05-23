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
# Guide
Comparé à Bootstrap, la feuille de style principale est utilisée comme support et est destinée à être modifiée. Les classes pré construites permettent de gagner du temps mais tout est custimisable rapidement.

Tous les éléments sont connectés entre eux via la classe container, il faut donc impérativement déclarer un contenu ou bloc de contenu dans un container pous assurer le responsive et maintenir un comportement harmonieux de la page.

Un fichier HTML est fournit dans le repôt pour voir une situation d'exemple.


### Mise en page
Comme Bootstrap on gère le contenu dans des blocs container

`.container` pour un container qui prend 100% de la largeur

`.container .custom` pur un container avec une taille spécifique (définie dans une variable scss, 80% de la largeur par défaut)

Le container peut être sticky (avec ou sans custom size).

`.container .sticky` pour un container sticky top (créé un margin-top sur le prochain container adjacent)

`.container .sticky .bottom` pour un container sticky bottom

`.container .sticky .left` pour un container fixé à gauche. Le container suivant s'adaptera à ce comportement en se placant sur la portion de l'écran restante. (le container est sticky top en responsive)

Si un container est full-size mais que d'autres sont custom, on peut harmoniser les marges en rajoutant une classe sur le container full size (pas indispensable si le container est en sidebar)

`.container .custom-content`

La largeur de l'élément dans le container s'adaptera en fonction de ces classes pour maintenir les marges.


