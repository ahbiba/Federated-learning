# Federated-learning
Projet2: Federated learning
# Agrégation Sécurisée pour l'Apprentissage Fédéré sur le Jeu de Données MNIST

## Objectif
Ce projet a pour objectif d'implémenter un système d'apprentissage fédéré sécurisé permettant l'entraînement d'un modèle sur le jeu de données MNIST, avec une agrégation sécurisée des mises à jour des clients. L'accent sera mis sur la confidentialité des données et l'efficacité de la communication.

## Sécurité
L'agrégation sécurisée est réalisée en utilisant des techniques de chiffrement pour garantir que les mises à jour des clients restent confidentielles. Cette technique permet de protéger les informations sensibles des utilisateurs tout en permettant au serveur d’agréger les mises à jour des modèles locaux.

## Prérequis

Avant de commencer, on doit vérifier l'installation de :
- Python 3.7+ 
- Bibliothèques Python : `tensorflow`, `numpy`, `flask`, `cryptography`

### 1. Télécharger et installer Python
- Téléchargez Python à partir de [python.org](https://www.python.org) et suivez les instructions d'installation.
- Lors de l'installation, cochez la case "Add Python to PATH" pour faciliter l'accès à Python depuis l'invite de commande.

### 2. Vérifier la version de Python
On doit s'assurer que Python est correctement installé en exécutant la commande suivante dans l'invite de commande :

python --version

### 3. Créer un environnement virtuel appelé 'venv'
python -m venv venv
venv\Scripts\activate

### 4. installer ces dépendances 
pip install tensorflow==2.10.0
pip install flask==2.1.2
pip install numpy==1.23.5
pip install cryptography==3.4.8

### 4. Structure du projet 
federated_learning_secured/
├── client.py          # Entraînement local + envoi des poids cryptés
├── server.py          # Serveur Flask qui reçoit, décrypte et agrège les poids
├── notebook.ipynb     # Notebook Jupyter avec explications pas à pas
├── cryptage.py        # Fonctions de cryptage/décryptage avec Fernet
├── model.py	       # chargement des poids sauvegardés dans le fichier model_weights
└── README.md          # Documentation du projet
