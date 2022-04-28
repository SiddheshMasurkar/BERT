# BERT
Reproducing results from BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding<br>
Paper: https://arxiv.org/pdf/1810.04805.pdf<br>
Official code: https://github.com/google-research/bert<br>

Note: The results are reproduced using Colab. The python notebook AI Mini Project.ipynb is to be used.<br>

### Dataset used: SQuAD 1.1
Training data: https://rajpurkar.github.io/SQuAD-explorer/dataset/train-v1.1.json<br>
Test data: https://rajpurkar.github.io/SQuAD-explorer/dataset/dev-v1.1.json<br>
Evaluate script: https://github.com/allenai/bi-att-flow/blob/master/squad/evaluate-v1.1.py <br>

### Git repo pull
The section 'Loading git files in Colab' in AI Mini Project.ipynb mounts the drive, creates a project folder, clones the official repo and sets the project path<br>

### Issue resolving
Run the 'Resolving issues' section in AI Mini Project.ipynb before fine tuning the BERT model. We are using the older version of numpy and tensorflow.

### Fine Tuning
run_squad.py is used to fine tune the model with hyperparamter settings<br>

**Instructions to follow before running the code in AI Mini Project notebook:**<br>
(Keep the names same to directly run the code)<br>
Create 'SQuAD' folder inside the project folder and add train, dev data and evalute script in it.<br>
Create 'BERT_BASE' folder and add the pre trained model, config and vocab files to it. Link can be found in the official github repo above.<br>
Create 'Output' folder and set as Output directory<br><br>
The run_squad cell in the notebook is used to fine tune the BERT pre trained model<br>
The hyperparameters currently used are set to a bare minimum and are enough to reproduce the results in the paper for BERT Base on SQuAD 1.1.<br>

### Checkpoints
How to use checkpoints?<br>
The checkpoints are added to the specified output folder. The run_squad checks for pre trained checkpoints and uses them to train. If full training cannot be completed in one go, then only keep the latest checkpoint in Output folder and re run the run_squad cell in the notebook. Note: Each checkpoint >= 1.2 GB.
<br><br>
How to use checkpoints to directly predict?<br>
The results in the notebook are produced by using a checkpoint which was previously trained by me. Add the trained checkpoint to the Output folder. Change the 'do_train' param to False and make 'do_predict' true to get predictions using a saved trained checkpoint without any training.

### Results
BERT Base fine tuned on SQuAD 1.1 gave an F1 score of 88.5(Reported in paper)
We are able to achieve 88 in our attempt to reproduce the results.<br>
Note: The results in the notebook are produced using a checkpoint. I believe full training can replicate the score of 88.5 using the notebook provided.
