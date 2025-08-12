TPLinker + NYT
 1. TPlinker-joint-extraction-master.zip
 Ce fichier contient la version originale du code TPLinker. Il s'agit de la base du projet, avant toute
 modification ou adaptation.
 2. Train copy(1).ipynb
 Notebook modifié pour rendre l'entraînement autonome et générique. Il : - Intègre tous les
 paramètres de configuration directement dans le notebook - Supprime la dépendance à 
config.py
 et wandb - Utilise 
logging standard et crée automatiquement les répertoires nécessaires - Contient
 un pipeline complet de prétraitement compatible avec tout dataset JSON de type NYT
 Voir le fichier 
Rapport d'Analyse des Modifications.pdf pour les détails techniques.
 3. Données - Fichiers JSON
 Fichier
 Description
 nyt_dataset - 
Copie.json <br>
 Copie(1).json
 nyt_dataset - 
Dataset brut original (non prétraité), issu
 directement de la source NYT.
 Dataset prétraité à l'aide du notebook adapté. Il
 nyt_dataset(1).json
 contient 
relation_list , 
entity_list et est
 prêt à l'entraînement.
 nyt_dataset_rel2id.json
 Fichier de correspondance entre les relations
 (predicates) et leurs ID numériques. Généré
 automatiquement.
 nyt_dataset_train.json
 Ensemble d'entraînement, extrait après
 prétraitement et division aléatoire.
 nyt_dataset_valid.json
 Ensemble de validation, extrait après division
 aléatoire.
 1
4. Rapport d'Analyse des Modifications.pdf
 Ce rapport documente toutes les modifications techniques apportées entre la version originale du
 notebook et la version adaptée. Points couverts : - Suppression des dépendances à 
config.py et
 wandb - Ajout d'un pipeline de prétraitement tokenisé - Gestion automatique de 
rel2id.json 
Robustesse face aux variations de format JSON
