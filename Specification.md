# Cahier des charges pour le package "equal"

## Workflow

### Objectif général

L'objectif de ce projet est de créer une plateforme d'e-learning permettant aux apprenants d'acquérir des compétences en
utilisant les technologies de YesBabylone. Le développement sera effectué de manière incrémentale avec une revue à
chaque étape pour assurer la qualité du produit final.

### Prérequis

Pour le développement de ce projet, les éléments suivants doivent être pris en compte :

- Utilisation de Material Angular version 2
- Intégration de sb-shared-lib
- Utilisation du squelette (skeleton) nommé "sandbox" pour créer la base de l'application du package

## Introduction

### Objectif spécifique

La plateforme d'e-learning aura pour objectif d'enseigner aux apprenants les technologies spécifiques de YesBabylone.
Parmi les compétences à acquérir, on peut citer :

1. Maîtrise de PHP
2. Utilisation efficace de Workbench

Cette plateforme s'inspire des modèles existants tels que Udemy et OpenClassRoom. Elle interagira étroitement avec
EqualFramework pour la transmission de données vers les vues.

## Consignes à respecter

Dans le cadre du développement de ce projet, certaines consignes devront être strictement respectées :

1. **Interface utilisateur cohérente :** Assurer une expérience utilisateur fluide et cohérente tout au long de la
   plateforme.

## Entity

- Pack
- Module
- Chapter
- Page
- Section
- Leaf

## Layout

Le layout sera composé de :

- Une barre latérale gauche pour le menu de navigation de la plateforme qui permettra de présenter les différents
  cursus.
- Une barre latérale droite pour le suivi du cours (nom du cursus → chapitres → Titre de la leçon). Les leçons
  comporteront :
    - Un chiffre représentant le numéro de la leçon pour la facilité.
    - Le titre.
    - Une icône ou un effet visuel pour savoir si la leçon a été achevée.
- Une top bar avec
    - **À gauche**, l'image représentant la plateforme avec un lien ramenant à la page d'accueil de la plateforme.
    - **Au centre**, un menu représentant les différentes sections du site.
    - **À droite**, un composant représentant la personne authentifiée. Avec :
        - Le nom et prénom de l'apprenant ainsi qu'une image de profil (avatar, image de profil, **ou pas**).
        - Au clic, un menu déroulant avec :
            1. Un lien pour une vue du profil.
            2. Des paramètres s'il y en a.
            3. Un bouton de déconnexion.

## Routes

|    ACTION     | URI                                                                     | VIEW | INFO                                                                                                                                                                                                                                                                                                      |
|:-------------:|:------------------------------------------------------------------------|------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   ``index``   | /learning                                                               |      | Homepage, avec ce que représente la plateforme, pourquoi elle est la, et de comment elle va former des gens.                                                                                                                                                                                              |                                                                                   
|   ``index``   | /learning/pack                                                          |      | Index packs, un annuaire des différentes formations.                                                                                                                                                                                                                                                      |
| ``show/edit`` | /learning/pack/{packId}                                                 |      | Get the specified pack with all information's related to it, <br>like a list of the module(s) inside it with its chapters and quiz, bundle and attachments, time spent to learn, ...<br><br>**Edition mode:** Edit the the information related to the pack and the possibility to add and remove modules. |
| ``show/edit`` | /learning/pack/{packId}/module/{moduleId}                               |      | Get the specified module with all information's related to it, <br> like a list of the chapter(s) inside it.<br><br>**Edition mode:** Edit the module informations and the possibility to add/remove chapters.                                                                                            |
| ``show/edit`` | /learning/pack/{packId}/module/{moduleId}/chapter/{chapterId}           |      | Get the specified chapter with all information's related to it. <br>like a list of the page it contains.<br><br>**Edition mode:** Edit the chapter informations and the possibility to add/remove pages.                                                                                                  |
| ``show/edit`` | /learning/page/{pageId}                                                 |      | Get the specified page with all information's related to it. <br>like a list of the sections or leaf it contains.<br><br>**Edition mode:** Edit the page informations and the possibility to add/remove leaf.                                                                                             |
| ``show/edit`` | /learning/page/{pageId}/section/{sectionId}                             |      | Get the specified section with all information's related to it. <br>like a list of the pages it contains.<br><br>**Edition mode:** Edit the section informations and the possibility to add/remove page.                                                                                                  |
| ``show/edit`` | /learning/page/{pageId}/leaf/{leafId}                                   |      | Get the specified leaf with all information's related to it. <br>like a list of the groups it contains.<br><br>**Edition mode:** Edit the leaf informations and the possibility to add/remove group.                                                                                                      |
| ``show/edit`` | /learning/page/{pageId}/leaf/{leafId}/group/{groupId}                   |      | Get the specified group with all information's related to it. <br>like a list of the widgets it contains.<br><br>**Edition mode:** Edit the group informations and the possibility to add/remove widgets.                                                                                                 |
| ``show/edit`` | /learning/page/{pageId}/leaf/{leafId}/group/{groupId}/widget/{widgetId} |      | Get the specified widget with all information's related to it.<br><br>**Edition mode:** Edit the widget informations.                                                                                                                                                                                     |
|   ``show``    | /learning/profile                                                       |      | The user information's and achievements.                                                                                                                                                                                                                                                                  |

## Views

- Homepage ( what this site does + why + how )
- Index Cursus
- Show cursus (info cursus + module's )
- Show module ( module room )
- ~ profile ( progressions of cursus, number of module achieved, ... )

## Fonctionnalités

Les fonctionnalités de la plateforme incluront, mais ne seront pas limitées à :

- Système d'inscription et de gestion des utilisateurs.
- Gestion de cours et modules d'apprentissage.
- Intégration avec EqualFramework pour la manipulation des données.
- Suivi des progrès des apprenants.
- Système de chat ou de pour la collaboration entre apprenants.
- Avoir la possibilité de lock le panel de droite avec un bouton qui a une icon de punaise.
- Il doit y avoir la possibilité de déplacer un chapitre ou une page ou une section dans un autre chapitre ou une autre
  page ou une autre section.

## Element graphique à prendre en considération

- pour chaque type de 'module', il y aura une icon qui lui sera associé, exemple :
    - pour un module de type 'video', il y aura une icon de video
    - pour un module de type 'quiz', il y aura une icon de quiz
    - pour un module de type 'text', il y aura une icon de feuille de papier
    - ...
