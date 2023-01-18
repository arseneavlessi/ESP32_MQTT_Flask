Projet de visualisation de température

Ce projet utilise Flask, Paho-MQTT et HTML pour afficher les données de température reçues via un serveur MQTT. Les données sont mises à jour en temps réel sur la page web sans avoir besoin d'actualiser manuellement.
Prérequis

    Python 3.x
    Flask
    Paho-MQTT

Installation

    Clonez ce dépôt sur votre ordinateur
    Installez les dépendances en utilisant la commande pip install -r requirements.txt
    Modifiez les informations de connexion au serveur MQTT dans le fichier app.py
    Lancez le serveur en utilisant la commande python app.py
    Ouvrez votre navigateur web et rendez-vous sur http://localhost:5000 pour voir les données de température mises à jour en temps réel

Fonctionnement

Le script app.py utilise Flask pour créer un serveur web. Il utilise également Paho-MQTT pour se connecter au serveur MQTT, s'abonner au topic de température et recevoir les données de température. Lorsque des données sont reçues, la fonction de callback on_message est appelée pour mettre à jour les données de température et appeler la fonction de mise à jour de la page HTML. La page HTML est générée à l'aide du template Jinja2 qui utilise la variable de température pour afficher les données sur la page web.