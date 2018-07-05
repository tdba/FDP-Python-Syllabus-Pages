.. Cette page est publiée sous la license Creative Commons BY-SA (https://creativecommons.org/licenses/by-sa/3.0/fr/)

Les types de données
====================

En Python comme dans la majorité des langages de programmation, chaque valeur a un certain type.
Il est en effet souvent important de savoir différencier un nombre d'un texte par exemple:
on ne mélange pas les pommes et les poires...

Pour afficher le type d'une variable, on utilise ``type()``:

.. code-block:: python

    >>> type(5)
    <class 'int'>
    >>> type("hello")
    <class 'str'>

On peut donc voir que le type de la valeur ``5`` est ``int``, ce qui signifie que 5 est un entier
(*integer* en Anglais) et que le type de la donnée ``"hello"`` est ``str``, une chaine de caractère
(*string* en Anglais).

Évidemment, dépendant des données, ces types seront différents. En voici une liste non-exhaustive:

===========  ==========================================================================  ==================
Nom du type  Signification                                                               Exemple
===========  ==========================================================================  ==================
``int``      Nombre entier (*integer* en Anglais)                                        12
-----------  --------------------------------------------------------------------------  ------------------
``float``    Nombre à virgule flottante                                                  3.14
-----------  --------------------------------------------------------------------------  ------------------
``str``      Chaine de caractère (*string* en Anglais)                                   "Bonsoir"
-----------  --------------------------------------------------------------------------  ------------------
``bool``     Booléen (une expression qui est évaluée soit a ``True``, soit à ``False``)  5 > 18
===========  ==========================================================================  ==================

Il s'agit ici de types de données de base, il en existe bien évidemment beaucoup d'autres,
certains qui vous seront présentés tout au long de ce cours.

Dans la suite de ce cours, nous utiliserons généralement le nom que Python donne aux types
(i.e. on dira que ``1`` est un ``int`` plutôt qu'un entier).

Il est à noter que c'est sur base du type des données que Python peut déterminer si une opération est faisable ou non.
En effet:

.. code-block:: python

    >>> "Le nombre que je préfère est le " + 5
    TypeError: Can't convert 'int' object to str implicitly

Python nous dit en effet qu'on ne peut pas additionner directement un entier et une chaine de caractère.
On dit en général que Python est un langage **fortement typé**, ce qui signifie que
les types des données doivent être cohérents pour pouvoir réaliser des opérations sur celles-ci (comme c'est le cas ici).

La conversion des données
-------------------------

Il est possible de convertir certaines valeurs d'un type en un autre type.
On utilise pour cela le nom du type, suivi de la valeur entre parenthèses.

Par exemple, si on veut transformer l'entier ``5`` en nombre à virgule (c'est-à-dire ``5.0``), on fera:

.. code-block:: python

    >>> float(5)
    5.0

On peut alors facilement faire le calcul qu'on voulait faire précédemment (appelé une *concaténation de strings*):

.. code-block:: python

    >>> "Le nombre que je préfère est le " + str(5)
    'Le nombre que je préfère est le 5'

Bien entendu, on ne peut pas faire de conversions insensées, sous peine de provoquer une erreur:

.. code-block:: python

    >>> float("Du texte")
    ValueError: could not convert string to float: 'Du texte'
