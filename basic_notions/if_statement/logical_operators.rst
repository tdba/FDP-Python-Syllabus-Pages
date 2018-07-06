.. Cette page est publiée sous la license Creative Commons BY-SA (https://creativecommons.org/licenses/by-sa/3.0/fr/)

====================
Opérateurs logiques
====================

Les operateurs logiques sont commes de operations arithmetic (+,-,*,/), dans le sens ou tu appliques les operateurs et il te calcule un resultat.
Dans l'arithmetic on calcule des valeurs commes des nombres (1+1) tant dis que les operateurs logiques evaluent des booléens. Et le resultat est d'une operation logique est lui aussi un booléen.

Un booléen en python s'écrit True et False. (bold)True est vrai en anglais et (bold)False est faux.

Les operateurs logiques sont and, or, not.
- X or(bold) Y: OU logique.
Si X est True (donc vrai) on evalue le tous en tant que vrai sinon c'est la valeur de Y (soite True ou False).
Donc il faut que au moins un des deux soit True pour être True

- X and(bold) Y : ET logique.
  Si X est évalué False, alors l'expression est False sinon c'est la valeur de Y.
  Donc il faut que les deux soit True pour être True.

- not(bold) X : NON logique.
  Sa évalue l'inverse donc si X est True on évalue False. Et inversement.

Les X et Y representent soite True ou False.

.. inginious-sandbox:: DummyScript

    print(True and True)
	print(True or False)
    print(not True)
    print(not False or True)
    print(not (False) or True)
    print(15 or 16) # ceci provoque une erreur vu que les elements sont des nombres et pas des booléens.


On peut print les evaluations de cet façon. 15 or 16 ne s'effectue pas parcequ'il ne sont pas des booléens et on travaille avec des operateurs logique.
print(not False or True) n'a pas le meme resultat vu l'ordre des priorités. C'est comme dans les arithmetic ou il faut un certain ordre 1+2*3 equivaut 7 et non 9.

L'ordre de priorité est d'abord les or puis les and et finalement les not.

Ici des tables de vérité afin de mieux comprendre les operateurs logiques.



=====  =====  ======  =======  =====
   Inputs         Output
------------  ----------------------
  X      Y    X or Y  X and Y  not Y
=====  =====  ======  =======  =====
False  False  False   False    True
True   False  True    False    True
False  True   True    False    False
True   True   True    True     False
=====  =====  ======  =======  =====
