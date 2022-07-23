# ITMO-Advanced-NLP

## Lab #1
### Part I
The task is to clear the text data of the crawled web-pages from different sites. 

It is necessary to ensure that the distribution of the 100 most frequent words includes only meaningful words in english language (not particles, conjunctions, prepositions, numbers, tags, symbols).

Determine the order of operations below and carry out the appropriate cleaning.

1. Remove non-english words
2. Remove html-tags (try to do it with regular expression, or play with beautifulsoap library)
3. Apply lemmatization / stemming
4. Remove stop-words
5. Additional processing - At your own initiative, if this helps to obtain a better distribution

### Part II
1. Detect duplicated text (duplicates do not imply a complete word-to-word match, but texts that may contain a paraphrase, rearrangement of words, sentences)
2. Make a plot dependency of duplicates on shingle size (with fixed minhash length) 
3. Make a plot dependency of duplicates on minhash length (with fixed shingle size) 

### Part III. Topic Modelling.
The provided data contain chunked stories by Edgar Allan Poe (EAP), Mary Shelley (MWS), and HP Lovecraft (HPL).

The dataset can be downloaded here: `https://drive.google.com/file/d/14tAjAzHr6UmFVFV7ABTyNHBh-dWHAaLH/view?usp=sharing`
1. Preprocess dataset with the functions from the Part 1
2. Implement the following three quality fuctions: `coherence` (or `tf-idf coherence`), `normalized PMI`, `based on the distributed word representation`(you can use pretrained w2v vectors or some other model). You are free to use any libraries (for instance gensim) and components.
3. Read and preprocess the dataset, divide it into train and test parts `sklearn.model_selection.train_test_split`. Test part will be used in classification part. For simplicity we do not perform cross-validation here, but you should remember about it.
4. Implement topic modeling with **NMF** (you can use `sklearn.decomposition.NMF`) and print out resulting topics. Try to change hyperparameters to better fit the dataset.
5. Implement topic modeling with **LDA** (you can use gensim implementation) and print out resulting topics. Try to change hyperparameters to better fit the dataset.


## Lab #2
For this task a well-known `quora duplicate detection dataset` will be used.
1. Do a little exploratory analysis. Find how many duplicates and non-duplicates are there in the train part and any other actions of 
your interest to better understand the data.
2. Build the **siamese network**
3. Measure the quality. To calculate loss use `Triplet Loss`. 
4. Train the model

## Lab #3
1. Implement `Self-Attention` mechanism
2. Analyse pre-trained BERT model for text processing


## Lab #4
Understand the fine-tuning procedure and get acquainted with `Huggingface Datasets library`.
1. Load tokenizer and model
2. Look at the predictions of the model as-is before any fine-tuning
3. Define optimizer, sheduler (optional)
4. Fine-tune the model (write the training loop), plot the loss changes and measure results in terms of weighted F1 score
5. Get the masked word prediction (sample sentences above) on the fine-tuned model, why the results as they are and what should be done in order to change that (write down your answer)







