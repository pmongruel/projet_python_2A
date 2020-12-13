# Comment prédire au mieux l'hypertension artérielle ?

## Présentation du sujet

Nos données sont issues d'une enquête de santé (NHANES, *national health and nutrition examination survey*), réalisée tous les deux ans aux Etats-Unis sur un échantillon représentant l'ensemble de la population. Nous disposons des résultats de l'enquête de 2017-2018 (soit la plus récente disponible), qui sont regroupés en plusieurs bases de données : 

- Demographics data : informations sur les caractéristiques sociales des individus, leurs caractéristiques familiales et leurs revenus ; 
- Questionnaire data : informations collectées par questionnaire auprès des individus, portant sur de nombreux sujets (pathologies, comportements alimentaires, activité physique, troubles psychiques, consommation de drogues...) 
- Laboratory data : informations obtenues par prélèvements (taux de cholestérol / de plomb / de fer / etc. dans le sang) et tests médicaux (hépatites, diabète, asthme, anémie, hypertension, etc.)

A partir de toutes ces données, nous cherchons à prédire au mieux l'hypertension artérielle, c'est-à-dire à la fois trouver les variables déterminantes de cette pathologie, tout en déterminant le meilleur modèle de prédiction de l'hypertension. 

## Fichiers

- webscrapping : webscrapping pour collecter les données médicales sur le site de la NHANES (national health and nutrition examination survey)
- data_xpt : dossier contenant les bases de données brutes (en format .sas) issues du webscrapping
- features_names.csv : fichier contenant le nom et le type de chaque variable, ce dont on se servira pour la création du dataset
- dataset_creation : création d'un unique csv (data.csv) à partir des bases de données initiales
- data.csv : fusion des bases de données (réalisée dans le fichier ci-dessus)
- preprocessing_and_statistics : nettoyage de la base data.csv et production de statistiques descriptives sur les variables d'intérêt. Le preprocessing nous permet d'obtenir les deux datasets que l'on utilisera par la suite : 
  - data_unscaled.csv : données non scalées
  - data_scaled.csv : données scalées
- clustering : clustering avec k-means sur les données scalées afin d'affiner la prédiction
- model_selection : feature selection et discrimination entre plusieurs modèles (random forest, decision tree, logistic regression)
