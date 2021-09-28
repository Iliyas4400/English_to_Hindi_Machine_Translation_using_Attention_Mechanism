# English_to_Hindi_Machine_Translation_using_Attention_Mechanism
Encoder Decoder architecture with Attention Mechanism to translate sentences from English to Hindi
### Data set
Text data is downloaded from(https://www.kaggle.com/aiswaryaramachandran/english-to-hindi-neural-machine-translation?select=Hindi_English_Truncated_Corpus.csv)

### Libraries used ###
Tensor Flow, Keras, NLTK, Regex, Sklearn, Matplotlib, Numpy and Pandas.

### Text preprocessing
Both the texts are processed using regex to remove unwanted words. sentences with suitable maximum length are selected.

### Model ###
Encoder Decoder Architecture with Additive(Bahdanau) Attention Mechanism.

![alt text](http://www.aican.hu/wp-content/uploads/2018/08/bahdanau.png)
 
English text tokens are passed to Encoder Embedding layers and then to GRU layers to get Hidden states for each token from input text .Attention weights are calculated using previous Hidden state of Decoder and all Hidden states of Encoder. Weights are passed through softMax layer and the obtained values are multiplied with Hidden states of Encoder and summed to get the final Context vector. This context vector along with Decoder input token are passed in as input to Decoder. This process of calculating Attention weights is continued for all GRU layers of Decoder.
Teacher forcing method is used to train the model. 

### Evaluation ###
BLEU(Bilingual Evaluation Understudy) score is used as Evaluation metric
0.4848 BLEU score is obtained on Train and CV dataset and 0.4329 on Test set.
