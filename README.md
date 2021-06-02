# Project: Transfer Learning Using VGG16 Network As Feature Extractor
## Objective: To classify two types of similar dogs, namely Pomeranian and Chihuahua.

### Brief

This small project is an attempt to train a classifer using transfer learning. The classifier will detect two species of similar small sized dogs, namely Pomeranian and Chihuahua.
Goal is to demonstrate how transfer learning can be used on small amount of data.

### Core Ideas:

1) A pretrained convolutional network will be used as a feature extractor.
2) The pretrained network is VGG16 which has been pretrained on ImageNet.
3) ImageNet has a lot of images of dogs, so the VGG16 network is familiar with extracting dog features. 
4) The fully connected layers of VGG16 is replaced with a custom classifier. 
5) The custom classifier will be a simple fully connected network to avoid overfitting the small dataset. 
6) After training, the model will be evaluated and wrongly classified images will be displayed for an easy human analysis of possible reasons for wrong classification. 
7) 70% of data will be for Training, 20% for Validation and 10% for Testing. 

### Datasets:
Comprised of images of pomeraninans and chihuahua collected over the internet. Some of the photos are my personal collection. 
* 202 images of pomeranians.
* 201 images of chihuahua. 

