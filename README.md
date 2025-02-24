# Pokémon Databricks Project

Ce projet analyse et classe les Pokémon par puissance totale en utilisant l'API PokéAPI, **Delta Lake**, et **Azure Databricks**. Une pipeline ETL automatisé a également été mis en place pour extraire, transformer et charger les données quotidiennement.

## Étapes du projet

1. **Extraction des données** via l'API PokéAPI.
2. **Stockage des données brutes** dans **Delta Lake**.
3. **Nettoyage et transformation des données** via un notebook Python sur Databricks.
4. **Analyse et classement** des Pokémon par puissance totale (attaque, défense, etc.).
5. **Visualisation** des résultats avec des graphiques et des clusters basés sur les caractéristiques des Pokémon.
6. **Automatisation** de tout le processus avec un **Job Databricks** pour garantir la mise à jour quotidienne des données.

## Automatisation du processus ETL avec Databricks Job

Pour automatiser ce projet, j'ai mis en place un **job Databricks** qui exécute le pipeline ETL quotidiennement. Ce job permet de récupérer les données de l'API PokéAPI, les transformer et les sauvegarder dans **Delta Lake**.

### Détails du Job

- **Source de données** : API [PokeAPI](https://pokeapi.co/)
- **Transformation des données** : Les données sont nettoyées, formatées, et analysées dans un [notebook Databricks](Pokemon_Ranking.ipynb).
- **Stockage** : Sauvegarde dans **Delta Lake**, permettant une gestion efficace des données.
- **Automatisation** : Le **Job Databricks** est planifié, garantissant que les données soient toujours à jour.
- **Cluster** : Utilisation du cluster `Pokemon Cluster` sur Databricks pour exécuter les tâches de calcul et de traitement des données.
