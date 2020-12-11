# projet_python_2A

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
- model_selection : feature selection et discrimination entre plusieurs modèles (random forest, decision tree, KNN, logistic regression, MLP classifier)
