# NietzscheNext

Trains neural networks on the collected works of Friedrich Nietzsche to create an app for text completion (autocomplete). 

Data was obtained from [Projekt Gutenberg](https://www.gutenberg.org/ebooks/author/779). The dataset comprises 1.8m characters or tokens, split into train and test sets with 1,180,649 and 590,549 tokens, respectively. 

Neural nets are trained to predict the next character based on a given context length. First, a character-level Recurrent Neural Network (RNN) model was trained, with a context length of 80 characters. This model yields a test-set prediction accuracy of 17.3% for predicting the next word from context. This accuracy gets boosted to 36.4% when the model receives the first character of the word in question as additional information: 

![see Figure 1](figures/rnn_prediction_accuracy.png)

Second, I trained a transformer model (Karpathy 2022), also based on a context length of 80 characters. The prediction accuracy is at 19.7% and 44.7% after adding additional information about the first character of the word: 

![Figure 2](figures/prediction_accuracy_transformer.png)

----
References:
Karpathy, Andrej. 2022. NanoGPT. https://github.com/karpathy/nanoGPT/tree/master


