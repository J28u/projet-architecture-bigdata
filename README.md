# OC/DS Projet 8 : Déployez un modèle dans le cloud
Formation OpenClassrooms - Parcours data scientist - Projet Professionnalisant (Juillet - Août 2023)

## Secteur : 
Agroalimentaire

## Technologies utilisées : 
  * Jupyter Notebook
  * Python
    - pyspark
      
  * AWS 
    - EC2
    - S3
    - EMR

## Mots-clés : 
BigData, Cluster de Machines

## Le contexte : 
Le client, une startup de l’AgriTech, souhaite se faire connaître grâce à une application mobile permettant d’obtenir des informations sur un fruit à partir d’une simple photo.

Le volume de données à traiter va augmenter très rapidement une fois l’application mise en production, ce qui va créer des besoins différents en matière d’infrastructures de stockage et de calculs. 

## La mission : 
Construire et tester une première version de l’architecture BigData nécessaire pour passer à l’échelle nos traitements sur de gros volumes de données, en s’inspirant d’un notebook laissé par un alternant qui vient de quitter l’entreprise.

## Livrables :
* notebook.ipynb : notebook contenant les scripts en Pyspark exécutables
* presentation.pdf : support de présentation pour la soutenance.

## Méthodologie suivie : 
Pour tester cette architecture BigData, on ne va pas entraîner de modèle de classification mais simplement nettoyer et pré-traiter le jeu de données d’entrées puis enregistrer le résultat, le tout sur le cloud. 

 1. Tester le script pyspark en local :
   *  nettoyage des données images
   *  extraction des features (transfer learning avec modèle MobileNetV2)
   *  réduction de dimensions (ACP)
   *  stockage des données transformées

2. Choisir les services AWS adaptés à notre problématique :
  *  création compte AWS et création d’alertes dépassement de budget
  *  création d’un bucket dans S3
  *  configuration du service EMR

3. Exécuter le script sur un cluster de machines géré par EMR :
  * lancement d’un cluster EMR
  * connexion au serveur maître via un tunnel SSH
  * exécution du notebook manuellement depuis JupyterHub hébergé sur le cluster

## Compétences acquises :  
* Utiliser les outils du cloud pour manipuler des données dans un environnement BigData
* Identifier les outils du cloud permettant de mettre en place un environnement Big Data
* Paralléliser des opérations de calcul avec Pyspark

## Data source : 
https://www.kaggle.com/moltean/fruits
