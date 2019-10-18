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
   ├──────────────────  manage.py 
```
*  cree deux dossier ***templates*** et ***static***  dans ***my_projectt***  
```
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
   ├──────────────────  manage.py 
   ├────────────────── templates
   ├──────────────────  static
```
#### 6 Configurations des fichier du projet
   ###### dans le settings.py
    * copier ce code a la fin aprés le commentaire  import static
  ```python
     # Static files (CSS, JavaScript, Images)
      # https://docs.djangoproject.com/en/2.2/howto/static-files/
      STATIC_URL = '/static/'
      STATICFILES_DIRS = [os.path.join(BASE_DIR, 'static')]
      MEDIA_URL = '/media/'
      MEDIA_ROOT = os.path.join(BASE_DIR, '../media_cdn')
      STATIC_ROOT = os.path.join(BASE_DIR, '../static_cdn')
  ```
     * dans la partie TEMPLATES: DIRS': []  remplace par ['templates']  on aura :
     ```python
     TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': ['templates'],
        'APP_DIRS': True,
        'OPTIONS': {
            'context_processors': [
                'django.template.context_processors.debug',
                'django.template.context_processors.request',
                'django.contrib.auth.context_processors.auth',
                'django.contrib.messages.context_processors.messages',
            ],
        },
    },
]
  ```
