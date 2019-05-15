### Replication package 

Paper: *Improving Deep Learning based Comment Generation through Extractive Code Preprocessing*

We provide data and files used in paper and experiments as follow:

folder: dl_commentageneration_data/

| Dataset for Models | File List                                 | Brief Description                                            |
| :----------------- | :---------------------------------------- | :----------------------------------------------------------- |
| RQ1-TOK-Seq2Seq    | train/valid/test<br />vocab.nl/vocab.code | sequential data for original Seq2Seq<br />vocabulary for tokens and comments |
| RQ1-TOK-OUR        | train/valid/test<br />vocab.nl/vocab.code | sequential data for improved Seq2Seq<br />vocabulary for tokens and comments |
| RQ1-SBT-DeepCom    | train/valid/test<br />vocab.nl/vocab.code | sequential data for original DeepCom<br />vocabulary for SBTs and comments |
| RQ1-SBT-OUR        | train/valid/test<br />vocab.nl/vocab.code | sequential data for improved DeepCom<br />vocabulary for SBTs and comments |
| RQ1-SBT-AO-Funcom  | dataset.pkl<br />smls/dats/coms.tok       | sequential data for original Funcom<br />vocabulary for SBT-AOs, tokens and comments |
| RQ1-SBT-AO-OUR     | dataset.pkl<br />smls/dats/coms.tok       | sequential data for improved Funcom<br />vocabulary for SBT-AOs, tokens and comments |

folder: DeepCom/Seq2Seq/Funcom

| Model   | File List                                   | Brief Description                                            |
| ------- | ------------------------------------------- | ------------------------------------------------------------ |
| Seq2Seq | config<br />data<br />translate          | Configuration files for training<br />dataset path<br />code of model |
| DeepCom | config<br />data<br />translate             | Configuration files for training<br />dataset path<br />code of model |
| Funcom  | data<br />train/predict/bleu.py<br />models | dataset path<br />code of model<br />path to store models    |

How to use the dataset to train a model:

For **DeepCom** & **Seq2Seq**, put the dataset file(i.e. RQ1-SBT-DeepCom) to corresponding path of model(i.e. DeepCom/data/), modify the description **data_dir** and **model_dir** to target dataset in code2nl.yaml. Then input the following command:

**python __main__.py ../config/code2nl.yaml --train -v**

___________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________

For **Funcom**, put the dataset file to corresponding path of model(Funcom/data/), modify the **data** and **outdir** to target dataset. THen input the following command:

**python train.py --model-type=ast-attengru --gpu=0**

______________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________

Get these dataset in [Download Link](ddd)
