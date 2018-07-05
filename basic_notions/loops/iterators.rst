.. Cette page est publiée sous la license Creative Commons BY-SA (https://creativecommons.org/licenses/by-sa/3.0/fr/)


Les itérateurs
==============

On a vu comment répéter une instructions plusieurs fois grâces aux boucles for et while. Il existe une autre manière pour traverser une liste d'éléments, il s'agit de l'itérateur.

Un itérateur nous donne une fontion ``*magique*`` qui nous permet de parcourir une série d'éléments.

.. code-block:: python

    >>> x = iter([0, 2, 4])
    >>> next(x)
    1
    >>> next(x)
    2
    >>> next(x)
    3
    >>> next(x)
    Traceback (most recent call last):
    File "<stdin>", line 1, in <module>
    StopIteration

Chaque fois qu'on appelle la méthode **next**, l'itérateur nous donne l'élément suivant. Si il n'y a plus d'élément, il envoie l'exception **StopIteration**.

La boucle for peut se servir des itérateurs pour donner les éléments un à un.

Voici un exercice pratique pour comprendre comment l'utiliser.

.. inginious:: WrongIterations
