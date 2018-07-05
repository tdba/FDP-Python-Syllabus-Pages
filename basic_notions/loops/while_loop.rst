.. Cette page est publiée sous la license Creative Commons BY-SA (https://creativecommons.org/licenses/by-sa/3.0/fr/)

La boucle while
===============

La boucle suivante se retrouve dans la plupart des autres langages de programmation et porte le même nom. Elle permet de répéter un bloc d'instructions tant qu'une condition est vraie (*while* signifie « tant que » en anglais).

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

Vous remarquerez l'utilisation d'une variable qui servira de compteur. Celui-ci permet à la fois d'évaluer l'état d'avancement de la boucle mais aussi dans le cas présent de participer au calcul des valeurs.

A présent, voyons un peu ce que vous avez compris en mettant un peu en pratique:

.. inginious:: Factorial

L'un des plus gros points d'attention repose bien entendu sur la condition employée dans la boucle, en fonction de celle-ci vous pourriez vous retrouver avec *!6* au lieu *!5* par exemple, il est donc important de prêter attention au moment de la définir.

Un autre point intéressant est qu'avec une bonne condition on peut limiter le nombre d'itérations afin d'arriver à une réponse. Il s'agit clairement de faire de l'optimisation de programme (ce qui n'est clairement pas le focus de ce chapitre mais ça méritait d'être noté).

Réessayez avec l'exercice suivant en tentant de réduire votre nombre d'itérations.

.. inginious:: GD
    
