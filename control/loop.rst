.. Cette page est publiée sous la license Creative Commons BY-SA (https://creativecommons.org/licenses/by-sa/3.0/fr/)


===============
Répéter du code
===============

Les boucles constituent un moyen de répéter un certain nombre de fois des instructions de votre programme. Prenons un exemple simple, même s'il est assez peu réjouissant en lui-même : écrire un programme affichant la table de multiplication par 7, de 1 * 7 à 10 * 7.

.. code-block:: python

    print(" 1 * 7 =", 1 * 7)
    print(" 2 * 7 =", 2 * 7)
    print(" 3 * 7 =", 3 * 7)
    print(" 4 * 7 =", 4 * 7)
    print(" 5 * 7 =", 5 * 7)
    print(" 6 * 7 =", 6 * 7)
    print(" 7 * 7 =", 7 * 7)
    print(" 8 * 7 =", 8 * 7)
    print(" 9 * 7 =", 9 * 7)
    print("10 * 7 =", 10 * 7)

… et le résultat :

.. code-block:: python

    1 * 7 = 7
    2 * 7 = 14
    3 * 7 = 21
    4 * 7 = 28
    5 * 7 = 35
    6 * 7 = 42
    7 * 7 = 49
    8 * 7 = 56
    9 * 7 = 63
    10 * 7 = 70

La boucle while
===============

La boucle suivante se retrouve dans la plupart des autres langages de programmation et porte le même nom. Elle permet de répéter un bloc d'instructions tant qu'une condition est vraie (*while* signifie « tant que » en anglais). J'espère que le concept de bloc d'instructions est clair pour vous, sinon je vous renvoie au chapitre précédent.

La syntaxe de *while* est :

.. code-block:: python

    while condition:
        # instruction 1
        # instruction 2
        # ...
        # instruction N

A présent voici un code servant à afficher les tables de multiplications. Dans l'exemple de base il s'agit de la table de 7 mais vous êtes libres de jouer avec.

.. inginious-sandbox:: DummyScript

    nb = 7 # On garde la variable contenant le nombre dont on veut la table de multiplication
    i = 0 # C'est notre variable compteur que nous allons incrémenter dans la boucle

    while i < 10: # Tant que i est strictement inférieure à 10
        print(i + 1, "*", nb, "=", (i + 1) * nb)
        i += 1 # On incrémente i de 1 à chaque tour de boucle



Exercices:
==========

.. inginious:: GD

.. inginious:: Average
    
