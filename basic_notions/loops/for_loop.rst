.. Cette page est publiée sous la license Creative Commons BY-SA (https://creativecommons.org/licenses/by-sa/3.0/fr/)


La boucle for
=============

Précédemment, vous étiez obligés d'utiliser un compteur afin de modifier les variable sà votre disposition dans votre boucle, avec *for* vous allez pouvoir le faire plus élégamment.

L'instruction for travaille sur des séquences. Elle est en fait spécialisée dans le parcours d'une séquence de plusieurs données. Retenez juste ça pour le moment, on reviendra sur les séquences par la suite.

La syntaxe de *for* est :

.. code-block:: python

    for element in sequence:
        # instruction 1
        # instruction 2
        # ...
        # instruction N

En attendant que vous voyez les séquences, voilà un petit tuyau pour en générer une: la méthode range

* ``range(a, b, c)`` génère une séquence allant de a (compris) à b (non compris) par pas de c,
* ``range(a, b)`` si on veut des pas de 1,
* ``range(a)`` si on veut une suite commençant par 0 jusqu'à a (non compris) et avancer par pas de 1.

.. inginious-sandbox:: DummyScript

    for i in range(1, 11, 2):
        print(i)

Vous remarquerez ques *i* prendra la valeur de un élément sur deux se trouvant entre 1 et 11 (non-inclus, attention aux bornes!) et ce sans qu'on doive l'incrémenter nous-même. Voilà de quoi s'assurer plus clair et élégant. Réessayons un exercice sur les boucles avec un for et un range à présent:

.. inginious:: FirstSum
