# EdocTApp - Application Médicale Django + Angular

## 📋 Description

EdocTApp est une application web médicale complète intégrant :

- Backend : API Django avec Django REST Framework et JWT
- Frontend : Application Angular moderne
- Base de données : MySQL via MAMP

## 🏗️ Structure du projet

EdocTApp/
├── backend/                 # API Django
│   ├── api/                # Application principale
│   ├── backend/            # Configuration Django
│   └── manage.py
├── frontend/               # Application Angular
│   └── EdoctApp/
├── requirements.txt        # Dépendances Python
└── README.md

## 🚀 Installation et Configuration

### Prérequis
- Python 3.8+
- Node.js 16+
- MAMP (pour MySQL)
- Git
### 1. Cloner le projet

git clone https://github.com/Omar-NGOM/E-doctApp.git
cd EdocTApp

## Solution pour Augmenter la taille du buffer Git

# Augmenter la taille du buffer HTTP
git config http.postBuffer 524288000

# Augmenter le timeout
git config http.lowSpeedLimit 0
git config http.lowSpeedTime 999999

# Faire maintenant le push
git push -u origin main

### 2. Configuration du Backend (Django)
#### 2.1 Créer et activer l'environnement virtuel

   # Créer l'environnement virtuel
   python -m venv venv

   # Activer l'environnement (macOS/Linux)
   source venv/bin/activate

   # Activer l'environnement (Windows)
   venv\Scripts\activate

#### 2.2 Installer les dépendances

pip install -r requirements.txt

## 2.3 Configuration de la base de données

1. Démarrer MAMP et s'assurer que MySQL fonctionne sur le port 8889
2. Créer la base de données :
   - Aller sur http://localhost:8888/phpMyAdmin/
   - Créer une base de données nommée edoctapp_db 

## 2.4 Migrations de la base de données

cd backend
python manage.py makemigrations
python manage.py migrate

## 2.5 Créer un superutilisateur Django

python manage.py createsuperuser

Suivez les instructions pour créer votre compte administrateur :

- Nom d'utilisateur : admin (ou votre choix)
- Email : votre@email.com
- Mot de passe : (choisissez un mot de passe sécurisé) 

## 2.6 Lancer le serveur Django

python manage.py runserver

✅ Le serveur sera accessible à : http://127.0.0.1:8000/

## 3. Configuration du Frontend (Angular) 

#### 3.1 Installer les dépendances

cd frontend/EdoctApp

npm install

## 3.2 Lancer le serveur Angular

ng serve

✅ L'application sera accessible à : http://localhost:4200/

## 🔐 Accès à l'administration

### Interface d'administration Django

- URL : http://127.0.0.1:8000/admin/
- Identifiants : Ceux créés avec createsuperuser

### Fonctionnalités disponibles
- Gestion des utilisateurs (Patients, Docteurs)
- Gestion des rendez-vous
- Gestion des consultations
- Configuration du système

## 📡 Points d'API disponibles

Endpoint Méthode Description
/api/hello/ GET Test de connexion
/api/login/ POST Connexion utilisateur
/api/register/ POST Inscription
/api/patients/ GET/POST Gestion des patients
/api/docteurs/ GET/POST Gestion des docteurs
/api/rendezvous/ GET/POST Gestion des rendez-vous
/api/token/ POST Obtenir un token JWT
/api/token/refresh/ POST Rafraîchir le token

## 🧪 Test de la connexion

1. 1.
   Backend : http://127.0.0.1:8000/api/hello/
2. 2.
   Frontend : http://localhost:4200/
3. 3.
   Admin : http://127.0.0.1:8000/admin/

## 🔧 Commandes utiles

### Django

# Créer des migrations
python manage.py makemigrations

# Appliquer les migrations
python manage.py migrate

# Créer un superutilisateur
python manage.py createsuperuser

# Collecter les fichiers statiques
python manage.py collectstatic

# Lancer le serveur
python manage.py runserver

### Angular

# Installer les dépendances
npm install

# Lancer en mode développement
ng serve

# Build pour la production
ng build --prod

# Générer un composant
ng generate component nom-composant

## 🐛 Dépannage
### Problèmes courants

1. Erreur de connexion à la base de données
   
   - Vérifiez que MAMP est démarré
   - Vérifiez le port MySQL (8889)
   - Vérifiez les identifiants dans settings.py
2. Erreur CORS
   
   - Vérifiez la configuration CORS dans settings.py
   - Redémarrez le serveur Django
3. Erreur de migration

python manage.py migrate --fake-initial

4. Port déjà utilisé

# Django sur un autre port
python manage.py runserver 8001

# Angular sur un autre port
ng serve --port 4201

## 🚀 Déploiement

### Variables d'environnement pour la production
Créez un fichier .env :

DEBUG=False
SECRET_KEY=votre-clé-secrète-très-longue
DATABASE_URL=mysql://user:password@host:port/database
ALLOWED_HOSTS=votre-domaine.com,www.votre-domaine.com

## 📞 Support

Pour toute question ou problème :

- 📧 Email : support@edoctapp.com
- 🐛 Issues : GitHub Issues


EdocTApp - Développé avec ❤️ pour la santé digitale
