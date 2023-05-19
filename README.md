# Zero-Shot BioNER
Zero-Shot and Few-Shot methods for NER in biomedical domain
## Dataset Conversion

Each of the datasets has been converted using a specific script to a format where the named entity (NE) has been transformed to 1, while everything else has been labeled as 0.

The conversion process can be implemented using the following steps:

1. Load the original dataset.
2. Define a conversion function that maps NE to 1 and other entities to 0.
3. Apply the conversion function to each dataset separately.
4. Merge the converted datasets into a single dataset.

### Converted datasets

##### Chemical NER 
- CHEMDNER 
- CDR-Chemical 

##### Disease NER 
- NCBI-Disease 
- CDR-Disease 

##### Gene/Protein NER 
- JNLPBA 

##### Drugs 
- n2c2/i2b2 

### Merged dataset is in table below
<img width="599" alt="objedinjeni_dataset" src="https://github.com/br-ai-ns-institute/Zero-ShotNER/assets/8451505/de4a9f46-f5f2-4574-aacc-0df3f3325990">

## Preprocessing Task Steps
To preprocess the dataseт, follow the steps outlined below:

1. **Splitting into Train, Validation, and Test Sets:** Dataset is divided into three subsets: a training set, a validation set, and a test set. The training set will be used to train the model, the validation set will be used for tuning hyperparameters and evaluating the model during training, and the test set will be used for final evaluation.

2. **Creating Transformer Encodings:** Generate transformer encodings for the dataset. These encodings should include two fields: "class" and "text". The "class" field will contain the labels for each instance, and the "text" field will contain the corresponding input text. These encodings are necessary for feeding the data into a transformer-based model.

3. **Aligning Labels with BERT Tokens:** Perform label alignment with BERT tokens. This step involves mapping the labels to align with the corresponding tokens generated by the BERT tokenizer. Ensure that the labels are correctly aligned with the appropriate tokens to maintain the integrity of the dataset.

4. **Transforming into Torch Dataset:** Convert the preprocessed dataset into a Torch dataset, which will serve as the input for your model. The Torch dataset provides compatibility with PyTorch. This conversion allows for seamless integration of the dataset with your model and facilitates efficient training and evaluation.

By following these preprocessing steps, you will have a properly prepared dataset ready for training your model. Ensure that each step is executed accurately and thoroughly to ensure the reliability and effectiveness of your results.
