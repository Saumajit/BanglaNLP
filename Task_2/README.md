## Shared Task Description
The objective is to detect the sentiment associated within a given text. This is a multi-class classification task that involves determining whether the sentiment expressed in the text is Positive, Negative, Neutral.

## Dataset Distribution
|              | **Train** | **Dev** |
|:------------:|:---------:|:-------:|
| **Positive** |   12364   |   1388  |
| **Negative** |   15767   |   1753  |
|  **Neutral** |    7135   |   793   |
### Sample Dataset
|                            **Sentence**                           | **Label** |
|:-----------------------------------------------------------------:|:---------:|
|             টানা দুই হারের পর জয়ের স্বাদ পেল ইউভেন্তুস \|             |  Positive |
|                  করোনায় আক্রান্ত হয়ে আরো ১ জনের মৃত্যু                 |  Negative |
| চিন্তা করেন যারা বক্তব্যে দিচ্ছে তাদের কন্ঠ ও ছবি দেখাতে সাহস ও পায় না |  Neutral  |

## Task 2 experiments and results during development phase:

| Approaches                      | Experimental Details                                           | Micro F1 |
|---------------------------------|----------------------------------------------------------------|----------|
| Traditional ML using TF-IDF | Logistic Regression | 55% |
| Traditional ML using TF-IDF | SGD Classifier      | 47%  |
| Traditional ML using TF-IDF | Multinomial Naive Bayes         | 56% |
| Traditional ML using TF-IDF | Majority Voting     | 55% |
| Traditional ML using TF-IDF | Stacking            | 54% |
| Finetuning                      | Finetuning [Bangla Bert](https://huggingface.co/sagorsarker/bangla-bert-base)                                         | 65.41%   |
| Finetuning                      | Finetuning [Indic Bert](https://huggingface.co/ai4bharat/indic-bert)                                          | 60.54%   |
| Finetuning                      | Finetuning [M-clip Bert](https://huggingface.co/M-CLIP/M-BERT-Base-ViT-B)                                         | 64.1%    |
| Finetuning                      | Finetuning [Bert-base-multilingual](https://huggingface.co/bert-base-multilingual-uncased)                              | 63.9%    |
| Finetuning                      | Finetuning [twitter-xlm-roberta-sentiment](https://huggingface.co/cardiffnlp/twitter-xlm-roberta-base-sentiment)                       | **68.07%**   |
| Finetuning                      | Finetuning [flan-t5-base](https://huggingface.co/google/flan-t5-base)                                        | 47.0%     |
| Prompt Tuning                   | [XLM-Roberta-Base](https://huggingface.co/xlm-roberta-base)                                                    | 49.62%   |
| Prompt Tuning                   | [XLM-Roberta-Large](https://huggingface.co/xlm-roberta-large)                                              | 63.46%   |
| Pretraining and then Finetuning | Pretrained [Bangla Bert](https://huggingface.co/sagorsarker/bangla-bert-base) and then Finetuned it                   | 61.94%   |

Here we report performance of a few additional experiments which we have performed and that are not mentioned in the paper due to page limit. We include them here  particularly because we want to highlight the Bangla Natural Language Processing community how they perform in similar classification tasks in a low-resource language like Bengali.

## Cite us 
If you refer to our [work](https://arxiv.org/abs/2310.09238v2), please cite us with the following bibtex entry:
```
@misc{saha2023banglanlp,
      title={BanglaNLP at BLP-2023 Task 2: Benchmarking different Transformer Models for Sentiment Analysis of Bangla Social Media Posts}, 
      author={Saumajit Saha and Albert Nanda},
      year={2023},
      eprint={2310.09238},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}
```
