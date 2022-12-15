# DeNovoL

A De novo molecular generation method using linguistic models(LSTM)


## Requirements

Jupyter or Google colab with python cell.
python > 3.7
TensorFlow: 2.92

NOTE: Following notebooks for building autoencoder and generating novel molecules was run on google collab with premium GPU.

## Running code

### Step 1: Store data 
______
Store the following files in a folder in google drive 
a. Create a folder in google drive named "next_gen_data"   
b. Copy the following files from the folder next_gen_data in git repo to the google drive   

**Files:**
1. **char_to_int.json**: mapping of smiles character to int
2. **int_to_char.json**: mapping of smiles index to character
3. **moses.smi**: dataset
Files which are generated using python notebook:
1. **LSTM_model.h5**: trained autoencoder with 65 epochs required in DeNovo_mol_gen.ipynb (Created by: LSTM_Base.ipynb)
2. **gen_model.h5**: generative model (Created by: DeNovo_mol_gen.ipynb)
3. **test.npy**: test set required in DeNovo_mol_gen.ipynb (Created by: LSTM_Base.ipynb)

 
### Step 2: Build autoencoder
____________
Run LSTM_Base.ipynb

Notebook performs following main tasks:   
1. Prepare dataset for training.
2. Define autoencoder
3. Train autoencoder

Required input: char_to_int.json, int_to_char.json and moses.smi   
Output: LSTM_model.h5(trained autoencoder), test.npy(test set after train/test split)

### Step 3: Generate novel molecules 
____________
Run DeNovo_mol_gen.ipynb

Notebook performs following main tasks:
1. Create standalone encoder, decoder (decomposition of autoencoder)
2. Experiment mol gen with different softmax temprature
3. Generate molecules from the latent space

Required input: LSTM_model.h5(autoencoder build from step 2), test.npy(test set split from step 2), char_to_int.json, int_to_char.json   
Output:  gen_model.h5(genrative model), generated_smiles.csv (sampled denovo molecule)

______________
#### Few sampled molecules from DeNovoL
![image](https://user-images.githubusercontent.com/82495070/207969079-81812325-d471-4bbb-a963-ed5b919d2df1.png)

