# NNDL - HW3

### 1. Transfer Learning

In this section, we trained a model for land use and land cover classification by transfer learning. We utelized the VGG16 model with pre-trained weights on Imagenet as the backbone (feature extractor) of our model. We froze the backbone and trained the following fully connected layars on [EuroSAT Dataset](https://www.researchgate.net/publication/319463676_EuroSAT_A_Novel_Dataset_and_Deep_Learning_Benchmark_for_Land_Use_and_Land_Cover_Classification), achieving an accuracy of 88%.

### 2. Object Detection and Counting

In this section we fine-tuned Faster RCNN object detection model on a [custom dataset](https://drive.google.com/file/d/1C2dcUGUipJBMhAVzBqhm1PBFuuu5k2ai/view?usp=sharing) and utelized the resulting model to detect and count objects in images. The dataset was in Pascal VOC format.
