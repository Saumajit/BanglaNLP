For Task 1, we have used Data Augmentation using the paraphrasing technique inorder to increase the size of the dataset.

For both the tasks, we have tried a lot of experiments. However each of these 2 above experiments for individual tasks stood out among all of our submissions during the development phase.


## Task 1 experiments and results during development phase: 

| Approaches                     | Experimental Details                                            | Macro F1 |
|--------------------------------|-----------------------------------------------------------------|----------|
| Traditional ML using TF-IDF | Logistic Regression | 52.97 |
| Traditional ML using TF-IDF | SGD Classifier      | 44.8  |
| Traditional ML using TF-IDF | Naive Bayes         | 52.13 |
| Traditional ML using TF-IDF | Majority Voting     | 51.67 |
| Traditional ML using TF-IDF | Stacking            | 50.99 |
| Finetuning                     | Finetuning Bangla Bert                                          | 64.5     |
| Finetuning                     | Finetuning Bert-base-multilingual                               | 67.2     |
| Finetuning                     | Finetuning multilingual-e5-base                                 | 60.92    |
| Finetuning                     | Finetuning multilingual-e5-base with prompt text                | 71.57    |
| Finetuning                     | Finetuning multilingual-e5-large with prompt text               | 60.48    |
| Data Augmentation + Finetuning | FT Multi-lingual bert after round 1                             | 69.3     |
| Data Augmentation + Finetuning | FT Multi-lingual bert after round 2                             | 65.2     |
| Data Augmentation + Finetuning | FT Bangla bert after round 2                                    | 69.4     |
| Data Augmentation + Finetuning | Finetuning multilingual-e5-base with prompt text after round 1  | **74.60%**   |
| Data Augmentation + Finetuning | Finetuning multilingual-e5-base with prompt text after round 2  | 73.38%   |
| Data Augmentation + Finetuning | Finetuning multilingual-e5-large with prompt text after round 1 | 69.36%   |
| Data Augmentation + Finetuning | Finetuning twitter-xlm-roberta-sentiment after round1           | 73.15%   |
| Data Augmentation + Finetuning | Finetuning mDeBERTa-v3-base-mnli-xnli after round 1             | 71.79%   |


## Task 2 experiments and results during development phase:

| Approaches                      | Experimental Details                                           | Micro F1 |
|---------------------------------|----------------------------------------------------------------|----------|
| Finetuning                      | Finetuning Bangla Bert                                         | 0.6541   |
| Finetuning                      | Finetuning Indic Bert                                          | 0.6054   |
| Finetuning                      | Finetuning M-clip Bert                                         | 0.641    |
| Finetuning                      | Finetuning Bert-base-multilingual                              | 0.639    |
| Finetuning                      | Finetuning twitter-xlm-roberta-sentiment                       | **0.6807**   |
| Finetuning                      | Finetuning flan-t5-base                                        | 0.47     |
| Ensembling                      | Ensemble of bangla, indic, m-clip bert using majority voting   | 0.3342   |
| Ensembling                      | Ensemble of bangla, indic, m-clip bert using average of logits | 0.3132   |
| Ensembling                      | Ensemble of bangla, m-clip bert                                | 0.368    |
| Prompt Tuning                   | XLM-Roberta                                                    | 0.4962   |
| Prompt Tuning                   | XLM-Roberta-Large                                              | 0.6346   |
| Pretraining and then Finetuning | Pretrained Bangla Bert and then Finetuned it                   | 0.6194   |
