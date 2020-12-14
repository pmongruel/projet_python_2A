# Comment prédire au mieux l'hypertension artérielle ?

## Présentation du sujet

Nos données sont issues d'une enquête de santé (NHANES, *national health and nutrition examination survey*), réalisée tous les deux ans aux Etats-Unis sur un échantillon représentant l'ensemble de la population. Nous disposons des résultats de l'enquête de 2017-2018 (soit la plus récente disponible), qui sont regroupés en plusieurs bases de données : 

- Demographics data : informations sur les caractéristiques sociales des individus, leurs caractéristiques familiales et leurs revenus ; 
- Questionnaire data : informations collectées par questionnaire auprès des individus, portant sur de nombreux sujets (pathologies, comportements alimentaires, activité physique, troubles psychiques, consommation de drogues...) 
- Laboratory data : informations obtenues par prélèvements (taux de cholestérol / de plomb / de fer / etc. dans le sang) et tests médicaux (hépatites, diabète, asthme, anémie, hypertension, etc.)

A partir de toutes ces données, nous cherchons à prédire au mieux le risque d'hypertension artérielle pour un individu, c'est-à-dire à la fois trouver les variables déterminantes de cette pathologie, tout en déterminant le meilleur modèle de prédiction de l'hypertension. 

## Fichiers

- webscraping_and_data_set_creation : webscrapping pour collecter les données médicales sur le site de la NHANES (national health and nutrition examination survey), puis création de la base de données (data.csv)
- data.csv : fusion des bases de données (réalisée dans le fichier ci-dessus)
- data_xpt : dossier contenant les bases de données brutes (en format .sas) issues du webscraping, dont on se sert pour la création du dataset
- features_names.csv : fichier contenant le nom et le type de chaque variable, ce dont on se sert pour la création du dataset
- modélisation : notebook du projet, contenant une partie preprocessing, une partie de statistiques descriptives, puis une partie feature selection et model selection
 
