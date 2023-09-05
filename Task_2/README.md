## Task 2 experiments and results during development phase:

| Approaches                      | Experimental Details                                           | Micro F1 |
|---------------------------------|----------------------------------------------------------------|----------|
| Finetuning                      | Finetuning [Bangla Bert](https://huggingface.co/sagorsarker/bangla-bert-base)                                         | 65.41%   |
| Finetuning                      | Finetuning [Indic Bert](https://huggingface.co/ai4bharat/indic-bert)                                          | 60.54%   |
| Finetuning                      | Finetuning [M-clip Bert](https://huggingface.co/M-CLIP/M-BERT-Base-ViT-B)                                         | 64.1%    |
| Finetuning                      | Finetuning [Bert-base-multilingual](https://huggingface.co/bert-base-multilingual-uncased)                              | 63.9%    |
| Finetuning                      | Finetuning [twitter-xlm-roberta-sentiment](https://huggingface.co/cardiffnlp/twitter-xlm-roberta-base-sentiment)                       | **68.07%**   |
| Finetuning                      | Finetuning [flan-t5-base](https://huggingface.co/google/flan-t5-base)                                        | 47.0%     |
| Prompt Tuning                   | [XLM-Roberta-Base](https://huggingface.co/xlm-roberta-base)                                                    | 49.62%   |
| Prompt Tuning                   | [XLM-Roberta-Large](https://huggingface.co/xlm-roberta-large)                                              | 63.46%   |
| Pretraining and then Finetuning | Pretrained [Bangla Bert](https://huggingface.co/sagorsarker/bangla-bert-base) and then Finetuned it                   | 61.94%   |
