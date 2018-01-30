# ROR_Basics
Les concepts basiques de rails, expliqué par un moussaillon



## Site statique / site dynamique

Un site statique est un site exclusivement en HTML et CSS alors qu’un site dynamique est interactif, par exemple en utilisant du javascript. 

## Les routes

Ce qui est sympa avec les routes, ce que leurs noms est super explicite : ce sont littéralement des routes vers les méthodes contenue dans le contrôleur. Elles guident les requête de l’internaute vers le méthodes correspondantes, qui sont dans un fichier nomfichier_controller.rb. 

## Le MVC

**Rails utilise la structure MVC**
*Kezako ?*

Il y a dans le dossier app de rails, trois dossiers nommés :

 - Model 
 - View 
 - Controller


Quand un utilisateur fait une requête sur le web, celle-ci est redirigée par rails (vous savez, dans le fichier `routes.rb`). Bon, en fonction de la requête, `routes.rb` ne va pas envoyer la même action, donc imaginons une action A, qui nous servira d'exemple.
Donc le routeur rails envoie l'action A au contrôleur .

**Le Contrôleur** est comme un gros sac de méthode (dont l'action A)
Il va demander au **Modèle** de lui fournir toutes les informations nécessaires à l'exécution de cette méthode.
Pour y arriver, le Modèle tire les informations dont il a besoin de la base de donnée. Il possède aussi les informations propres à chaque type d'objets (oui, les classes!)

Quand le Modèle a envoyé les informations nécessaires au Contrôleur, c'est au tour de **la Vue** de rentrer en scène : **elle transforme le code complet en HTML, CSS et Javascript, c'est à dire en élément visuel avec lesquels l'utilisateur va interagir** (ce n'est pas pour rien qu'on l'appelle vue !) Tout cela est encore renvoyé au contrôleur qui l'envoie en au navigateur, qui l'affiche à l'utilisateur.


## Le CRUD

CRUD fait référence à un ensemble de méthode :

 - **C** pour create

 Toutes les actions liées à la méthode POST  qui envoie des informations au serveurs. Par exemple dans le cas de la création d’un formulaire. 

 - **R** pour read

 Toutes les actions liées à la méthode GET, qui reçoit de l’information. Par exemple, quand l’on veut afficher un ensemble de photo sur un site.

 -  **U** pour update

  Toutes les actions liée à la methode PUT, qui met a jour un élément , une information

 - **D** pour destroy

 Toutes les actions liée à la méthode DELETE qui … supprime les éléments. 

## La migration

La migration est un moyen de mettre à jours son fichier schema.rb, c’est à dire sa base de donnée, sans pour autant avoir à écrire en SQL. 


## BDD Bases de données

Les bases de données sont les fichiers qui possèdent toutes les informations nécessaires au fonctionnement des méthodes stockées dans le contrôleur.  Elles sont liée au modèles et ils est possible de trouver dans la base de donnée, des classes enfants des classes dans le modèle. 

