Commentaire
===============

Il est très important que tu commentes ton code. Tu n'es pas obligé de faire de la documentation avec les normes (même si je te le conseille)
mais tu dois au minimum commenter tes boucles for/while, tes if ou même tes lignes de code compliquées au cas ou quelqu'un d'autre relise ton code 
ou même si toi tu veux revenir dessus plus tard.

Plusieurs types de commentaire
-----------------------------------

Il est important de bien commenter sa page python. En Python il existe 2 types de commentaire différent :

	- les docstrings qui démarrent par le caractère """ ou '''	
		.. code-block:: python
		
			"""Je suis une docstring"""
			'''Je suis une autre manière d'écrire les docstrings'''
			
	- les commentaires classiques qui démarrent par le caractère #
		.. code-block:: python
		
			#Je suis un commentaire classique
			
Les docstring sont faits pour écrire des longs commentaires et les commentaires classiques pour ajouter une précision sur le code.

Normes pour commenter
------------------------
En Python un outil très pratique permet de faire de la documentation automatiquement, le module Sphinx. Il a d'ailleurs été utilisé pour écrire cette documentation et beaucoup de documentation officielle
que l'on trouve sur internet. Pour créer une documentation Sphinx lit les docstrings présentes dans le code Python. Il faut donc qu'elles soient écrites avec une norme et une structure
particulière.

En Python il existe 2 normes :

	- La norme **Numpy docstring**
	- La norme **Google docstring**
	
Example de norme numpy
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

L'example ci-dessous a été rédigé par moi. Pour avoir un exemple officiel suis ce lien :
https://numpydoc.readthedocs.io/en/latest/format.html

.. code-block:: python

	'''Author : A.DUPONT
	date : 31/10/20
	
	This code is usefull to read and write in a specific sensor
	'''
	
	import os
	import pandas
	import pyModbus
	
	class ImportData():
		'''
		This class is used to import data from the sensor XXX
		
		Attributes
		-----------
		sensor_adress : str
			Correspond to the sensor IP adress
		sensor_id : int
			Correspond to the sensor ID
			
		Methods
		---------
		connect_to_sensor()
			Create a link with the sensor
		translate_data(str data)
			Translata data from a protocole to an other
		'''
		
		sensor_adress = "192.168.0.1" #Adress IP du capteur
		sensor_id = 10
		
		def connect_to_sensor():
			'''Example of a function to connect to a sensor
			
			This function use the pyModbus Librairy to connect to a sensor thanks to an ip adress
			
			Parameter
			-----------
			None
			
			Returns
			---------
			None
			'''
			pyModbus.connect(this.sensor_adress)
			print("Connected to device",this.sensor_adress)
			
		def translate_data(data):
			'''Example of a function to translate data from a protocole to an other
			
			This function use external librairy to translate data from a protocole to an other
			with the data to translate in Parameter. Data need to be a String type.
			
			Parameters
			-----------
			data : str
				data to translate. Needs to be a str
				
			Returns
			-----------
			data_translated : str
				data translated thanks to the librairy
			'''
			
			data.translate() = data_translated
			return data_translated

Example de norme Google
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

L'example ci-dessous a été rédigé par moi. Pour avoir un exemple officiel suis ce lien :
https://sphinxcontrib-napoleon.readthedocs.io/en/latest/example_google.html#example-google

.. code-block:: python

	'''Author : A.DUPONT
	date : 31/10/20
	
	This code is usefull to read and write in a specific sensor
	'''
	
	import os
	import pandas
	import pyModbus
	
	class ImportData():
		'''
		This class is used to import data from the sensor XXX
		
		Attributes
		-----------
			sensor_adress(str): Correspond to the sensor IP adress
			sensor_id(int): Correspond to the sensor ID
			
		Methods
		---------
		connect_to_sensor()
			Create a link with the sensor
		translate_data(str data)
			Translata data from a protocole to an other
		'''
		
		sensor_adress = "192.168.0.1" #Adress IP du capteur
		sensor_id = 10
		
		def connect_to_sensor():
			'''Example of a function to connect to a sensor
			
			This function use the pyModbus Librairy to connect to a sensor thanks to an ip adress
			
			Args
			-----------
			None
			
			Returns
			---------
			None
			'''
			pyModbus.connect(this.sensor_adress)
			print("Connected to device",this.sensor_adress)
			
		def translate_data(data):
			'''Example of a function to translate data from a protocole to an other
			
			This function use external librairy to translate data from a protocole to an other
			with the data to translate in Parameter. Data need to be a String type.
			
			Args
			-----------
				data (str) : data to translate. Needs to be a str
				
			Returns
			-----------
				data_translated (str) : data translated thanks to the librairy
			'''
			
			data.translate() = data_translated
			return data_translated