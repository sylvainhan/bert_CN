# Projet d'étude pour [Bert](https://github.com/google-research/bert)

## Dépendances
``` bash
python>=3.6
tensorflow>=1.11.0
```
### Pré trained
**[`BERT-Base, Chinese`](https://storage.googleapis.com/bert_models/2018_11_03/chinese_L-12_H-768_A-12.zip)**:
    Chinese Simplified and Traditional, 12-layer, 768-hidden, 12-heads, 110M

### Train et test
- `train.tsv` Collection de Train
- `dev.tsv` Collection de Vérification

----
# Installer l'environnement


## Télécharger et Installer Anaconda
https://www.anaconda.com/distribution/

## Installer tensorflow_cpu
Open a new Anaconda/Command Prompt window

``` bash
conda create -n tensorflow_cpu pip python=3.6

activate tensorflow_cpu

pip install --ignore-installed --upgrade tensorflow==1.11

```

----
## Récuprer ce projet

## Lancer l'étude par commande,

``` bash
D:\Workspace\02_AI_BERT\BERT>SET BASE_DIR=D:\Workspace\02_AI_BERT
D:\Workspace\02_AI_BERT\BERT>SET BERT_Chinese_DIR=%BASE_DIR%\chinese_L-12_H-768_A-12
D:\Workspace\02_AI_BERT\BERT>SET Demo_DIR=%BASE_DIR%\BERT\data
D:\Workspace\02_AI_BERT\BERT>SET Out_DIR=%BASE_DIR%\BERT\out

D:\Workspace\02_AI_BERT\BERT>python run_classifier.py   --task_name=mytask   --do_train=true   --do_eval=true   --data_dir=%Demo_DIR%   --vocab_file=%BERT_Chinese_DIR%\vocab.txt   --bert_config_file=%BERT_Chinese_DIR%\bert_config.json   --init_checkpoint=%BERT_Chinese_DIR%\bert_model.ckpt   --max_seq_length=128   --train_batch_size=32   --learning_rate=2e-5   --num_train_epochs=3.0   --output_dir=%Out_DIR%
```
