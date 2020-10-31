
Les librairies
==================

La force de python est de savoir qu'il existe de nombreuse librairies à disposition et facilement installable

Installer une librairie avec pip
----------------------------------------

Dans python il existe un module très pratique pour installer des librairies: l'outil *pip*.
Pour l'utiliser il y aura a mon avis deux cas de figure :
	- Tu n'utilises pas d'IDE comme Anaconda et tu dois tout faire en ligne de commande
	- Tu utilises un IDE comme Anaconda

Installation dans un terminal
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~	

Il faudra ouvrir un terminal. Que ce soit un terminal windows ou Linux d'ailleurs.

**Rappel** : sur windows pour ouvrir un terminal il faut faire la touche Windows + r et ensuite taper cmd et entrée sur linux le raccourci c'est souvent ctrl + alt + t

Une fois que le terminal est lancer tu peux directement vérifier si il y a python d'installer en tapant l'une de ces commandes suivante (je te mets pas le détail mais ca change 
selon le système d'exploitation donc essye et tu verras bien !)

	- :command:`python --version`
	- :command:`python3 --version`
	- :command:`py --version`
	- :command:`py3 --version`

Si tu as le choix privilégie une version de python 3.X.

Une fois que tu sais que python est installé tu peux installer n'importe quelle librairie avec la commande pip. Par exemple si tu veux installer numpy tu fais:
	:command:`pip install numpy`
	
Tu vas voir des lignes de code s'afficher et normalement numpy va s'installer (attention parfois faut confirmer en tapant un 'y' dans le terminal.

Installation dans un IDE
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~	

Dans un IDe, il doit y avoir normalement un endroit qui s'appelle 'console' ou 'terminal'. Si tu ne le trouves pas go check sur internet comment y accéder. Une fois que
tu es dedans tu peux directement écrire :command:`pip install mylibrairie`

Petite astuce, tu peux chercher sur internet "comment installer la librairie XXX" et bien souvent tu tombes sur des instruction avec pip.

Liste de librairie utiles:
-----------------------------------

Avec python on utilise très souvent certaine librairie que tu dois connaitre. Pour éviter que tu ne cherches trop longtemps je t'en mets quelques unes:

**Ps:** si la fonction est "*buildin*" alors tu n'as pas besoin de l'installer avec pip, juste de l'importer.

.. csv-table:: Liste de librairie
	:header: "Nom","utilité","importation courante", "buildin function"
	
	"Numpy", "Très pratique pour faire des calculs mathématique en tout genre", "import numpy as np", "non"
	"matplotlib.pyplot", "Très utile pour tracer des graphes (même en 3D !)","import matplotlib.pyplot as plt", "non"
	"seaborn","Ressemblant a pyplot mais est fait exprès pour visualiser des données de statistiques et des données en générales. Par exemple tu peux afficher plusieurs graph avec des
	axes différents sur une même feuille. Très pratique pour faire de la comparaison de graphe", "import seaborn as sb", "non"
	"pandas", "Indispensable pour faire des actions sur des fichiers csv", "import pandas as pd", "non"
	"sklearn", "Pratique pour faire des calculs statistique et du machine learning/IA","import sklearn as sk", "non"
	"os","Indispensable pour interagir avec le système (ex une clé usb, des actions directement dans le systeme etc)","import os", "oui"
	"sys", "S'utilise en interaction avec os, les 2 modules sont quais toujorus importé ensemble","import sys", "oui"
	"time", "Pratique pour calculer le temps entre deux ligne de code via l'instruction time.time()", "import time", "oui"
	"datetime", "S'utilise pour gérer les dates", "import datetime", "non"
	"csv", "S'utilise pour traiter les fichiers csv. Moins pratique que pandas mais plus léger à mettre en place si tu as un petit fichiers","import csv","oui"
	"pyModbus", "Permet de lire des informations en modbus", "import pydmodbus","non"
	"re","Module d'expression régulière. Permet de faire des recherche ultra rapide dans des grandes string","import re", "oui"
	"scapy","Bibliothèque pour faire du réseau informatique mais je ne la connais pas", "import scapy", "non"
	