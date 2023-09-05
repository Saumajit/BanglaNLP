For Task 1, we have used Data Augmentation using the paraphrasing technique inorder to increase the size of the dataset.

## Task 1 experiments and results during development phase: 

| Approaches                     | Experimental Details                                            | Macro F1 |
|--------------------------------|-----------------------------------------------------------------|----------|
| Traditional ML using TF-IDF | Logistic Regression | 52.97% |
| Traditional ML using TF-IDF | SGD Classifier      | 44.8%  |
| Traditional ML using TF-IDF | Naive Bayes         | 52.13% |
| Traditional ML using TF-IDF | Majority Voting     | 51.67% |
| Traditional ML using TF-IDF | Stacking            | 50.99% |
| Finetuning                     | Finetuning [Bangla Bert](https://huggingface.co/sagorsarker/bangla-bert-base)                                          | 64.5%     |
| Finetuning                     | Finetuning [Bert-base-multilingual](https://huggingface.co/bert-base-multilingual-uncased)                               | 67.2%     |
| Finetuning                     | Finetuning [multilingual-e5-base](https://huggingface.co/intfloat/multilingual-e5-base) with prompt text                | 71.57%    |
| Finetuning                     | Finetuning [multilingual-e5-large](https://huggingface.co/intfloat/multilingual-e5-large) with prompt text               | 60.48%    |
| Data Augmentation + Finetuning | Finetuning [Bert-base-multilingual](https://huggingface.co/bert-base-multilingual-uncased) after round 1                             | 69.3%     |
| Data Augmentation + Finetuning | Finetuning [multilingual-e5-base](https://huggingface.co/intfloat/multilingual-e5-base) with prompt text after round 1  | **74.60%**   |
| Data Augmentation + Finetuning | Finetuning [multilingual-e5-large](https://huggingface.co/intfloat/multilingual-e5-large) with prompt text after round 1 | 69.36%   |
| Data Augmentation + Finetuning | Finetuning [twitter-xlm-roberta-sentiment](https://huggingface.co/cardiffnlp/twitter-xlm-roberta-base-sentiment) after round1           | 73.15%   |
| Data Augmentation + Finetuning | Finetuning [mDeBERTa-v3-base-mnli-xnli](https://huggingface.co/MoritzLaurer/mDeBERTa-v3-base-mnli-xnli) after round 1             | 71.79%   |
