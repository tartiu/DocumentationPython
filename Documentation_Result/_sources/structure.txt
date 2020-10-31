Structure d'un fichier Python
===================================================

Pour s'y retrouver lorsque plusieurs développeurs lisent un code, il faut s'imposer des règles.

Règles pour le nommage des variables
-----------------------------------------------

Pour nommer une variable en Python on préfèrera utiliser la séparation par des underscores.

**Exemple:**

	.. code-block:: python
	
		fichier = open("monfichier.txt", "rb")
		string_fichier = fichier.read()
		print(fichier)
		
Les noms de classe en Python respectent les caractéristiques suivantes :
	
	- Ils utilisent la camelCase
	- Ils commencent par une majuscule
	
.. code-block:: python
	
	class MaClasse():
	
Les noms de fonctions sont écrits de la même manière que les noms de variable.

	.. code-block:: python
	
		def string_to_int():
		
Règle pour construire un fichier Python
-------------------------------------------------

Pour éviter des conflits lors de l'importation de fichiers Python, il faut respecter une structure particulière de construction du fichier.
Si par exemple on souhaite avoir un script qui importe le contenu d'un fichier et qui traite ce fichier pour remplacer les caractères "è" par des "e".
Dans un script classique de Python on pourrait avoir les instructions suivantes:

	.. code-block:: python
	
		fichier = open("mon_fichier.txt", "rb")
		f_str = fichier.read()
		
		def remplacement(str):
			new_str = str.replace("è", "e")
			return new_str
			
		print(remplacement(f_str))
		
Le problème de ce fichier c'est qu'à chaque fois qu'on va vouloir l'importer dans un autre script python (par exemple pour réutiliser la méthode *remplacement*)
le code se rééxecutera et on aura le contenu de *mon_fichier.txt* qui s'affichera systématiquement dans la console.

Pour éviter ce problème on encapsule la fonction à executer dans une condition if de la manière suivante:

	.. code-block:: python
	
		def main():
			'''Fonction principale qui va s'executer quand on lancera le script
			'''
		
			#Execution du code
			fichier = open("mon_fichier.txt", "rb")
			f_str = fichier.read()
			
			#Affichage du résultat
			print(remplacement(f_str))
		
		#Fonction ecrit en dehors du main. Elle peut être importer facilement par un autre script
		def remplacement(str):
			'''Fonction qui remplace le caractère "è" par "e"
			
			Parameters
			-----------
			
			str : str
				Str où les caractères vont être remplacés
			
			Returns
			-----------
			new_str : str
				Retourne la chaine de caractère avec le caractère remplacés
			'''
		
			new_str = str.replace("è", "e")
			return new_str
			
		#Condition ultra importante pour éviter que le script s'execute lorsqu'on importe une fonction
		if __name__=="__main__":
			#Fonction que l'on veut exécuter lorsqu'on lance le script seul
			main()
			
Ligne de code indispensable
------------------------------------

Entre python 2.X et python 3.X il existe de grosses différences d'encodage des caractères et de la gestion de l'écriture des variables. Pour éviter tout problème
on n'utilise jamais ou très rarement python2 et python3 sur le même fichier. Généralement on choisit une version et on s'y tient. Néanmoins pour expliquer à Python l'encodage à utiliser
il faut systématiquement écrire tout en haut du fichier python la ligne suivante:

.. code-block:: python
	
	# -*- coding: utf-8 -*-
	
**PS:** Si t'as le choix, utilise python 3 !
			
			

