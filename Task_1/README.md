## Shared Task Objective 
The primary objective of this task is to identify and classify threats associated with violence, which can potentially lead to further incitement of violent acts.
The task categories are defined as follows:

- Direct Violence: This category encompasses explicit threats directed towards individuals or communities, including actions such as killing, rape, vandalism, deportation, desocialization (threats urging individuals or communities to abandon their religion, culture, or traditions), and resocialization (threats of forceful conversion). The detection of direct violence is crucial due to its potential to yield severe consequences in the future.

- Passive Violence: In this category, instances of violence are represented by the use of derogatory language, abusive remarks, or slang targeting individuals or communities. Additionally, any form of justification for violence is also classified under this category.

- Non-Violence: The contents falling under this category pertain to non-violent subjects, such as discussions about social rights or general conversational topics that do not involve any form of violence.

## Dataset Distribution

| **Class Labels** | **Train** | **Dev** |
|:----------------:|:---------:|:-------:|
|   Non-Violence   |    1389   |   717   |
| Passive Violence |    922    |   417   |
|  Direct Violence |    389    |   196   |

### Sample Dataset

|                                          **Sentence**                                          |     **Label**    |
|:----------------------------------------------------------------------------------------------:|:----------------:|
|                 একজন বাবা কতোটা অসহায় হলে এই কথা বলতে পারে আল্লাহ তুমি বিচার করো                 |   Non-Violence   |
| অসৎ এর বাচ্চারা তোরা কলেজ বিশ্ববিদ্যালয়ে এগুলো করার জন্যেই যাস, আর তোদের জন্য নীরিহ মানুষরা মারা যায়😡 | Passive Violence |
|   এই শালারে জন সম্মুখে আগুনে পুড়িয়ে মারা হউক, যাতে করে আর কোন অমানুষ এ রকম কাজ করতে সাহস না পায় ।   |  Direct Violence |

For this task, we have used Data Augmentation using the paraphrasing technique inorder to increase the size of the dataset.

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
| Data Augmentation + Finetuning | Finetuning [Bert-base-multilingual](https://huggingface.co/bert-base-multilingual-uncased)                             | 69.3%     |
| Data Augmentation + Finetuning | Finetuning [multilingual-e5-base](https://huggingface.co/intfloat/multilingual-e5-base) with prompt text  | **74.60%**   |
| Data Augmentation + Finetuning | Finetuning [multilingual-e5-large](https://huggingface.co/intfloat/multilingual-e5-large) with prompt text | 69.36%   |
| Data Augmentation + Finetuning | Finetuning [twitter-xlm-roberta-sentiment](https://huggingface.co/cardiffnlp/twitter-xlm-roberta-base-sentiment)           | 73.15%   |
| Data Augmentation + Finetuning | Finetuning [mDeBERTa-v3-base-mnli-xnli](https://huggingface.co/MoritzLaurer/mDeBERTa-v3-base-mnli-xnli)              | 71.79%   |

Here we report performance of a few additional experiments which we have performed but their descriptions did not make it to the paper due to page limit. The purpose of reporting the performance here is to help the Bangla Natural Language Processing community to get an idea of how these models stand amongst each other with respect to this classification task.

## Cite us
If you refer to this [work](https://arxiv.org/abs/2310.10781), please cite us with the following bibtex entry:

```
@misc{saha2023banglanlp,
      title={BanglaNLP at BLP-2023 Task 1: Benchmarking different Transformer Models for Violence Inciting Text Detection in Bengali}, 
      author={Saumajit Saha and Albert Nanda},
      year={2023},
      eprint={2310.10781},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}
```
