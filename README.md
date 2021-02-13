# Question-Answering-with-BERT-and-Knowledge-Distillation

This repository contains the essential code in order to fine-tune BERT on the SQuAD 2.0 dataset. Additionally, the technique of [_Knowledge Distillation_](https://arxiv.org/abs/1503.02531) is applied by fine-tuning [_DistilBERT_](https://arxiv.org/abs/1910.01108) on SQuAD 2.0 dataset using BERT as the teacher model. All of the results have been obtained using 1 Tesla V100 GPU using Google Colab. 


## 1. What is SQuAD?
Stanford Question Answering Dataset (SQuAD) is a reading comprehension dataset, consisting of questions posed by crowdworkers on a set of Wikipedia articles, where the answer to every question is a segment of text, or span, from the corresponding reading passage, or the question might be unanswerable.

<b>SQuAD2.0</b> combines the 100,000 questions in SQuAD1.1 with over 50,000 unanswerable questions written adversarially by crowdworkers to look similar to answerable ones. To do well on SQuAD2.0, systems must not only answer questions when possible, but also determine when no answer is supported by the paragraph and abstain from answering.
