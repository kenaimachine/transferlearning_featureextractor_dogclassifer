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

Sample Images:


### Expected Data Directory Structure
As I will be using the ImageDataGenerator class's method called flow_from_directory(), the images of the two dog types must be organized according to the directory structure show in the diagram below.
![Featureextractor_diagram](https://user-images.githubusercontent.com/61535921/120498986-43af5c80-c3f2-11eb-8e61-a8cfe8b1e039.jpg)


### Some Observation
Start with a small fully connected layer. Because there is only small number of images available for training, if you have a large fully connected layer for classification, it will tend to overfit easily or the network simply memorized the training data.

High dropout rate will cause wild swings in the training data. 

The model also tend to classify images wrongly whenever there are two types of dogs in the same image.

