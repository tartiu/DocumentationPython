Les classes en Python
=================================

Les classes Python sont vraiment très utiles pour stocker plusieurs informations différentes les unes des autres. Un peu à la manière d'un dicitonnaire
sauf que la on peut rajouter des actions et des méthodes à effectuer pour traiter des informations.

Rappel de la syntaxe des classes Python
-----------------------------------------------

Avant de démarer, je te conseille vivement de lire la section :doc:`comment` pour commenter correctement tes classes si tu en as besoin.

Rappel, dans une classe il y a des atributs, des méthodes (avec souvent des "getters and setters" pour avoir la valeur des attribut ... En python pas besoin),
un constructeur.

En Python il n'y a pas beosin de getters and setters car on peut directement accéder à l'attribut d'une classe par l'instruction suivante:

.. code-block:: python

	#Construction de l'objet de la classe Class
	class = Class()
	
	#Affichage de l'attribut
	attribut = class.attribut1
	
La classe se définit avec l'instruction suivante :

.. code-block:: python

	class MyClassSensor():
		'''Commentaire pour expliquer la classe
		'''
		
		#attribut de la classe
		id = 0
		nom = "bonjour"
		defaults = [1, 6, 7]
		
Pour une classe il faut toujours un constructeur ! En python il se déclare avec une méthode particulière "__init__"

.. code-block:: python

	class MyClassSensor():
		'''Commentaire pour expliquer la classe
		'''
		
		#attribut de la classe
		id = 0
		nom = "bonjour
		defaults = [1, 6, 7]
		
		def __init__(self, nom, default):
			'''Constructeur avec un nom et des defaults
			'''
			self.id = class.id + 1
			self.nom = nom
			self.default = [default]
			
Tu remarques surement l'apparition du mot clé "self" et "class" le mot clé class fait référence à tous les instances de ta classe. En fait c'est un attribut de classe.
Ici par exemple, à chaque fois qu'une instance de MyClassSensor est créée, l'attribut id commun a toutes les instances de la classe est augmenté. Donc avec cette instruction :

.. code-block:: python

	self.id = class.id +1

l'id de la précédente instance (class.id) est récupéré puis incrémenté de 1 et affecté à la valeur d'id de cette instance en particulier.

L'instruciton self par contre permet de faire référence non plus à la classe mais à l'instance elle même. En gros tu vas dire que l'attribut nom de cette instance en particulier
et maintenant celui donné en paramètre.

**Bon à savoir** : quand tu crées une méthode dans une classe, tu dois très souvent réutiliser les attributs et donc faire référence à l'instance elle même. C'est pour ca qu'il faut quasi 
toujours la mettre en paramètre de ta fonction.

.. code-block:: python

	class MyClassSensor():
		'''Commentaire pour expliquer la classe
		'''
		
		#attribut de la classe
		id = 0
		nom = "bonjour
		defaults = [1, 6, 7]
		
		def __init__(self, nom, default):
			'''Constructeur avec un nom et des defaults
			'''
			self.id = class.id + 1
			self.nom = nom
			self.default = [default]
			
		def changeName(self, name):
			'''Change le nom de l'instance
			'''
			
			self.name = name
			
		def addDefault(self, default):
			'''Ajoute un defaut a la liste
			'''
			
			self.defaults.append(default)
			
Et même dans tous les cas, pour appeler ta méthode tu dois passer par ton instance. Ce qui donnera une instruction dans ce style :

.. code-block:: python

	#default
	defaut = 1
	
	#Créer un capteur
	instance = MyClassSensor("nom", defaut)
	
	#Applique des méthodes au capteur
	instance.changeNome("nom plus cool")
	instance.addDefault(3)
	
	#Affiche le nom et la liste des defauts du capteur
	print(instance.nom)
	print(instance.defaults)
	
Appel et utilisation d'une classe
----------------------------------------

Souvent les classes Python sont écrites dans leur propre fichier appelé *nom_class.py*.
Ensuite, lorsque l'ont veut utiliser la classe on créer un autre fichier python par exemple *run.py* et on importe la classe. 

**PS** : n'oublie pas la structure des fichiers Python apprise ici : :doc:`structure` !

Voici le contenu du fichier run.py

.. code-block:: python

	# -*- coding: utf-8 -*-
	
	from nom_class.py import NomClass
	
	def main():
		instance = NomClass()
		print(instance.attribut)
		
	if __name__ == "__main__":
		main()
			