.. Cette page est publiée sous la license Creative Commons BY-SA (https://creativecommons.org/licenses/by-sa/3.0/fr/)

==========================
Structures conditionnelles
==========================

Après avoir testé des instructions d'une façon linéaire : l'interpréteur exécutait au fur et à mesure le code saisi dans la console. Mais il ya moyen d'enrichir nos programmes en demandant à exécuter certaines instructions dans un cas, et d'autres instructions dans un autre cas.

Dans ce chapitre, nous parlerons des structures conditionnelles, qui vont permettre de réaliser des tests et d'aller plus loin dans la programmation.

Les conditions permettent d'exécuter une ou plusieurs instructions dans un cas, d'autres instructions dans un autre cas.

L'intruction *if*:
==================

L'instruction if permet d'exécuter le code se trouvant en dessous de lui si la condition est validée.

La syntaxe de *if* est :

.. code-block:: python

    if condition:
        # instruction 1
        # instruction 2
        # ...
        # instruction N
		
Vous remarquez que les instructions apparetenant se déclenchant dans le cas où la condition est validée sont toutes indentées d'un cran en plus par rapport à l'indentation du *if*. Ces éléments d'avantages indentés appartiennent au bloc d'instruction de la condition et ne seront exécutés que si celle-ci est validée. Cela permet notamment de faire la différence entre du code devant s'exécuter dans tous les cas et du code qui ne s'exécutera que si la condition est validée. 

Comme on apprend toujours mieux par l'exemple je vous propose d'exécuter le code suivant pour voir ce qu'il print puis de passer la condition de *True* à *False* et de relancer l'exécution pour observer le fonctionement de l'instruction.

.. inginious-sandbox:: DummyScript

    if True:
		print("Je suis dans la condition.")
	print("Ceci est un test.")
	
	
A présent vous pouvez vous exercer sur une tâche réelle!

.. inginious:: Min

L'intruction *else*:
====================

Le mot-clé *else*, qui signifie « sinon » en anglais, permet de définir une première forme de complément à notre instruction *if*.

.. code-block:: python

    if condition:
        # instruction 1
	else:
        # instruction 2

L'intruction *elif*:
====================

Le mot-clé *elif*,est une contraction de « else if », que l'on peut traduire très littéralement par « sinon si ». Avec celle-ci nous pouvons à présent avoir une forme complète pour nos conditions.

.. code-block:: python

    if condition 1:
        # instruction 1
	elif condition 2:
        # instruction 2
	else:
		# instruction 3
		
Avec toutes ces informations vous devriez pouvoir vous occuper de l'exercice suivant assez facilement:
		
.. inginious:: Median

L'astuce: operateur ternaire:
=============================

Afin de gagner quelques lignes, des aménagements sont possibles:

.. code-block:: python

    # instruction 1 if condition else instruction 2
	
.. inginious-sandbox:: DummyScript

    # Essayez vous-même !

