.. Cette page est publiée sous la license Creative Commons BY-SA (https://creativecommons.org/licenses/by-sa/3.0/fr/)

===============================
Introduction à la programmation
===============================

Pour aborder ce cours, la première grosse question à se poser est:
*Qu'est-ce que la programmation et pourquoi apprendre programmer?*

La programmation
----------------

La programmation consiste en l'écriture de programmes informatiques, appelés
également **codes**, effectuant chacun un certain résultat. Ce résultat peut être
divers. En effet, il peut simplement s'agir d'un nombre affiché par le code, ça
peut également être un changement dans un fichier.

Un code consiste en un ensemble d'**expressions** et de **statements**:

.. code-block:: python

    <expression>
    <expression>
    <statement>
    <expression>

Un **statement** est un ligne de code ne calculant pas de résultat, à l'inverse
d'une **expression**, qui calcule un résulat.

.. code-block:: python

    5 + 5               => expression
    sin(pi) + cos(pi)   => expression
    affiche 5           => statement
    verifie 5 > 0       => statement

Chaque programme est écrit dans un langage informatique comprenant un vocabulaire,
c'est à dire un ensemble de symboles et de mots clés ayant une action
prédéterminée (par exemple en **java**: *while*, *for*, *public*, *void*, *try*,
*catch*, *assert*,...) et un syntaxe propre au langage.

Utilisation
-----------

La programmation est une partie essentielle des sciences informatiques. Elle est
présente partout sur un ordinateur, que l'ordinateur soit un ordinateur de bord
d'une voiture, un serveur ou un portable, dont voici une courte liste comprenant
certaines utilisations de la programmation:

- Le système d'exploitation:
    C'est bien sûr un code, que ce soit Windows, MacOS ou
    un GNU/Linux, c'est l'un des plus imposants programmes sur n'importe quel ordinateur,
    la plupart prenant plus de 8 GB de mémoire et tournant en permanence lorsque l'ordinateur
    est en fonction.
- Les jeux vidéos:
    Ce sont également sont des programmes informatiques compliqués utilisant beaucoup
    de mémoire et utilisant beaucoup la carte graphique pour effectuer des calculs
    imposants sur des matrices en 2D ou 3D pour l'affichage du jeu.
- Les navigateurs:
    Ce sont des programmes informatiques qui peuvent gérer trois différents
    langages en plus des différents protocoles internet. En effet, les pages
    internet affichées par le navigateur sont en **HTML**, le style de ces pages
    est en **CSS** et les animations effectuées par ces pages sont en
    **JavaScript**
- Les bases de données:
    Les bases de données sont d'immenses tableaux remplis de données et pour faire
    des recherches parmi toutes ces données, on utilise des programmes codés dans
    langage spécifique, comme le **SQL**.

Les exemples ci-dessus ne reprennent qu'une petite partie de ce que l'on peut
faire avec la programmation. La programmation comporte d'innombrables applications
que vous aborderez au fur et à mesure de votre apprentissage, de la simulation
et la modélisation mathématique au machine learning et à l'IA
