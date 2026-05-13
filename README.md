# LAB 8 : Analyse de posture et exposition d'applications mobiles avec BeVigil et Yaazhini

Analyste : souaid med amine



## Présentation du Projet

Ce laboratoire consiste en une analyse de sécurité "Black Box" et "Grey Box" d'une application Android. Ce document retrace les étapes de préparation, de traçabilité et d'analyse initiale (OSINT).

## Task 0 — Règles, Périmètre et Éthique

Objectif : Définir le cadre légal pour éviter tout risque juridique.

### Création du dossier :

<img width="300" height="124" alt="image" src="https://github.com/user-attachments/assets/21eb35bb-320e-4d2c-99bb-d4054aee1c0d" />

### Création du fichier de périmètre :

<img width="332" height="399" alt="image" src="https://github.com/user-attachments/assets/33c43fa2-4767-4de3-a3f6-17aa9fd86e30" />

### vérification du contenu:

<img width="370" height="281" alt="image" src="https://github.com/user-attachments/assets/97efd3d0-3f08-42da-bf0a-8fd7c391a497" />

## Task 1 — Préparation du Workspace et Traçabilité

Objectif : Créer une structure professionnelle pour l'audit et assurer l'historique des actions.c

### Création de l'arborescence complète

<img width="476" height="145" alt="image" src="https://github.com/user-attachments/assets/77c5a729-7bca-4e76-adde-78d775f0c1cb" />

### Initialisation du fichier d'information

<img width="479" height="151" alt="image" src="https://github.com/user-attachments/assets/ecc0e17a-4a97-4983-ba11-49ac0850edb0" />

### Initialisation du journal des commandes

<img width="479" height="146" alt="image" src="https://github.com/user-attachments/assets/b27b44e9-48cf-4ff3-aa94-5df6024f5440" />

### Vérification de la structure

<img width="357" height="299" alt="image" src="https://github.com/user-attachments/assets/3a7e3e45-6024-4769-90df-cfcac0af4c3e" />


## Task 2 — Préparer l'Artefact Autorisé

Objectif : Compiler l'application et garantir son intégrité via un Hash SHA-256.

### Compilation de l'APK

<img width="458" height="61" alt="image" src="https://github.com/user-attachments/assets/198a6da1-8185-4e47-ad05-03a76d2c530b" />

### Déplacement vers le dossier scope

<img width="475" height="143" alt="image" src="https://github.com/user-attachments/assets/256cca52-8759-4811-845e-c71c807ca595" />

<img width="440" height="62" alt="image" src="https://github.com/user-attachments/assets/4ba13e05-5b58-4274-afd9-2370ed7222ad" />

### Mise à jour de la documentation avec le hash

<img width="478" height="317" alt="image" src="https://github.com/user-attachments/assets/748e7223-37a3-40a0-9321-78b9c2f82fdc" />

## Task 3 — Démarrage et Prise en main BeVigil

Objectif : Analyser l'exposition externe (OSINT) de l'application.
  
<img width="1750" height="892" alt="image" src="https://github.com/user-attachments/assets/a392aed8-5d93-4093-867c-f5f17b4e14e9" />

- Recherche de l'application cible sur BeVigil (CloudSEK) pour obtenir des informations sur les apps mobiles indexées.
  
  
<img width="1800" height="807" alt="image" src="https://github.com/user-attachments/assets/559af175-f946-4419-a60a-d838e501ad0e" />


- Upload du fichier app-debug.apk sur la plateforme BeVigil via l'option "Scan .apk file" pour analyse de vulnérabilités.

  
<img width="945" height="485" alt="image" src="https://github.com/user-attachments/assets/80e68003-a924-4a76-83de-0b61d8bd8027" />


  - Confirmation que le fichier APK a été soumis avec succès, le rapport de risque sera disponible prochainement.
    
<img width="945" height="526" alt="image" src="https://github.com/user-attachments/assets/0133131e-6048-488b-bf8c-671b101dec63" />

- Analyse du certificat de l'APK via BeVigil Certificate Viewer révèle que l'app est signée avec un certificat de débogage

  
<img width="945" height="707" alt="image" src="https://github.com/user-attachments/assets/312d659c-3eee-416d-bff7-85a74695fb5c" />


- Installation et importation réussie du certificat racine YaazhiniProxy
  
  
<img width="945" height="400" alt="image" src="https://github.com/user-attachments/assets/6872625c-1fce-4576-bdbb-085f7628a151" />


## Task 4 — Démarrage et prise en main Yaazhini

- Interface de l'outil Yaazhini (VegaBird Technologies) permettant de scanner un fichier APK ou d'intercepter les requêtes API via le proxy configuré sur l'IP 172.29.32.1 port 8088.

  
<img width="945" height="543" alt="image" src="https://github.com/user-attachments/assets/9d101aa2-fb08-4ae8-978f-3af1528c19e0" />


- L'outil Yaazhini API Scanner affiche les 4 étapes d'utilisation : configurer le proxy Android, installer le certificat, naviguer dans l'app, puis générer le rapport de vulnérabilités.

  
<img width="945" height="413" alt="image" src="https://github.com/user-attachments/assets/4cf5d64a-2116-4059-aa40-a84816cee644" />


<img width="711" height="1297" alt="image" src="https://github.com/user-attachments/assets/9844ea3f-5da2-4357-a840-93b7aa40ccd5" />


