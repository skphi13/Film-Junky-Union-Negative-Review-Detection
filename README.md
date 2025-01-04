# Film-Junky-Union-Negative-Review-Detection
The Film Junky Union, a new edgy community for classic movie enthusiasts, is developing a system for filtering and categorizing movie reviews. The goal is to train a model to automatically detect negative reviews.


## Data Description

The data is stored in the `imdb_reviews.tsv` file. Download the dataset.

The data was provided by Andrew L. Maas, Raymond E. Daly, Peter T. Pham, Dan Huang, Andrew Y. Ng, and Christopher Potts. (2011). Learning Word Vectors for Sentiment Analysis. The 49th Annual Meeting of the Association for Computational Linguistics (ACL 2011).

Here's the description of the selected fields:

`review`: the review text
`pos`: the target, '0' for negative and '1' for positive
`ds_part`: 'train'/'test' for the train/test part of dataset, correspondingly

## Conclusions
After normalizing and vectorized 3 models with a dummy model alongside for a baseline, we have successfully created 3 models and evaluated their performances.

 Model 2: Used the Natural Language Toolkit with TF-IDF vectorization fit to a Logistic Regression model showed to be an effective model.

  - Accuracy : 0.94 0.88
  - F1 : 0.94 0.88
  - APS : 0.98 0.95
  - ROC AUC : 0.98 0.95

Model 3: Used spaCY library for NLP in addition to TF-IDF vectorization, fit to Logistic Regression model also performed well.

  - Accuracy : 0.93 0.88
  - F1 : 0.93 0.88
  - APS : 0.98 0.95
  - ROC AUC : 0.98 0.95

Model 4: Used the spaCY library for NLP in addition to TF-IDF vectorization as well, fit to a gradient boosted decision tree model.

  - Accuracy: 0.92 0.86
  - F1 Score: 0.92 0.86
  - APS: 0.98 0.93
  - ROC AUC: 0.98 0.94


- Model 2 and Model 3 performed well, achieving high scores across all metrics. Model 2 slightly outperformed Model 3 in terms of F1 and Accuracy, making it a reliable and efficient choice.

- Model 4 showed competitive performance with an F1 score of 0.92 and solid APS (0.98) and ROC AUC (0.94) scores. While it no longer significantly outperforms the Logistic Regression models, it remains a strong alternative, especially for scenarios where gradient boosting's robustness might be beneficial.

**Recommendation:**

- Model 2 remains a standout for its balance between performance and simplicity. However, Model 4 provides comparable performance and could be favored in cases where a tree-based model's interpretability or robustness is advantageous.
