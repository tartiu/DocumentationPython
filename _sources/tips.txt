Tips Python
===================================================

Tips pour utiliser Python efficacement

Un type de variable très utile : les dictionnaires !
-------------------------------------------------------------

En Python tu peux utiliser les variables de type classique (int, float, str, list, ...) mais aussi des type propre à Python comme les dictionnaires (dict).
Ce type de variable est très pratique lorsque tu veux stocker des informations de types différents et y accéder rapidement. Le fonctionnement du dictionnaire est simple,
il marche par système de clé et de valeur et se déclare entre accolade ({}) contrairement au liste qui se déclare en crochet ([]). La clé doit toujours être une string
et la valeur peut être de n'importe quel type (liste, str, int, float) et cela indépendemment des autres types de valeur de ton dictionnaire.

.. code-block:: python

	#déclaration de valeur
	valeur1 = "salut"
	valeur2 = [10, 29, "str", 2.0]

	#dictionnaire vide
	dictionnaire = {}
	
	#dictionnaire non vide avec deux paire "clé/valeur"
	dictionnaire = {"cle1": valeur1, "cle2", valeur2}
	
Une fois que ton dictionnaire est déclaré, tu peux facilement accéder à la valeur que tu veux en utilisant la bonne clé:

..code-block:: python

	#Appelle d'un dictionnaire pour afficher la valeur1
	print dictionnaire["cle1"]
	
Dans l'exemple ci-dessous, "salut" est écrit dans le terminal

Exemple
~~~~~~~~~~

Mettons par exemple qu'on dispose
d'une liste de capteurs et que pour chaque capteur on dispose d'une information à stocker avec ce capteur en particulier. Le code s'écrira de la façon suivante:

.. code-block:: python

	#Liste de capteurs
	capteurs = read_list_capteur()
	
	#liste vide pour stocker les informations de capteurs et le capteur
	capteur_et_info = []
	
	#boucle pour lire l'infos remontant de chaque capteur et l'ajouter dans une liste
	for capteur in capteurs:
	
		#Lecture de l'info dans le capteur
		infos_capteur = read_infos(capteur)
		
		#Création d'un dictionnaire
		dictionnaire = {"capteur" : capteur, "infos": infos_capteur}
		
		#ajout dans la liste du dictionnaire
		capteur_et_info.append(dictionnaire)
		
	#Affichage des infos et du capteur pour chaque capteur dans la liste
	for dictio in capteur_et_info:
		print("L'informations " + str(dictio["capteur"]) + " a été lu dans " + str(dictio["capteur"]))
		
Attention aux caractères spéciaux
---------------------------------------

Tout est dans le titre ... En anglais tout est sans accent, du coup évite au maximum d'écrire en français ou alors fait le sans accent (pas de à, é, è, ç, °, ...).
Cette règle est valable aussi bien pour les commentaires de ton script, les noms de fichier que tu vas utiliser et même le contenus des fichiers que tu vas utiliser !!

Les classes !
-----------------

Vraiment très utile en Python mais rarement utilisé, les classes te permettent de faire des objets avec des caractéristiques bien rangé et d'accéder rapidement aux informations
que tu veux stocker. Penses à les utiliser et n'hésite pas à te renseigner sur la page classe de ce docuement. (:doc:`classe`)

Print
--------

Utiliser l'instruction print est très pratique mais doit se faire avec parcimonie. Exemple attention à bien utiliser des types str dans l'affichage !

Il existe d'ailleurs plusieurs manières d'afficher avec print:

	1. L'affichage pour une seul variable avec du texte 
	.. code-block:: python
		
		#option 1
		print("Texte à afficher :" + str(variable))
		
		#option 2
		print("Texte à afficher :", variable)
		
	2. L'affichage de plusieurs variables
	.. code-block:: python
	
		#option 1
		print("Variable 1 :" + str(var1) + "Variable 2 :" + var2)
		
		#option 2
		print("Variable 1 : {}, Variable 2 : {}".format(var1, var2))
		
		#option 3 (je la maitrise pas bien et elle est plus trop utilisé ...
		print("Variable 1 : %i, %s, %d"(1, 2.0, "string"))
	
		
		


