Tutoriel
========

Vous trouverez dans ce document la mise en place et l'implémentation du Live Viewver
avec Varnish Custom Statistic.

Pré-requis
---------

* [Varnish Plus](https://www.varnish-software.com/products/varnish-plus) et [Varnish Cache Statistic](https://www.varnish-software.com/plus/varnish-custom-statistics)
* La librairie [d3.js](https://d3js.org/)
* [eZ Platform](http://ezplatform.com/) / [eZ Studio](http://ezstudio.com/) (fonctionne également avec des versions 5.x d'eZ Publish Platform).

Concept
-------

    Afin de visualiser en temps réel (ou proche pour la démo) des contenus provenant d'eZ, il va être nécessaire
de rajouter des headers. Varnish va alors utiliser ceux ci afin de rajouter des statistiques à VCS et par
conséquent de nous générer une liste d'URL avec un score. Le score est tout simplement le nombre de personnes
consultant la page.

Configuration d'eZ Platform / eZ Studio
---------------------------------------

    Si vous utilisez eZ Platform / eZ Studio, la création de contrôleur est nécessaire afin de gérer les affichages 
en fonction des types de contenus. En effet la représentation d'un article est, dans la plupart des cas, différente
d'un blog post par exemple.
Pour plus d'informations sur l'installation et configuration d'eZ, référez vous à la [documentation](https://doc.ez.no/display/TECHDOC/Beginner+Tutorial).

Configuration de Varnish
------------------------

Mise en place de d3.js
----------------------