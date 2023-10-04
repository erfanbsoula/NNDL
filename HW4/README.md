# NNDL - Homework 4

### 1. Image Captioning

In this section, we implemented an image captioning model based on the research article [Image Captioning](https://arxiv.org/abs/1805.09137). Pre-trained Resnet18 is used to extract features from the input images. Image features are projected into the embedding space by a fully connected layer and fed to the LSTM layers to generate the caption. The model is trained on flickr8k dataset and word embeddings are learned from scratch by an embedding layer during training.

### 2. Intent Classification

In this section, we train a model for text classification using bidirectional LSTM architecture following the research article titled ["Intent Classification in Question-Answering Using LSTM Architectures"](https://arxiv.org/abs/2001.09330). We used pre-trained GloVe for embedding the preprocessed text data.

