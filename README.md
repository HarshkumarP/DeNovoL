# DeNovoL
A De novo molecular generation method using linguistic models(LSTM)

Environment: Google colab/ python


To run python notebooks perform following steps:

1. Store following files in a folder in google drive 
    a. Create a folder in google drive named "next_gen_data"
    b. Copy following files from the folder next_gen_data in git to google drive
    
    Mandatory files:
    1. char_to_int.json: mapping of smiles character to int
    2. int_to_char.json: mapping of smiles index to character 
    3. moses.smi: dataset
        
    Optional files which are created using python notebook:
    1. LSTM_model.h5: trained autoencoder with 65 epochs (Created by:)
    2. gen_model.h5: genrative model (Created by:)
    3. test.npy: testset (Created by:)
    
    recommended to copy all file.
    
2. Run note book


3. Run note book
