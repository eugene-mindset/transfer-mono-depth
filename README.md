# transfer-mono-depth
Improving Transferability in Monocular Depth Estimation.



Filesystem structure:

```models/    transfer-mono-depth/    monodepth2/    datasets/    logs/...```

Models contains our fully trained serialized networks. Model directories should be named as so:

```['Modification']|-Finetuned|/```

Modification represents if the network is changed (e.g. 'Control', 'Frozen-Last-Layer').
Finetuned indicates whether this model was finetuned or not. Simply append '-Finetuned' if thats the case.

Each experiment will have a branch in monodepth2 corresponding to the changes we've made to the model. Make sure to give it the same name as the name of the model.


## Phase I: Setup

- [ ] Create train-valid-test split for our indoor dataset.
- [ ] Preprocess data to work with network if neccessary.
- [ ] Train control model like described in the paper.
- [ ] Decide on a fixed fine-tuning process
- [ ] Setup dataset directory to have the proper files in their locations.
- [ ] Create a dataset script to handle creating the necessary splits.

## Phase II: Experimentation

- [ ] Evaluate performance of control model on indoor test set.
- [ ] Evaluate performance of Control + Finetune on indoor test set.
- [ ] ...