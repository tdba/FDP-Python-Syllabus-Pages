.. Cette page est publiée sous la license Creative Commons BY-SA (https://creativecommons.org/licenses/by-sa/3.0/fr/)

Ouvrir un fichier
=================

Actuellement, tout ce que vous faites imprime du texte dans la console ou sauve des informations dans des variables, mais rien n'est permanent.

Pour stocker des informations de manière permanente et pour pouvoir les récupérer plus tard il faut utiliser des fichiers.

La première chose à faire pour cela est ouvrir le fichier. En effet il n'est pas autorisé d'écrire ou de lire un fichier sans l'avoir ouvert au préalable.

Attention, après avoir ouvert un fichier, il faut le refermer!

Il existe une limite au nombre de fichier qui peuvent être ouvert simultanément, donc oublier de refermer les fichiers fera planter le programme plus tard.

Il y a deux méthodes principales pour ouvrir et fermer un fichier correctement:


.. code-block:: python

    with file_object as open("filename.txt"):
        # your code here
        # file_object contient le descripteur de fichier
    # le fichier n'est plus ouvert ici

À l'intérieur du block qui commence avec "with", le fichier "filename.txt" est ouvert et la variable "file_object" contient un *objet*
(on reviendra sur les objets plus tard dans le cours) qui permet de faire des opérations sur le fichier, comme le lire ou écrire dedans.

Cette méthode (avec with) est pratique car il est impossible d'oublier de fermer le fichier. Il se ferme lorsqu'on sort du block d'indentation du with.

L'autre méthode est d'ouvrir et fermer le fichier explicitement.

.. code-block:: python

    file = open("filename.png") # n'importe quel type de fichier peut être ouvert, png, txt ou même sans aucune extension
    #your code here
    file.close()
    # le fichier n'est plus ouvert ici

De nouveau le fichier est stocké dans un objet (ici nommé "file").

Les modes d'ouverture
---------------------

Les fichiers peuvent être ouvert dans divers modes, dont le mode "read only", le more "write only" etc...

Par défaut, il sont ouvert en mode *read only* et il est donc impossible d'écrire dedans.

On peut ajouter un paramètre à la fonction "open()" pour changer le mode d'ouverture.

Example:

.. code-block:: python

  with file_object as open("filename.txt", "w"): #On a ajouté un "w" dans les paramètres de fonction
      # your code here
  # le fichier n'est plus ouvert ici

Le "w" mis comme deuxième paramètre dans la fonction open permet de l'ouvrir en mode "write only"


Les différent modes disponibles sont:

* "r" Lecture seulement
* "w" Écriture seulement, attention, le contenu du fichier sera remplacé (tout ce qui était avant disparaît)
* "r+" Lecture et écriture
* "w+" Lecture et écriture, de plus le fichier est créé s'il n'existe pas

Les modes suivant dépendent de l'emplacement du curseur lorsqu'on ouvre le fichier.
Le curseur correspond à l'endroit où on se trouve dans le fichier. Si le curseur est à la fin et qu'on fait un "write" on écrira à la fin du fichier.
Les opérations commencent à l'emplacement du curseur.

* "a" Écriture seulement, de plus le curseur est placé à la fin du fichier
* "a+" Écriture et lecture, de plus le curseur est placé à la fin du fichier
