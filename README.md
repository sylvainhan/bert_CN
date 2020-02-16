Install Anaconda
https://www.anaconda.com/distribution/

Télécharger Anaconda et L'installer

----

Open a new Anaconda/Command Prompt window
taper commande

conda create -n tensorflow_cpu pip python=3.6

activate tensorflow_cpu

pip install --ignore-installed --upgrade tensorflow==1.11


Récuprer le projet dans la disque dur,

Et lancer l'étude par commande,

D:\Workspace\02_AI_BERT\BERT>SET BASE_DIR=D:\Workspace\02_AI_BERT
D:\Workspace\02_AI_BERT\BERT>SET BERT_Chinese_DIR=%BASE_DIR%\chinese_L-12_H-768_A-12
D:\Workspace\02_AI_BERT\BERT>SET Demo_DIR=%BASE_DIR%\BERT\data
D:\Workspace\02_AI_BERT\BERT>SET Out_DIR=%BASE_DIR%\BERT\out

D:\Workspace\02_AI_BERT\BERT>python run_classifier.py   --task_name=mytask   --do_train=true   --do_eval=true   --data_dir=%Demo_DIR%   --vocab_file=%BERT_Chinese_DIR%\vocab.txt   --bert_config_file=%BERT_Chinese_DIR%\bert_config.json   --init_checkpoint=%BERT_Chinese_DIR%\bert_model.ckpt   --max_seq_length=128   --train_batch_size=32   --learning_rate=2e-5   --num_train_epochs=3.0   --output_dir=%Out_DIR%

