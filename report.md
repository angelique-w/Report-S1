CSS responsive :
===============


Adapter le design d'une application (ou site web) selon le support utilisé (mobile, tablette, desktop)


Bonnes pratiques : 
------------------


privilégier le mobile first = penser le design pour affichage mobile et ensuite adapter pour la version desktop.
Le nombre d'utilisateurs de mobiles ayant dépassé le nombre d'utilisateurs de desktop.


Outils de CSS responsive:
------------------------


### Utilisation de media queries :



Les media queries permettent d'appliquer un CSS selon une condition définie : exemple affichage mobile ou affichage desktop.

*Dans l'HTML*

  <link rel="stylesheet" href="style.css">
  
  <meta name='viewport' content='width=device-width, initial-scale=1.0, maximum-scale=1.0' />

*Dans le CSS* 

  @media(min-width:961px){
    .files article{
      display: inline-block;
      margin : 0px 10px 100px 10px;
      padding:10px;
      background-color: #e6e6e6;
      height: 400px;
      width:25%;
      text-align:center;
      }
    }
  
Dans le code ci-dessus :

à partir du moment ou la taille de l'écran est supérieure à 961px (min-width 961px)

appliquer le css.


*Pour rentrer dans le détail :*

  * affichage <768px = smartphone
  
  * 768px < affichage portrait tablette < 992px
  
  * 992px < affichage paysage tablette < 1200px
  
  * affichage >1200px desktop
  

au lieu d'utiliser plusieurs media-queries, possibilité d'appeller plusieurs feuilles de CSS dans l'HTML:

<link rel="stylesheet" href = "mobile.css">

<link rel="stylesheet" href = "tablette.css">


### Flexbox :



L'objectif est de gagner en efficacité dans l'affichage, l'alignement, la distribution des espaces dans un élément (container par ex.)

  .container {
    display: flex; /* or inline-flex */
  }


### CSS grid :



CSS grid va au delà de ce que propose flexbox.
Flexbox a été créé pour de l'affichage en lignes ou colonnes (rows, columns), CSS grid permet d'aller plus loin et de travailler dans un système de grilles.
Les deux fonctionnent bien conjointement.

  .container {
    display: grid | inline-grid;
  }


Sources :
---------


* [CCS tricks flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

* [CSS tricks grid](https://css-tricks.com/snippets/css/complete-guide-grid/)

* [Open classrooms : rédiger en markdown](https://openclassrooms.com/fr/courses/1304236-redigez-en-markdown)





Les outils:


GitHub: est un site web participatif utilisé pour échanger de données entre développeur 

Git: est un utilitaire pour l’organisation des données depuis le terminal (shell) 

visual studio code, sublime texte ainsi que notepad++ sont des éditeurs de texte, 

Curl: est un logiciel qui permet de récupérer le contenu d’une ressource informatique et de les collecter.

nvm: est un utilitaire du terminal qui sert a maintenir les paquets a jour.

php: est langage de programmation libre , principalement utilisé  pour produire des pages web dynamique via un serveur http. le serveur fait un interpretation du langage php pour le traduire en html.

Sur Mac l’installation de Homebrew pour permettre l’installations de paquets 





