# Cahier des charges pour le package "equal"

## Workflow

### Objectif général
L'objectif de ce projet est de créer une plateforme d'e-learning permettant aux apprenants d'acquérir des compétences en utilisant les technologies de YesBabylone. Le développement sera effectué de manière incrémentale avec une revue à chaque étape pour assurer la qualité du produit final.

### Prérequis

Pour le développement de ce projet, les éléments suivants doivent être pris en compte :

- Utilisation de Material Angular version 2
- Intégration de sb-shared-lib
- Utilisation du squelette (skeleton) nommé "sandbox" pour créer la base de l'application du package

## Introduction

### Objectif spécifique
La plateforme d'e-learning aura pour objectif d'enseigner aux apprenants les technologies spécifiques de YesBabylone. Parmi les compétences à acquérir, on peut citer :

1. Maîtrise de PHP
2. Utilisation efficace de Workbench

Cette plateforme s'inspire des modèles existants tels que Udemy et OpenClassRoom. Elle interagira étroitement avec EqualFramework pour la transmission de données vers les vues.

## Consignes à respecter

Dans le cadre du développement de ce projet, certaines consignes devront être strictement respectées :

1. **Interface utilisateur cohérente :** Assurer une expérience utilisateur fluide et cohérente tout au long de la plateforme.

## Layout

Le layout sera composé de :

- Une barre latérale gauche pour le menu de navigation de la plateforme qui permettra de présenter les différents cursus.
- Une barre latérale droite pour le suivi du cours (nom du cursus --> chapitres --> Titre de la leçon). Les leçons comporteront :
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

## Entity
- Cursus
- Lesson
- Comment
- Student

## Views

- Homepage ( what this site does + why + how )
- Index Cursus
- Show cursus (info cursus + lessons's )
- Show lessons ( lessons room )
- ~ profile ( progressions of cursus, number of lessons achieved, ... )

## Fonctionnalités

Les fonctionnalités de la plateforme incluront, mais ne seront pas limitées à :

- Système d'inscription et de gestion des utilisateurs
- Gestion de cours et modules d'apprentissage
- Intégration avec EqualFramework pour la manipulation des données
- Suivi des progrès des apprenants
- Système de chat ou de pour la collaboration entre apprenants


