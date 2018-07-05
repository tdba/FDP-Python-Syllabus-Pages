.. Cette page est publiée sous la license Creative Commons BY-SA (https://creativecommons.org/licenses/by-sa/3.0/fr/)

===========================
Représentation des données:
===========================

Enregistrer des données est à la base de la programmation.

Dans ce chapitre, nous abordons plusieurs manières d'enregistrer une suite de données dans des variables.

Les chaînes de caractères:
==========================

Les chaînes de caractères couramment appelées **strings**, sont des variables qui contiennent du texte.

.. code-block:: python

    x = "Bonjour!"

Les indices:
------------

On les appelles chaînes de caractères en français car on peut accéder à chacune des lettres individuellement. Grâce au '[]' on peut accéder à des lettres de la string, comme dans l'exemple qui suit:

.. inginious-sandbox:: DummyScript

    x = "Je préfère Charles à Kim."
    print(x[1])
    print(x[6])

Comme on peut le remarquer, **x[1]** affiche e. Ce qui nous indique bien que le compte des caractères d'une **string** commence toujours à 0. Par contre, si vous avez un peu expérimenté, vous avez remarqué qu'on peut aller dans les négatifs. Lorsqu'on va dans les négatif, on boucle sur la **string**. On a donc: print("ab"[-1]) qui va afficher b.

Les slices:
-----------

On peut également sélectionner des parties de string toujours avec les crochets.

.. inginious-sandbox:: DummyScript

    x = "Je préfère Kim à Charles."
    print(x[11:14])

Ici, vous pouvez remarquer que la borne inférieure est comprise mais pas la borne supérieure. De plus, on a quelques cas particuliers qu'on va discuter ensemble:

* On peut prendre des indices dépassant la longueur de la string. ``print("OpenWeek"[4:10000])`` va afficher "Week".
* On peut également aller dans les négatifs. Ici, ça se complique car on a encore 2 cas, dans ces deux cas, on peut pour descendre en dessous de l'opposé de la longueur:

  * *D'un nombre négatif à un nombre négatif* (0 non inclu), on prend alors de la lettre correspondante inclue (comme vu précédemment) à la lettre correspondante non inclue.  ``print("OpenWeek"[-8:-4])`` va afficher "Open".
  * *D'un nombre négatif à un nombre positif* (0 inclu), on ne prend en compte que les nombres positif et on fait comme si on commençait à 0. ``print("OpenWeek"[-8:4])`` va afficher "Open".

Les opérations:
---------------

On peut effectuer des opérations sur les strings. On peut les concaténer (mettre bout à bout) deux strings pour en avoir une nouvelle. On fait cela grâce à l'opération '+'.

.. inginious-sandbox:: DummyScript

    print("Coucou" + " " + "Tanguy!")
