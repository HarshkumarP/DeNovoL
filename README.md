# DeNovoL

A De novo molecular generation method using linguistic models(LSTM)


## Requirements

Jupyter or Google collab with python cell.
python => 3.7
TensorFlow: 2.92

NOTE: Following notebooks for building autoencoder and generating novel molecules are run on google collab with premium GPU.

## Running code

### Step 1: Store data 
Store the following files in a folder in google drive 
a. Create a folder in google drive named "next_gen_data" 
b. Copy the following files from the folder next_gen_data in git to the google drive

**Mandatory files:**
1. **char_to_int.json**: mapping of smiles character to int
2. **int_to_char.json**: mapping of smiles index to character
3. **moses.smi**: dataset

**Optional files** which are generated using python notebook:
1. **LSTM_model.h5**: trained autoencoder with 65 epochs (Created by:)
2. **gen_model.h5**: generative model (Created by:)
3. **test.npy**: test set (Created by:)

 
### Step 2: Build autoencoder

### Step 3: Generate novel molecules 
