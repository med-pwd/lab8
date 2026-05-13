LAB 8 : Analyse de posture et exposition d'applications mobiles avec BeVigil et Yaazhini
Analyste : Hafssa Azarg Date : 31 Mars 2026 Cible : sg.vantagepoint.lab8

Présentation du Projet
Ce laboratoire consiste en une analyse de sécurité "Black Box" et "Grey Box" d'une application Android. Ce document retrace les étapes de préparation, de traçabilité et d'analyse initiale (OSINT).

Task 0 — Règles, Périmètre et Éthique
Objectif : Définir le cadre légal pour éviter tout risque juridique.

Création du dossier :
image
Création du fichier de périmètre :
image
vérification du contenu:
image
Task 1 — Préparation du Workspace et Traçabilité
Objectif : Créer une structure professionnelle pour l'audit et assurer l'historique des actions.c

Création de l'arborescence complète
image
Initialisation du fichier d'information
image
Initialisation du journal des commandes
image
Vérification de la structure
image
Task 2 — Préparer l'Artefact Autorisé
Objectif : Compiler l'application et garantir son intégrité via un Hash SHA-256.

Compilation de l'APK
image
Déplacement vers le dossier scope
image image
Mise à jour de la documentation avec le hash
image
Task 3 — Démarrage et Prise en main BeVigil
Objectif : Analyser l'exposition externe (OSINT) de l'application.

image
Recherche de l'application cible sur BeVigil (CloudSEK) pour obtenir des informations sur les apps mobiles indexées.
image
Upload du fichier app-debug.apk sur la plateforme BeVigil via l'option "Scan .apk file" pour analyse de vulnérabilités.
image
Confirmation que le fichier APK a été soumis avec succès, le rapport de risque sera disponible prochainement.
image
Analyse du certificat de l'APK via BeVigil Certificate Viewer révèle que l'app est signée avec un certificat de débogage
image
Installation et importation réussie du certificat racine YaazhiniProxy
image
Task 4 — Démarrage et prise en main Yaazhini
Interface de l'outil Yaazhini (VegaBird Technologies) permettant de scanner un fichier APK ou d'intercepter les requêtes API via le proxy configuré sur l'IP 172.29.32.1 port 8088.
image
L'outil Yaazhini API Scanner affiche les 4 étapes d'utilisation : configurer le proxy Android, installer le certificat, naviguer dans l'app, puis générer le rapport de vulnérabilités.
image image
About
No description, website, or topics provided.
Resources
 Readme
 Activity
Stars
 0 stars
Watchers
 0 watching
Forks
 0 forks
Report repository
Releases
No releases published
Packages
No packages published
Contributors
1
@hafssa799
hafssa799
Footer
# lab8
