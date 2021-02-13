## 1. Download Data

Download the data from the following link: [SQuAD 2.0](https://github.com/chrischute/squad/tree/master/data) and place it to the `./data/` folder.


## 2. How to Run
* After fine-tuning the BERT model (used as a teacher in Knowledge Distillation) on SQuAD 2.0, place the file containing the model weights in `./models_with_distillation/fine_tuned_bert/`.

* To fine-tune DistilBERT on SQuAD 2.0 while using Knowledge Distillation from BERT during fine-tuning, please run the notebook `With_Distillation_Fine_Tune_DistilBERT_SQuAD_2_0.ipynb`.

* To fine-tune DistilBERT on SQuAD 2.0 without Knowledge Distillation, please run the notebook `Without_Distillation_Fine_Tune_DistilBERT_SQuAD_2_0.ipynb`.

* To evaluate the fine-tuned DistilBERT models, please run the notebook `Eval_SQuAD_2_0.ipynb`.
