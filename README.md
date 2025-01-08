# NietzscheNext

Trains neural networks on the collected works of Friedrich Nietzsche to create an app for text completion (autocomplete). 

Data was obtained from Project Gutenberg. Predictions at character level, N tokens. Train-test split, N tokens. 

First, a character-level Recurrent Neural Network (RNN) model was trained, with a context length of 80 characters. This model yields a test-set prediction accuracy of 17.3% for predicting the next word from context. This accuracy gets boosted to 36.4% when the model receives the first character of the word in question as additional information. 

Second, I trained a transformer model (Karpathy XXXX). 
44.7% after 
