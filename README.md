---
title: "COURS SUR RSTUDIO"
author: "Dr_Bill"
date: "`r Sys.Date()`"
output: html_document
editor_options: 
  markdown: 
    wrap: 75
---

# COURS SUR RSTUDIO

# Prise-en-main-R

Je vous dédit cet espace afin de vous permettre de vous appliquer à
faire votre toute première prise main de cet outil d'analyse si
important et crucial pour la suite de votre carrière professionnelle. Il
contient tout ce dont vous aurez besoin. Veuillez suivre les étapes !

- Plan du Travail
  - Chapitre 1: PRESENTATION DE R ET RSTUDIO
  - Chapitre 2: RAPPELS ou REGLES SUR LES PRINCIPES D'USAGE
  - Chapitre 3: LES PACKAGES INDISPENSABLES
  - Chapitre 4: LES VARIABLES
  - Chapitre 5: GRAPHIQUES
  - Note

## Introduction

R est un langage open source (accès libre) conçu pour les statistiques,
l’analyse de données et la modélisation. Il est largement utilisé en
recherche, en data science, en finance, en santé publique et dans tout
domaine nécessitant une analyse rigoureuse. Sa force vient de sa
communauté active et de milliers de packages spécialisés.

#Chapitre 1: PRESENTATION DE R ET RSTUDIO

Définition de R R est un langage de programmation et un logiciel libre
et gratuit, conçu pour l'analyse statistique et la visualisation de
données.

### À quoi sert-il en santé ?

Nettoyer des données d'enquête, calculer des indicateurs, réaliser des
tests statistiques, des graphiques et des cartes.

### Comment l'utiliser ?

On lui donne des instructions écrites (du code) : il calcule et renvoie
le résultat.

Définition de RSTUDIO: RStudio est un environnement de développement
intégré (IDE) pour R : une seule fenêtre qui rassemble tout ce qu'il
faut pour écrire et exécuter du code.

- Ce qu'il apporte :

  - Éditeur de scripts,
  - Console,
  - Liste des objets,
  - Graphiques,
  - Aide et packages,
  - Une autocomplétion et coloration du code.

NB: Il faut télécharger et installer R avant de télécharger RSTUDIO, car
RSTUDIO ne fonctionne pas sans R.

Lien pour télécharger R : <https://cran.r-project.org/> Une fois R
installé, lancez le fichier d'installation de RStudio et suivez les
instructions à l'écran. Après l'installation, ouvrez RStudio pour
vérifier que tout fonctionne correctement et que la console R s'affiche.

Lien pour télécharger RSTUDIO : <https://posit.co/downloads>

Après avoir télécharger les logiciels R et RSTUDIO, nous allons en
aventure dans l'analyse des données disponibles

# Chapitre 2 : RAPPELS OU REGLES SUR LES PRINCIPES D'USAGE

## Créer un projet RStudio

File \> New Project Commenter son code

## Importation des données

data \<- read.csv("patients.csv")

Sauvegarder régulièrement avec cette commande au clavier : Ctrl + S

## Explorer les données

head(data)
str(data)
summary(data)

### NETTOYAGE
Gérer les valeurs manquantes
colSums(is.na(data))

# Chapitre 3 : LES PACKAGES INDISPENSABLES

Installation d'un package 

  install.packages("ggplot2")
  install.packages("gtsummary")
  install.packages("dplyr")
  install.packages("readr")
  install.packages("tidyr")
  install.packages("tidyverse")
  install.packages("epiR")

NB: Respecter la même syntaxe que ceux citer ci-haut


- Chargement d'un package
  library(ggplot2)
  library(readr)
NB: Respecter la même syntaxe que ceux citer précédemment
  
Manipulation des données
  library(dplyr)
  library(tidyr)
  library(readr)
  
# Visualisation
  library(ggplot2)

# Statistiques médicales
library(gtsummary)
library(epiR)

 Bioinformatique
library(DESeq2)
library(edgeR)
library(limma) 

# Chapitre 4 : LES VARIABLES
Création d'une variable 
age <- 25 

## Variables numériques 
poids <- 68.5

## Variables caractères 
nom <- "Bill" 

## Variables logiques 
malade <- TRUE
non_malade <- FALSE

## Vérifier le type d'une variable
class(age) 

# Chapitre 5 : GRAPHIQUES
Ici, il s'agit de faire une représentation en image sous forme de graphique afin de faciliter la compréhension ou de faciliter la présentation des résultats de nos données.
Nous disposons de plusieurs types de graphiques qui suivent :

### Histogramme
hist(age)

### Diagramme en barres
barplot(table(sexe))

## Boxplot
boxplot(age \~ profession, data = smp1)

### Graphique avec ggplot2
ggplot(smp1, aes(x = prof, y = age)) + geom_boxplot(fill = "lightblue")

### Nuage de points 
ggplot(smp1, aes(x = age, y = n.enfant)) + geom_point()

Nous avons citer parallèlement les graphiques et la syntaxe qui permet de générer cela.

# Note 
  - Bonnes pratiques Toujours travailler dans un projet.
- Bien commenter son script.
- Utiliser des noms explicites.
- Vérifier les données avant l'analyse.
- Sauvegarder régulièrement.

  - Règle d'or
Ne jamais interpréter un résultat statistique sans avoir réalisé une exploration graphique préalable des données.


Conclusion R et RStudio constituent des outils essentiels pour l'analyse de données en santé, en pharmacie, en finance, en logistique, en biostatistique et en bio-informatique. Une bonne maîtrise des principes de base facilite l'apprentissage des analyses plus avancées.
