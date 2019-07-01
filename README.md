# dog-breed-prediction
CNN that classifies dog breeds 

In order to evaluate this code, make sure that you've downloaded the required dog dataset:
* Download the [dog dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip).  Unzip the folder and place it in this project's home directory, at the location `/data/dog_images`. 

## Create a CNN to Classify Dog Breeds (from Scratch)

In this section, I'm creating a CNN that classifies dog breeds from scratch:

<img src="images/from_sratch.png"> 

Test Accuracy of the model created from scratch after 55 epochs: 12% (102/836)

## Create a CNN to Classify Dog Breeds using Transfer Learning

Using transfer learning, I'm creating a CNN that classifies dog breeds using the pretrained ResNet50 architecture. 
ResNet50 is a deep residual network and a very good architecture with 50 layers perfectly suitable for image classification problems. The only adjustment I make to this pre-trained model is changing the number of output features for the last (fc) Linear layer which previously was 1000 (for detecting 1000 classes) to 133 which is the number of classes we are interested in detecting.

Test Accuracy of the model created using transfer learning after 30 epochs: 77% (649/836)

## Predicting Dog Breed with the Transfer Learning Model
Sample results:
_____________________________________________________________________________________________
<img src='images/Beagle_01182.jpg' width="300"> 

Output class: **Beagle** 
_____________________________________________________________________________________________

<img src='images/Greyhound_05562.jpg' width="300"> 

Output class: **Greyhound** 
_____________________________________________________________________________________________

<img src='images/dog1.jpg' width="300"> 

Output class: **Golden retriever**  
_____________________________________________________________________________________________

<img src='images/dog2.jpg' width="300"> 

Output class: **Pomeranian** 
_____________________________________________________________________________________________

<img src='images/dog3.jpg' width="300"> 

Output class: **Chow chow** 
