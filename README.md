# BERT
Reproducing BERT results from BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding

### Fine Tuning
Instructions to run the code below:<br>
Create 'SQuAD' folder where project path is set and add train, dev and evalute script in it.<br>
Create 'BERT_BASE' folder and add model, config and vocab files to it.<br>
Create 'Output' folder and set as Output directory<br>
The below code is used to fine tune a model<br>
<br>
How to use checkpoints?<br>
If full training cannot be completed add the saved latest checkpoint to the output folder. The run_squad checks for pre trained checkpoints and uses them to train.
<br><br>
How to use checkpoints to predict directly?<br>
The below results are derived by using a checkpoint which was previously trained by me. Change the do_train param to False and make do_predict true to get predictions using a saved trained checkpoint added to the output folder.

