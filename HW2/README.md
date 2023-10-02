# NNDL - Homework 2

### 1. Shallow CNN for Image Classification

In this section, we implemented a shallow convolutional neural network for image classification based on the research article titled ["Shallow Convolutional Neural Network for Image Classification"](https://link.springer.com/article/10.1007/s42452-019-1903-4). The SCNNB architecture consists of two convolutional layers, two max-pooling layers, and two fully connected layers with a final softmax activation function. Batch Normalization is added after each convolutional layer to improve network generalization.

### 2. Chest X-Ray Image Classification for Pneumonia Detection

In this section, we fine-tuned a pre-trained EfficientNetB2 model for pneumonia diagnosis from chest X-ray images. The code is based on the research article titled ["Automated Diagnosis of Pneumonia from Classification of Chest X-Ray Images using EfficientNet"](https://www.researchgate.net/profile/Nusrat-Jahan-122/publication/351643298_Automated_Diagnosis_of_Pneumonia_from_Classification_of_Chest_X-Ray_Images_using_EfficientNet/links/60bf9e35a6fdcc512815ddae/Automated-Diagnosis-of-Pneumonia-from-Classification-of-Chest-X-Ray-Images-using-EfficientNet.pdf). The dataset consists of 5863 images, comprising 4273 images from individuals with pneumonia and 1583 images from healthy individuals.

Data augmentation is used during training to compensate for small number of training samples and given the class imbalance in the dataset, different class weights are assigned to deal with the issue. The paper uses Adam optimizer with a learning rate of 0.001 and a batch size of 128. But the same setting produced unsatisfactory results for us.

The following changes helped us achieve a desirable accuracy:

1. Increasing the number of layers allowed for training, leaving only the first 74 layers frozen and allowing 5 out of 7 blocks of the network to be trainable.

2. Reducing the learning rate, as increasing the number of trainable layers and parameters can lead to rapid instability or overfitting. A learning rate scheduler was used to further reduce the learning rate in two stages.

3. Reducing the batch size to 32 to achieve faster convergence.
