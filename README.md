

## About The Project

Le but de ce projet est de réaliser une classification de documents, il consiste à classifier des mails en spams/hams en utilisant plusieurs techniques de Machine Learning, les étapes sont :

- Récolte des données
- Nettoyage et préparation des données
  - Supprimer la ponctuation
  - tokenizer les données
  - Elimination des stop words (mots sans valeurs sémantiquement)
  - réduction de la taille du document en réduissant le nombre de type de mot présent dans le doc (stemming ou lemmatization)
- vectorisation (transformer le text en chiffres)
  - vectorisation contextuelle N grams
  - vectorisation tf-idf
  - Feature Engineering : enrichir les données avec de nouvelles variables ou transformer les variables excitantes
- Construire des jeux de données pour l'entrainement et le test
  - Cross-Validation et méthode K-fold
  - matrice de confusion
- Modèles
  - SVM
  - SVM_CrossValidation
- Évaluation des modèles
  - Métriques de performance : precision, recall et accuracy.
- sélection du meilleur modèle

#### Keywords

Machin Learning, NLP, tokenizer, stemming, lemmatization, vectorisation, N_grams, tf-idf, Feature Engineering, Cross-Validation, k-fold, SVM,

#### Built With

* Python
* Pandas
* re
* nltk


## Packages & Library

```python
import pandas as pd
import re
import string
import nltk
from nltk.corpus import stopwords

```

## Dataset

Le Dataset [SMSSpamCollection.txt](Data/SMSSpamCollection.txt) peut être téléchargé [ici](http://dcomp.sor.ufscar.br/talmeida/smspamcollection/)   
Ce jeu de données contient deux informations principales : le contenu d'un mail, et le label qui définit si le mail est spam/ham




## Result
Métriques de performance utilisé : precision, recall et accuracy.    
- Résultats pour le [model SVM](SVM_model.ipynb)
  - precision = 0.966, recall = 0.929, accuracy = 0.986
- Résultat pour le [model SVM_CrossValidation](SVM_model.ipynb)
  - accuracy pour chaque batch = [0.97774587 0.9856425  0.9798995  0.98420675]
  - accuracy totale = 0.9818736539842067
- Résultat pour le [model SVM_TF-IDF](SVM_model.ipynb)
  - precision = 0.993, recall = 0.905, accuracy = 0.987


