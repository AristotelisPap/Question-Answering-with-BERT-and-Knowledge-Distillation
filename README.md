# Question-Answering-with-BERT-and-Knowledge-Distillation

This repository contains the essential code in order to fine-tune BERT on the SQuAD 2.0 dataset. Additionally, the technique of [_Knowledge Distillation_](https://arxiv.org/abs/1503.02531) is applied by fine-tuning [_DistilBERT_](https://arxiv.org/abs/1910.01108) on SQuAD 2.0 dataset using BERT as the teacher model. All of the results have been obtained using 1 Tesla V100 GPU using Google Colab. 


## 1. What is SQuAD?
Stanford Question Answering Dataset (SQuAD) is a reading comprehension dataset, consisting of questions posed by crowdworkers on a set of Wikipedia articles, where the answer to every question is a segment of text, or span, from the corresponding reading passage, or the question might be unanswerable.

<b>SQuAD 2.0</b> combines the 100,000 questions in SQuAD 1.1 with over 50,000 unanswerable questions written adversarially by crowdworkers to look similar to answerable ones. To do well on SQuAD 2.0, systems must not only answer questions when possible, but also determine when no answer is supported by the paragraph and abstain from answering. For more information regarding the SQuAD dataset and the current leaderboard, you can visit the following [_link_](https://rajpurkar.github.io/SQuAD-explorer/).


## 2. How to Run
* To fine-tune BERT on SQuAD 2.0, please run `Fine_Tune_BERT_SQuAD_2_0.ipynb`. This notebook will automatically save the fine-tuned BERT model in `./models/`.
* To evaluate the fine-tuned BERT model, please run `Eval_SQuAD_2_0.ipynb`.
* To use DistilBERT and apply Knowledge Distillation, please check the README in `./Knowledge_Distillation/`.


## 3. Results

| Model                                                      | EM                    | F1 | HasAns_EM | HasAns_F1 | NoAns_EM | NoAns_F1  | No. of parameters (millions) |
| :---:                                                      |    :---:              | :---:| :---:| :---:| :---:| :---:| :---:| 
| BERT-base-uncased                                          |  **72.43**            | **75.74** | 72.54 | 79.15 | 72.33 | 72.33 | 110 |   
| DistilBERT-base-uncased (with distilled fine-tuning)       |  **70.05**            | **73.23** | 70.95 | 77.32 | 69.15 | 69.15 | 66 |   
| DistilBERT-base-uncased (without distilled fine-tuning)    |  **66.93**            | **70.26** | 67.09 | 73.76 | 66.78 | 66.78 | 66 |  


## 4. Code and Paper References

1. A part of the code has been based on the publicly available code of [_HuggingFace Transformers library_](https://github.com/huggingface/transformers).
2. V. Sanh, L. Debut, J. Chaumond, T. Wolf. DistilBERT, a distilled version of BERT: smaller, faster, cheaper and lighter. 5th Workshop on Energy Efficient Machine Learning and Cognitive Computing - NeurIPS 2019. ([_link_](https://arxiv.org/abs/1910.01108))
3. G. Hinton, O. Vinyals, J. Dean. Distilling the Knowledge in a Neural Network. NIPS 2014 Deep Learning Workshop. ([_link_](https://arxiv.org/abs/1503.02531))
4. Smaller, faster, cheaper, lighter: Introducing DistilBERT, a distilled version of BERT. ([_Medium Blog_](https://medium.com/huggingface/distilbert-8cf3380435b5))

