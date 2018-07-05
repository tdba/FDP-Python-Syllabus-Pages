.. Cette page est publiée sous la license Creative Commons BY-SA (https://creativecommons.org/licenses/by-sa/3.0/fr/)

La fonction print
=================

La fonction print permet d'afficher du texte dans la console.

La syntaxe est très simple, par exemple:

.. inginious-sandbox:: hello-world

    print("Hello World!")

Va imprimer le texte entre guillements (dans ce cas-ci: *Hello World!*) dans la console.
À noter que les guillemets simple et double sont interchangable print('Hello World!') et print("Hello world!") ont le même effet.

Certain charactères doivent être précédés d'un backslash car autrement ils ont un effet spécifique

* \\n permet de sauter à la ligne
* \\t permet de faire une tabulation
* \\" permet d'inclure un charactère "
* \\\\ permet d'inclure un backslash

Il en existe d'autres, mais inutile de les connaître tous par cœur, ceux-ci sont les plus commun et lorsque quelque chose ne s'imprime pas correctement,
essayez de mettre un backslash devant, il s'agit peut-être d'un autre charactère avec un effet spécifique.
Entrainez vous en essayant d'imprimer dans la console le texte suivant

  | "Bonjour,
  | Ceci "est" une
  |     tabulation
  | Monsieur\\Madame\\\\
  | Au revoir"

.. inginious-sandbox:: training

Il est possible bien sur d'en mettre plusieurs à la suite

.. inginious-sandbox:: several-print

    print("Hello")
    print("World")
    print("!")

Auquel cas le résultat de chaque print sera sur une ligne séparée

D'autres possibilitées de la fonction print:

On peut séparer les textes qu'on veut print par des virgules, le résultat est qu'ils seront imprimés séparément avec un espace entre chaque texte:

.. inginious-sandbox:: several string

    print("Hello", "World", "!")

On peut changer ce qui est imrpimé à la fin du print. Par défaut il s'agit d'un retour à la ligne, mais on peut mettre autre chose:

.. inginious-sandbox:: end

    print("Hello", end="\t")
    print("World", end="!\n")

Voilà, vous conaissez maintenant les bases de la fonction print. Vous verrez plus tard certaines autre fonctionnalitées telles que ".format",
mais même sans ça vous découvrirez bien vite à quel point il est pratique de pouvoir imprimer des choses dans la console.
