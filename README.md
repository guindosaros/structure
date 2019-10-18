#  création et structure_django d'un projet django
Nous Allons Voir dans Ce Tutoriel comment Cree et Configurer un Projet Django
- Si Vous n'avez par python installer python3 sur votre ordinateur 
* Sur Votre ordinateur Cree un nouveau dossier ***dossier_django***
* ensuite ouvrir le dossier dans votre interpreteur de commande

#### 1- Creation de l'environnement virtuel 
* a l'interieur de votre dossier_django faire la commande suivante :
```bash
   dossier_django/
   ├─────────────── venv
```
* aprés avoir taper la commande vous aurez un dossier nouveau dossier ***venv*** l'interieur de votre ***dossier_django***
```pyhon
   python -m venv venv 
```
#### 2 - activation de la machine virtuel 
* sur mac os et linux 
```bash
  source venv/bin/activate
```
* Windows
```bash
  .\Scripts\activate
```
* aprés avoir activer notre environnement virtuel
 
#### 3 - installation de Django
```pyhon
   pip install django
```
* on peut cree notre premier project django
#### 4 - mise a l'emplace de la structure du projet 
*  l'interieur de votre dossier ***dossier_django***  cree un dossier firstproject :
```bash
   dossier_django/
   ├─────────────── venv
   ├─────────────── firstproject
```
*  l'interieur de votre dossier ***firstproject***  cree deux sous dossier static_cdn et media_cdn :
```bash
   dossier_django/
   ├─────────────── venv
   ├─────────────── firstproject
   │                ├── media_cdn
   │                ├── staic_cdn
```
 #### 5 creation du project django 
 *  l'interieur de votre dossier ***firstproject*** tape la commande suivante  :
```pyhon
   django-admin startproject my_project
```
*  a la suite de cette commande vous verez un nouveau dossier creee ***my_projectt*** contenant des dossier et fichier  :
```bash
   dossier_django/
   ├─────────────── venv
   ├─────────────── firstproject
   │                ├── media_cdn
   │                ├── staic_cdn
   │                ├── my_project/
   ├─────────────────  my_project/
   │                         ├── __inti__.py
   │                         ├── settings.py
   │                         ├── urls.py
   │                         ├── wsgi.py
   ├────────────────── manage.py 
```
