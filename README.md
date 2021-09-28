# English_to_Hindi_Machine_Translation_using_Attention_Mechanism
Encoder Decoder architecture with Attention Mechanism to translate sentences from English to Hindi
### Data set
Text data is downloaded from(https://www.kaggle.com/aiswaryaramachandran/english-to-hindi-neural-machine-translation?select=Hindi_English_Truncated_Corpus.csv)

### Text preprocessing
Both the texts are processed using regex to remove unwanted words. sentences with suitable maximum length are selected.

### Model ###
Encoder Decoder Architecture with Attention Mechanism model is used.

![alt text](https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.tensorflow.org%2Ftext%2Ftutorials%2Fnmt_with_attention&psig=AOvVaw2nSW8i0DFqaK1EFfxdulTj&ust=1632892680210000&source=images&cd=vfe&ved=0CAgQjRxqFwoTCPiMkMX1oPMCFQAAAAAdAAAAABAD)
 
English text tokens are passed to Encoder Embedding layers. Final hidden states of  unit are passed in as initial states to Decoder LSTM units to generate Hindi text tokens. 
Teacher forcing method is used to train the model. 

### Evaluation ###
BLEU(Bilingual Evaluation Understudy) score is used as Evaluation metric
0.4848 BLEU score is obtained on Train and CV dataset and 0.4329 on Test set.
