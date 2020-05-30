# test

### Replication package


Paper: _Improving Deep Learning based Comment Generation by Highlighting Essential Code_


We provide data and files used in paper and experiments as follow:
Our models are named by ** model + "_" +version**



| Model | Version | Description |
| --- | --- | --- |
| Seq2Seq | Original
Extractive
 | original input only
extractive input only(use mask)
both of inputs above |
| DeepCom | Original
Extractive
 | original input only
extractive input only(use mask)
both of inputs above |
| Funcom | Original
Extractive
 | original input only
extractive input only(use mask)
both of inputs above |


---

#### How to use the dataset to train a model:


For **DeepCom** & **Seq2Seq**, put the dataset file(i.e. RQ1-SBT-DeepCom) to corresponding path of model(i.e. DeepCom_Original/data/), modify the description **data_dir** and **model_dir** to target dataset in code2nl.yaml.
if you have multiple gpus, you can change the gpu_id as you like.
Then input the following command:
**python __main__.py ../config/code2nl.yaml --train -v**
**
For **Funcom**, put the dataset file to corresponding path of model(Funcom/data/), modify the **data** and **outdir** to target dataset. Then input the following command:
**python train.py  --gpu=0**
After training, if you want to evaluate the metrics for your trained model, you need to run **predict.py**  to output the generated comment for test dataset. Then the **bleu.py**  will help you compute these values.

---

Get these dataset in [Download Link](https://drive.google.com/drive/folders/1JQILCDm8Wv6SqWvIH-PrzUyLIU8ykO_Y?usp=sharing)
