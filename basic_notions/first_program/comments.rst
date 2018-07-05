.. Cette page est publiée sous la license Creative Commons BY-SA (https://creativecommons.org/licenses/by-sa/3.0/fr/)

Les commentaires
================

Parfois, les programmeurs souhaites expliquer leur code, ou bien inclure des informations qui ne seront pas exécutées dans leurs fichier de code.

Pour cela, il est possible d'inclure des commentaires.

Il existe deux manières de faire des commentaires.

Tout d'abord les commentaires sur une seule ligne, qui vont transformer tout ce qui les suit dans la ligne en commentaire.

En python, ils commencent par le charactère #

Par exemple:

.. inginious-sandbox:: DummyScript

  #commentaire
  print("hello")  #world

comme vous pouvez le voir, tout ce qui est après le # est ignoré.

Si le # se trouve entre guillemets, il ne commencera pas un commentaire, mais sera considéré comme un charactère comme un autre.

.. inginious-sandbox:: DummyScript

  print("dièse: #")  # Le # à l'intérieur du print est ignoré car il est entre guillemets

Toutefois bien que très pratique, ce type de commentaires ne transforme qu'une seule ligne en commentaire.

Pour faire un commentaire sur plusieurs lignes, il existe des commentaires multilignes, qui sont entourés de """ (trois guillemets, simple ou double)

Attention, il y a une limitation à ce type de commentaire: Il ne peuvent pas être sur la même ligne que du code.


.. inginious-sandbox:: DummyScript

    """ceci est un commentaire
    sur plusieurs lignes"""

Vous verrez que parfois ça peut être très sympa d'avoir du code avec des commentaires expliquant son fonctionnement.
Les collègues/membres de groupe qui commentent leur code ont tendance à être plus appréciés.
