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
| Finetuning                     | Finetuning [Bangla Bert](https://huggingface.co/sagorsarker/bangla-bert-base)                                          | 64.5     |
| Finetuning                     | Finetuning [Bert-base-multilingual](https://huggingface.co/bert-base-multilingual-uncased)                               | 67.2     |
| Finetuning                     | Finetuning [multilingual-e5-base](https://huggingface.co/intfloat/multilingual-e5-base)                                 | 60.92    |
| Finetuning                     | Finetuning [multilingual-e5-base](https://huggingface.co/intfloat/multilingual-e5-base) with prompt text                | 71.57    |
| Finetuning                     | Finetuning [multilingual-e5-large](https://huggingface.co/intfloat/multilingual-e5-large) with prompt text               | 60.48    |
| Data Augmentation + Finetuning | Finetuning [Bert-base-multilingual](https://huggingface.co/bert-base-multilingual-uncased) after round 1                             | 69.3     |
| Data Augmentation + Finetuning | Finetuning [Bert-base-multilingual](https://huggingface.co/bert-base-multilingual-uncased) after round 2                             | 65.2     |
| Data Augmentation + Finetuning | Finetuning [Bangla Bert](https://huggingface.co/sagorsarker/bangla-bert-base) after round 2                                    | 69.4     |
| Data Augmentation + Finetuning | Finetuning [multilingual-e5-base](https://huggingface.co/intfloat/multilingual-e5-base) with prompt text after round 1  | **74.60%**   |
| Data Augmentation + Finetuning | Finetuning [multilingual-e5-base](https://huggingface.co/intfloat/multilingual-e5-base) with prompt text after round 2  | 73.38%   |
| Data Augmentation + Finetuning | Finetuning [multilingual-e5-large](https://huggingface.co/intfloat/multilingual-e5-large) with prompt text after round 1 | 69.36%   |
| Data Augmentation + Finetuning | Finetuning [twitter-xlm-roberta-sentiment](https://huggingface.co/cardiffnlp/twitter-xlm-roberta-base-sentiment) after round1           | 73.15%   |
| Data Augmentation + Finetuning | Finetuning [mDeBERTa-v3-base-mnli-xnli](https://huggingface.co/MoritzLaurer/mDeBERTa-v3-base-mnli-xnli) after round 1             | 71.79%   |


## Task 2 experiments and results during development phase:

| Approaches                      | Experimental Details                                           | Micro F1 |
|---------------------------------|----------------------------------------------------------------|----------|
| Finetuning                      | Finetuning [Bangla Bert](https://huggingface.co/sagorsarker/bangla-bert-base)                                         | 65.41%   |
| Finetuning                      | Finetuning [Indic Bert](https://huggingface.co/ai4bharat/indic-bert)                                          | 60.54%   |
| Finetuning                      | Finetuning [M-clip Bert](https://huggingface.co/M-CLIP/M-BERT-Base-ViT-B)                                         | 64.1%    |
| Finetuning                      | Finetuning [Bert-base-multilingual](https://huggingface.co/bert-base-multilingual-uncased)                              | 63.9%    |
| Finetuning                      | Finetuning [twitter-xlm-roberta-sentiment](https://huggingface.co/cardiffnlp/twitter-xlm-roberta-base-sentiment)                       | **68.07%**   |
| Finetuning                      | Finetuning [flan-t5-base](https://huggingface.co/google/flan-t5-base)                                        | 47.0%     |
| Ensembling                      | Ensemble of bangla, indic, m-clip bert using majority voting   | 33.42%   |
| Ensembling                      | Ensemble of bangla, indic, m-clip bert using average of logits | 31.32%   |
| Ensembling                      | Ensemble of bangla, m-clip bert                                | 36.8%    |
| Prompt Tuning                   | [XLM-Roberta-Base](https://huggingface.co/xlm-roberta-base)                                                    | 49.62%   |
| Prompt Tuning                   | [XLM-Roberta-Large](https://huggingface.co/xlm-roberta-large)                                              | 63.46%   |
| Pretraining and then Finetuning | Pretrained [Bangla Bert](https://huggingface.co/sagorsarker/bangla-bert-base) and then Finetuned it                   | 61.94%   |
