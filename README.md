<h1><center>Analyse de la consommation électrique en Ile de France</center></h1>

<h2><center>SOMMAIRE</center></h2>
- [CONTEXTE DU PROJET](#CONTEXTE DU PROJET)
- [IMPORT DES LIBRAIRIES](#IMPORT DES LIBRAIRIE)
- [FONCTIONS PERSONNELLES](#FONCTIONS PERSONNELLES)
- [LES DONNEES DU PROJET](#LES DONNEES DU PROJET)
- [NETTOYAGE](#NETTOYAGE)
- [Correction de l'effet température : ](#Correction de l'effet température)
    - [1-1 Analyse des variables](#1-1 Analyse des variables)
    - [1-2 Régression linéaire pour corriger l'effet température](#1-2 Régression linéaire pour corriger l'effet température)
- [Transformation pour rendre stationnaire la série : ](#Transformation pour rendre stationnaire la série : )
    - [2-1 Méthode de la soustraction de la moyenne mobile](#2-1 Méthode de la soustraction de la moyenne mobile)
    - [2-2 Méthode différenciation](#2-2 Méthode différenciation)
- [Prédictions : ](#Prédictions : )
    - [3-1 Méthode de Holt Winters](#3-1 Méthode de Holt Winters)
    - [3-2 Méthode SARIMA](#3-2 Méthode SARIMA)
    - [3-3 Focus sur les prédictions à 1 an des 2 modèles](#3-3 Focus sur les prédictions à 1 an des 2 modèles)
- [CONCLUSION](#CONCLUSION)
- [Annexes : Autre méthode pour décomposer une série temporelle](#Annexes : Autre méthode pour décomposer une série temporelle)

<h2>[CONTEXTE DU PROJET]</h2>
<p>Vous êtes employé chez Enercoop, société coopérative qui s'est développée grâce à la libéralisation du marché de l’électricité en France. Elle est spécialisée dans les énergies renouvelables.</p>

<p>La plupart de ces énergies renouvelables est cependant intermittente, il est donc difficile de prévoir les capacités de production d'électricité. De plus, la demande en électricité des utilisateurs varie au cours du temps, et dépend de paramètres comme la météo (température, luminosité, etc.) Tout le challenge est de mettre en adéquation l'offre et la demande !</p>

