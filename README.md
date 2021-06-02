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

**Google Colab is used to build this model**

### Datasets:
Comprised of images of pomeraninans and chihuahua collected over the internet. Some of the photos are my personal collection. 
* 202 images of pomeranians.
* 201 images of chihuahua. 

**Sample Images:**
![SamplePom_Images](https://user-images.githubusercontent.com/61535921/120502319-e79a0780-c3f4-11eb-856c-3f59807547dc.png)
![SampleChihuahua_images](https://user-images.githubusercontent.com/61535921/120502328-e9fc6180-c3f4-11eb-8d52-6619657c163c.png)

### Expected Data Directory Structure
As I will be using the ImageDataGenerator class's method called flow_from_directory(), the images of the two dog types must be organized according to the directory structure show in the diagram below.
![Featureextractor_diagram](https://user-images.githubusercontent.com/61535921/120498986-43af5c80-c3f2-11eb-8e61-a8cfe8b1e039.jpg)


### Results
![Model_accuracy](https://user-images.githubusercontent.com/61535921/120509980-95101980-c3fb-11eb-889f-5436cf2edfce.png)
![Model_loss](https://user-images.githubusercontent.com/61535921/120509996-97727380-c3fb-11eb-9ea3-587b8d6136a3.png)
![ConfusionMatrix](https://user-images.githubusercontent.com/61535921/120510003-993c3700-c3fb-11eb-8d83-553dccec670c.png)

**Wrongly Classified Images**
![WronglyClassified](https://user-images.githubusercontent.com/61535921/120510274-d7d1f180-c3fb-11eb-8cbf-2539db63c750.png)

### Some Observation
Start with a small fully connected layer. Because there is only small number of images available for training, if you have a large fully connected layer for classification, it will tend to overfit easily or the network simply memorized the training data.

High dropout rate will cause wild swings in the training data. 

Some Pomeranians and long-haired Chihuahuas can be difficult to distinguish even for humans. 
The model also tend to classify images wrongly whenever there are two types of dogs in the same image.

**Fine Tuning**
If you attempt to do fine tuning, don't turn on too many layers for training. There is insufficient data to train the the initial layers. 

