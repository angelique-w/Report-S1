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

Sur Mac l’installation de Homebrew pour permettre l’installations de paquets.


Métier dde développeur et veille:

 Nous avons appris ce qu'est le métier de développeur et ses différentes facettes:
UX/UI, Front-End, Back-End et DévOps.

Grâce au Daily Stand-Up, nous pratiquons la méthode agile (nous faisons un point sur ce qu'on a fait, nos objectifs et connaitre l'avancée des autres).

Comme les technologies changent rapidement, tout développeur doit faire sa veille. Il y a plusieurs façons: aller sur des sites  tels que dev.to, css weekly... ainsi que sur des sites ressources tels que css tricks ou MDN, mais également sur des forums de communautés de développeurs comme slack ou rocket.

TERMINAL WEEK ONE
==================

1. ouverture du terminal (ctrl+alt+t (linux)/ command+space+t (Mac))
      
      ===>  programmes telechargés:x
              - sudo apt get/install/update/upgrade... (linux)
                  |-> sudo = super user
                  - home brew (mac)
                  - nvm (node version manager => manager de paquet pour node.js)
                  - Git (logiciel de gestion de version decentralisé => permet de collaborer et travailler en commun sur des mêmes projets en même temps. )
                  - Curl (interface en ligne de commande, destiné à récupérer le contenu d'une ressource accessible par un réseau informatique)
                  - VsCode (éditeur de texte sous forme graphique)
                  - SSh Key (système sécurisé permettant de se connecter de façon sécurisée à une machine distante.)
                  - php 7.3 ( dernière version du langage PHP language back-end de programmation)

2. Utilisation du Terminal 

    a. Naviguer dans les dossiers 

      .se situer dans le terminal avec la commande "pwd"

          pwd / se situer à l'instant dans le terminal

          pwd Renvoyer le chemin absolu du répertoire courant ce qui est utile puisqu’en général le shell n’affiche que le nom du répertoire courant.
       
      .Navigation Répertoire avec commande "cd" :

          cd / Permet de se retrouver à la racine du disque.

          cd ~ ou cd Accéder directement au répertoire de l’utilisateur.

          cd /var/www/ Aller dans le répertoire /var/www.

          cd .. Remonter dans le répertoire parent à partir de là où vous êtes.

          cd - Permet de revenir au répertoire précédent.   

          
      .Afficher contenu avec commande "ls" :

          ls -l Afficher les informations de manière détaillée.

          ls -a Afficher les fichiers cachés.

          ls -h Afficher la taille des fichiers de facon lisible.

          ls -r Tri inversé.

          ls -t Trier les fichiers par date du plus récent au plus ancien.

          ls -S Trier par taille décroissante.

          ls -la Afficher tous les fichiers y compris les fichiers cachés.

          ls -lhS Afficher les informations des fichiers, avec des tailles lisibles le tout ordonné du plus grand au plus petit.


      .pour créer des copies avec commande "cp"  

          cp foo/bar.txt baz/ Copier le fichier bar.txt dans le répertoire baz.

          cp -r foo/ baz/ Copier des répertoires entiers (note : si baz existe, la cible sera baz/foo/).

      .Pour déplacer renommer des fichiers avec la commande "mv" :

          mv foo/bar.txt baz/ Déplacer le fichier bar.txt dans le répertoire baz.

          mv foo_bar.txt foo_baz.txt Renommer le fichier foo_bar.txt en foo_baz.txt.

      
 
      .Pour effacer fichier répertoire avec la commande "rm" :

          rm *.txt Supprimer tous les fichiers ayant pour extension txt.

          rm foo.txt bar.txt Supprimer les fichiers foo.txt et bar.txt.

          rm -rf baz/ Supprimer le répertoire baz et tout son contenu.

      . pour créer un répertoir avec la commande "mkdir" :

          mkdir -v Retourner des informations lors de la création d'un répertoire.

          mkdir -p Cette option permet de créer une arborescence complète.

          mkdir foo Créer le répertoire foo.

          mkdir -v foo /tmp/bar Créer les répertoires foo et /tmp/bar.

          mkdir -p foo/bar/baz Créer l’arborescence foo/bar/baz.   

  

Voici la liste des commandes vu cette semaine et pour les curieux voici un lien pour les futurs commandes utiles "http://juliend.github.io/linux-cheatsheet/"

4. Editeur de texte avec le Terminal

Les éditeurs de texte principaux sont "nano", "vim", "emacs".

Nano : un éditeur de texte facile d'utilisation (débutant)

Vim : un éditeur de texte pour les utilisateurs plus confirmés comprenant un environnement de développement complet 
avec installations de plugins (plus rapide et stable une fois configurer)

Emacs : un éditeur de texte avec un environnement de développement complet.

Conclusion : 

Le terminal est une interface de commande permettant tous types de fonctionnalités (gérer ces fichiers, dossiers, ouvrir des logiciels, avoir accés à des commandes systèmes, écrire directement des languages grâces aux éditeurs de textes .....)
Pour résumer, le terminal permet d'effectuer directement et rapidemenet toutes les commandes de l'interface graphique à partir d'une seule et même fenêtre en ayant la bonne connaissances des commandes.


# Git

## Qu’est-ce que Git ?

Git est un système de gestion de versions décentralisé. C'est un logiciel libre créé par Linus Torvald, auteur du noyau Linux. C'est aujourd'hui le logiciel de gestion de versions le plus populaire.

Objectifs :
* travailler à plusieurs sur le même code
* historiser le code 
* gérer les versions

##  Comment cela fonctionne ?

Installation via le terminal ( sous Ubuntu : sudo apt install git ; pour les autres OS, cf. https://git-scm.com/book/fr/v1/D%C3%A9marrage-rapide-Installation-de-Git)


## Paramétrage de Git

Git propose 3 niveaux de configuration :
*1. Locale. Spécifique à chaque dépôt local, elle est stockée dans le .git/config. On y trouve notamment les trackings de branches, le remote, etc. 
*2. Globale. Spécifique à l'utilisateur, elle est stockée à la racine de son compte, dans le fichier ~/.gitconfig. C'est celle qui nous intéresse ici. 
*3. Système. Généralement stockée dans /etc/gitconfig, elle est partagée par tous les utilisateurs. Elle est rarement employée. 
Git a OBLIGATOIREMENT besoin de 2 paramètres pour fonctionner qui correspondent à notre identité, notre NOM et notre EMAIL (qui doivent être les mêmes que ceux de notre compte GitHub créé en ligne). Ces données seront utilisées pour chaque commit que l’on fera (=enregistrement / modification). 

*Il est possible de paramétrer d’autres choses (personnalisation) comme l’éditeur de texte utilisé par Git (par défaut nous avons nano sur Ubuntu) ; l’outil utilisé pour résoudre les conflits de fusion ; l’affichage de couleurs ; des aliases (sortes de raccourcis clavier pour donner une commande, ex : ci pour commit) ; la pagination ; les whitespaces ; etc.
Ces configurations se font via le terminal de commande.
Il est possible de customiser le terminlal et son PS1 à travers le ficher bashrc.*

## Commandes

Les commandes de Git sont directement liées à celles du terminal. 
Voici les commandes que nous avons pu découvrir durant les quêtes :
* init : initialise le répoertoire comme projet Git
* add : ajoute un fichier qui sera suivi par Git
* commit : enregistre l'index (liste des fichiers trackés) vers un nouveau commit, avec un commentaire sur les modifications effectuées
* status : donne l'état du suivi des fichiers ainsi que les fichiers ayant des différences de version
* branch : lister, créer ou supprimer une branche
* checkout : se déplacer entre les branches

## Utiliser Git avec un repository distant

Il faut câbler et paramétrer le repository distant (qui se situe sur notre GitHub) avec notre repository local (qui se situe dans notre machine) afin de les lier.

2 commandes :
* push : envoyer vers le repository distant
* pull : récupérer depuis le repository distant

