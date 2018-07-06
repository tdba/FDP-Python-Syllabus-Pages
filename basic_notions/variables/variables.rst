.. Cette page est publiée sous la license Creative Commons BY-SA (https://creativecommons.org/licenses/by-sa/3.0/fr/)

Les variables
=============

Jusqu'à maintenant, nous n'avons utilisé Python que pour faire des calculs comme une calculatrice pourrait le faire,
et pour afficher les résultats de ces calculs. Cependant, après leur affichages, tous nos résultats sont perdus.
Nous allons ici voir comment stocker les résultats de ces calculs (ou d'autres informations): les variables.

Ce concept se retrouve dans énormément de langages de programmation.

Qu'est-ce qu'une variable? Avant toute chose, il faut remettre en contexte certaines choses.
Grosso modo, un ordinateur est comme une calculatrice très rapide avec une grande mémoire.
On peut voir cette mémoire comme un ensemble de cases qui vont contenir différentes valeurs (qui peuvent varier).
Les variables permettent de manipuler une ou plusieurs de ces cases de mémoires, et par conséquent, les valeurs qu'elles contiennent.

*Note: ceci est une façon extrêmement simplifiée de voir un ordinateur.*

On peut voir une variable comme une étiquette que l'ordinateur colle a une de ces cases de mémoire.
De cette façon on pourra facilement demander à l'ordinateur d'y stocker une valeur
ou de récupérer la valeur qui y est stockée.

Concrètement, on va créer une variable et lui donner une valeur de la façon suivante: ``nom_de_variable = valeur``.
Par exemple:

.. code-block:: python

    >>> a = 7

Ici, on a créé une variable appelée ``a`` et qui contient la valeur ``7``. D'un point de vue vocabulaire,
on appelle ``a`` l'**identificateur** de la variable, ou plus simplement son **nom**, et 7 sa **valeur**.
La création d'une variable est appelée une **déclaration**. Lui donner une valeur est une **affectation**.

*Note: les espaces autour du symbole ``=`` sont facultatifs.*

Nous ne sommes maintenant plus obligés de faire des calculs uniquement sur des valeurs en elles-mêmes!
Notez qu'on peut rapprocher cela des notations mathématiques. Par exemple, on va ici calculer l'aire d'un rectangle
quelles que soient sa largeur et sa hauteur:

.. code-block:: python

    >>> # On va d'abord déclarer la largeur et la hauteur
    >>> largeur = 5.5
    >>> hauteur = 3.0
    >>> # On calcule ensuite l'aire du rectangle
    >>> aire = largeur * hauteur

En changeant les valeurs de ``largeur`` et ``hauteur``, on peut facilement calculer l'aire de différents rectangles
sans avoir à réécrire la formule de l'aire.

Vous pouvez donc voir qu'on **déclare** et **affecte** une variable en utilisant le symbole ``=``.
On récupère (et utilise) ensuite sa valeur à partir de son nom.

Il est aussi possible d'affecter deux variables en une seule ligne, comme suit:

.. code-block:: python

    >>> largeur, hauteur = 5.5, 3.0  # `largeur` vaut 5.5 et `hauteur` 3.0

Bien sûr, si on essaye d'utiliser une variable non-déclarée, une erreur se produit:

.. code-block:: python

    >>> # La variable `non_declaree` n'a pas ete declaree
    >>> a = non_declaree + 1
    NameError: name 'non_declaree' is not defined

Comme le mot "variable" nous le dit, il est possible de changer la valeur d'une variable. On appelle cette opération
une **réaffectation**:

.. code-block:: python

    >>> # On declare une variable affectee a une certaine valeur
    >>> hello = "hello"
    >>> # On reaffecte la variable
    >>> hello = "bonjour"

Les types des variables
-----------------------

Comme pour les données, une variable a (forcément) un type, qui correspond au type de sa valeur.
On peut le retrouver exactement comme on l'a fait précédemment:

.. code-block:: python

    >>> age = 12
    >>> type(age)
    <class 'int'>
    >>> hello = "Hi!"
    >>> type(hello)
    <class 'str'>

Les opérations entre différentes variables sont soumises aux mêmes règles que pour les valeurs, comme on peut le voir dans cet exemple:

.. code-block:: python

    >>> hello = "Hello, "
    >>> name = "Dave"
    >>> hello + name
    'Hello, Dave'
    >>> number = 17
    >>> hello + number
    TypeError: Can't convert 'int' object to str implicitly

À noter qu'une réaffectation peut changer le type d'une variable:

.. code-block:: python

    >>> var = 6.28
    >>> type(var)
    <class 'float'>
    >>> var = "slt"
    >>> type(var)
    <class 'str'>

Les règles et conventions de nommage
------------------------------------

Il est évidemment très important de connaitre les règles et conventions qui régissent le monde des variables en Python.
Vous ne voudriez pas que votre programme plante parce que vous auriez mal nommé une variable, ou pourrir votre réputation
de programmeur en utilisant des noms de variables qui ne sont du gout de personne.

Pour être valide, une variable doit avoir un nom composé uniquement des caractères suivants:

* des lettres (minuscules ou majuscules)

* des chiffres sauf en première position

* des underscores (_)

Donc, ``variable``, ``LOL`` et ``youpi_8`` sont des noms de variables valides, tandis que ``5eme``, ``une variable``, ou ``5*3`` n'en sont pas.
Faites-y attention car utiliser un nom de variable invalide peut vous retourner des erreurs difficiles à comprendre:

.. code-block:: python

    >>> nom-invalide = 8
    SyntaxError: can't assign to operator

Il est à noter qu'on déconseille d'utiliser des lettres accentuées dans vos noms de variables, car cela pourrait poser
des problèmes d'encodage sous certains systèmes.
En général, il est considéré comme bonne pratique de nommer ses variables en anglais (et donc sans accents).

Python fait aussi la différence entre des lettres majuscules et minuscules: ``variable``, ``Variable``, ``VARIABLE`` et ``VARiable``
sont donc considérées comme 4 variables différentes.

Il existe également un certain nombre de mots réservés par Python, et qui ne peuvent donc pas être des noms de variables.
En voici une liste exhaustive:

+--------------+-----------------+--------------+--------------+-----------+
| False        | await           | else         | import       | pass      |
+--------------+-----------------+--------------+--------------+-----------+
| None         | break           | except       | in           | raise     |
+--------------+-----------------+--------------+--------------+-----------+
| True         | class           | finally      | is           | return    |
+--------------+-----------------+--------------+--------------+-----------+
| and          | continue        | for          | lambda       | try       |
+--------------+-----------------+--------------+--------------+-----------+
| as           | def             | from         | nonlocal     | while     |
+--------------+-----------------+--------------+--------------+-----------+
| assert       | del             | global       | not          | with      |
+--------------+-----------------+--------------+--------------+-----------+
| async        | elif            | if           | or           | yield     |
+--------------+-----------------+--------------+--------------+-----------+

Il est interdit d'utiliser ces mots comme noms de variable. Le faire produira une erreur.

En Python, il existe enfin des conventions par rapport à la façon dont vous nommez vos variables. Cela signifie que vous n'êtes
pas obligé de suivre ces conventions (ça ne provoquera pas d'erreur), mais que c'est considéré comme une bonne pratique
(ça permettra aux autres de lire votre code plus facilement). Ces conventions s'appliquent quand le nom d'une variable
est constituée de plusieurs mots.

Là où d'autres langages utilisent un format qu'on appelle le *camelCase* (où chaque mot sauf le premier a une majuscule),
Python préfère qu'on nomme les variables en utilisant le *snake_case* (où les mots sont séparés par des underscores et
n'ont pas de majuscules).

On nommera donc une variable plutôt ``my_great_variable`` que ``MYGREATVARIABLE`` ou ``maSuperVariable``.

Vous pouvez lire la *PEP8* sur le site officiel de Python (en anglais) pour plus d'informations.

Opérateurs spécifiques aux variables
------------------------------------

Si on vous demandait d'ajouter ``1`` à la variable ``number`` préalablement déclarée (opération qu'on appelle une **incrémentation**),
vous feriez sans doute ceci:

.. code-block:: python

    number = number + 1

Ce genre d'opération se fait *très* souvent en Python. On a donc créé des opérateurs qui nous permettent de l'écrire plus rapidement.
Le code suivant fait la même chose que celui présenté ci-dessus:

.. code-block:: python

    number += 1

L'opérateur ``+=`` permet d'ajouter un certain nombre à la variable.
Des opérateurs similaires existent pour d'autres opérations:

=========================  ==============
Opération                   Opérateur
=========================  ==============
Addition                    ``+=``
-------------------------  --------------
Soustraction                ``-=``
-------------------------  --------------
Multiplication              ``*=``
-------------------------  --------------
Division                    ``/=``
-------------------------  --------------
Division entière            ``//=``
-------------------------  --------------
Modulo (reste)              ``%=``
-------------------------  --------------
Puissance                   ``**=``
=========================  ==============

De nouveau, les espaces autour de l'opérateur sont facultatifs.
