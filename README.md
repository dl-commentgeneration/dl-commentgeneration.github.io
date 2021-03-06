### Replication package 

Paper: *Improving Deep Learning based Comment Generation by Highlighting Essential Code*

We provide data and files used in paper and experiments as follow:
Our models are named by **model** +"\_"+ **version**. You can download the **Original_Extractive_Syncretic.zip** from our link and get all of them.

| Model   | Version                                   | Brief Description                                            |
| ------- | ------------------------------------------- | ------------------------------------------------------------ |
| Seq2Seq | Original<br />Extractive<br />Syncretic          | original input only<br />extractive input only (use mask)<br />both of inputs above |
| DeepCom | Original<br />Extractive<br />Syncretic             | original input only<br />extractive input only (use mask)<br />both of inputs above |
| Funcom  | Original<br />Extractive<br />Syncretic | original input only<br />extractive input only (use mask)<br />both of inputs above |

___________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________

How to use the dataset to train a model:

For **DeepCom** & **Seq2Seq**, put the dataset file (i.e. sbt_dataset) in corresponding path of model (i.e. DeepCom_Original/data/), modify **data_dir** and **model_dir** to target dataset in code2nl.yaml. If you have multiple gpus, you can change the **gpu_id** as you like. 

Then input the following command:
**python __main__.py ../config/code2nl.yaml --train -v**

For **Funcom**, put the dataset file in corresponding path of model (Funcom_Original/data/), set **data** and **outdir** to be target dataset. 

Then input the following command:
**python train.py --model-type=ast-attengru --gpu=0**

After training, if you want to evaluate the metrics for your trained model, you need to run **predict.py**  to output the generated comment for test dataset. Then the **bleu.py** will help you compute these values.

______________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________

Get these dataset in [Download Link](https://drive.google.com/file/d/112jjsI-Uzs83URh0IfYPhGzWol1cjnhD/view?usp=sharing)
