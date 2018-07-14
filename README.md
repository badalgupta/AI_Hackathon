# AI_Hackathon
Sentiment Analysis

Approach:-

Preprocess data
Remove null column values by any textual data as I did by using "fillna" in my code.
Select number of features, max length and embedding to use
max_features = 100000, maxlen = 150, embedding used = Glove
Use Tokenizer to tokenize text, convert them to sequences and pad the comments so that each one becomes = maxlen of 150 words.
Used Glove embedding to create embeddings of words which are in vocabulary.
Create model
Take Input of shape = maxlen
Create Embedding layer of max_features
Apply SpatialDropout
Use Bidirectional LSTM with 128 layers.
Apply Conv1D and reduced the number of layers to 64.
Apply GlobalAveragePooling1D and GlobalMaxPooling1D and concatenate them.
Apply Dropout
Use Dense Layer with activation as sigmoid
Compile the model with 'binary_crossentropy'.
Fit the model and run for 10 epochs(after that it converges).
Perform k fold with number of folds = 4.
