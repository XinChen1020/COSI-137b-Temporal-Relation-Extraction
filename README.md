# COSI-137b-Temporal-Relation-Extraction

Preprocess pipeline is adopted from https://github.com/PlusLabNLP/JointEventTempRel

To run the codes:
1. Add glove.6B.50d.txt to the folder _other_
2. python3 code/featurize_data.py -data_type tbd -data_dir data/ -other_dir other/
3. python3 code/context_aggregator.py -data_dir data/ -data_type tbd
4. python3 code/joint_model.py -relation_weight 1.0 -entity_weight 1.0 -data_type "tbd" -batch 4 -model "multitask/pipeline" -eval_gold False -pipe_epoch 1000 -epoch 10 -other_dir other/      (-biaffine or -multihead command can be added if want to train an attention module)


