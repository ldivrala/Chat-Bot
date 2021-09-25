# Chat-Bot

Dataset :: [Cornell movie corpus](https://www.cs.cornell.edu/~cristian/Cornell_Movie-Dialogs_Corpus.html "Movie Chat Trainset")

* Dataset :: 
  * This dataset contains a large collection of fictional conversations extracted from raw movie scripts:.
  * We will use tensorflow for dataset pipeline.

* Inspiration::
  * We have to train a model for chat bot creation.
  * We will use transformer architecture for our model training.

Tools :: Tensorflow, Keras, Pandas, TextVectorization, Numpy \
Architecture :: Transformer (Encoder, Decoder both)

### Steps::
  1. Dataset:: \
    - First we will filter out our dataset according to our use case. \
    - We will create vectorization(tokenization) layer with the help of training dataset. \
    - Dataset loader batch, shuffle, caching etc.
  
  2. We will use glove vector with 300 dimensions for word embedding. 

  3. Model:: \
    - Transformer Encoder creation with multihead attention. \
    - Positional Embedding, Word Embedding layers creation with mask intialization. \
    - Transformer Decoder creation two dense and one multihead attention.
  
  4. Training:: \
    - We will train our model with 8 head attention layers. \
    - Dense dimension in transformer will be 2048. \
    - WordSequences -> TokenSequences -> (WordEmbedding + PositionalEmbedding) -> Encoder \
    - DecoderSequences(Initial start_token(<SOS>)) -> WordEmbedding -> TransformerDecoder(With Encoder.output) -> Dense(vocab_size) \
    - We will train our model with 40 epochs, rms_prop optimizer, sparse_categorical_crossentropy loss etc..
  
 
