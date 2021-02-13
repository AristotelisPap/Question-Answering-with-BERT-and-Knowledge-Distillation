# Question-Answering-with-BERT-and-Knowledge-Distillation

This repository contains the essential code in order to fine-tune BERT on the SQuAD 2.0 dataset. Additionally, the technique of [_Knowledge Distillation_](https://arxiv.org/abs/1503.02531) is applied by fine-tuning [_DistilBERT_](https://arxiv.org/abs/1910.01108) on SQuAD 2.0 dataset using BERT as the teacher model. All of the results have been obtained using 1 Tesla V100 GPU using Google Colab. 


## 1. What is SQuAD?
Stanford Question Answering Dataset (SQuAD) is a reading comprehension dataset, consisting of questions posed by crowdworkers on a set of Wikipedia articles, where the answer to every question is a segment of text, or span, from the corresponding reading passage, or the question might be unanswerable.

<b>SQuAD 2.0</b> combines the 100,000 questions in SQuAD 1.1 with over 50,000 unanswerable questions written adversarially by crowdworkers to look similar to answerable ones. To do well on SQuAD 2.0, systems must not only answer questions when possible, but also determine when no answer is supported by the paragraph and abstain from answering. For more information regarding the SQuAD dataset and the current leaderboard, you can visit the following [_link_](https://rajpurkar.github.io/SQuAD-explorer/).


## 2. Results

| Model                                                      | EM                    | F1 | MNLI | MRPC | QNLI | QQP  | RTE  | SST-2| STS-B| WNLI              |
| :---:                                                      |    :---:              | :---:| :---:| :---:| :---:| :---:| :---:| :---:| :---:| :---:             |
| BERT-base-uncased                                          |  **72.43**             |  | 75.74 | 88.6 | 91.8 | 89.6 | 69.3 | 92.7 | 89.0 | 53.5              |
| DistilBERT-base-uncased (with distilled fine-tuning)       |  **77.0**             | 51.3 | 82.1 | 87.5 | 89.2 | 88.5 | 59.9 | 91.3 | 86.9 | 56.3              |
| DistilBERT-base-uncased (without distilled fine-tuning)    |  **78.2**             | 58.2 | 83.9 | 87.8 | 91.0 | 89.2 | 66.1 | 91.7 | 89.2 | 46.5              |


## 3. Code and Paper References

1. A part of the code has been based on the publicly available code of [_HuggingFace Transformers library_](https://github.com/huggingface/transformers).
2. V. Sanh, L. Debut, J. Chaumond, T. Wolf. DistilBERT, a distilled version of BERT: smaller, faster, cheaper and lighter. 5th Workshop on Energy Efficient Machine Learning and Cognitive Computing - NeurIPS 2019. ([_link_](https://arxiv.org/abs/1910.01108))
3. G. Hinton, O. Vinyals, J. Dean. Distilling the Knowledge in a Neural Network. NIPS 2014 Deep Learning Workshop. ([_link_](https://arxiv.org/abs/1503.02531))
4. Smaller, faster, cheaper, lighter: Introducing DistilBERT, a distilled version of BERT. ([_Medium Blog_](https://arxiv.org/abs/1503.02531))

