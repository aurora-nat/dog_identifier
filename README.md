# Dog Idenitfier
## _Udacity Capstone Project for Data Scientist Nanodegree_

Deep Learning Techniques to identifying a dog or human face. 

This project utilizes Convolution Neural Network (CNN) techniques to classify dog breeds and human faces. The models utilize real-world user-supplied images and the famous imageNet database to train or transfer learn new models for the classification of dog breeds. This project fufills the Udacity Data Scientist Nanodegree Capstone Project and our goal of developing an algorithm that could be utilized on a mobile application. Our final algorithm utilizes a transfer learning method to classify the model as this provides the highest accuracy.
For a full description of our project check out the Medium Blog Post: https://nataly-nuila.medium.com/are-you-a-hooman-or-a-dog-f506fa54e19d

## Table of Contents
1. Deep learning techniques used
2. Requirements
3. File Descriptions
4. Installation Instructions
5. API Google Cloud Instructions
6. Implentation Example
7. Licensing 


## Deep Learning Techniques
Some deep learning techniques utilized for this project are:
- Haar Cascaade Front Face Classifier utilized to detect human faces in images
- Google Cloud Vision API to provide another way to detect human faces in images
- ResNet50 Keras Model imported to detect dog breeds in images
- A CNN built from scratch
- CNN Built with transfer learning including bottleneck features from: DogInceptionV3Data.npz, DogResNet50Data.npz, DogVGG16Data.npz, DogXceptionData.npz
- A finall implementation of previously used techniques to develop an algorithm to classify an image as a dog or human and then provide the dog breed the images resembles most. 


## Requirements
For exact requirements please utilize the requirements.txt file
- Python3
- Numpy
- Pandas
- CV2
- TensorFlow
- Keras
- tqdm

## File Descriptions
- haarcascades - folder contains the XML utilize to connect OpenCV Haarcascade Classifier for human face identificcation
- images: a set of sample images the final algorithm utilizes to test run
- saved_models: folder containing the saved weights from our 4 transfer learning models
- dog_app.ipynb - Our Jupyter Notebook going over all steps in our captsone project
- extract_bottleneck_features.py file containing methods to extract the bottle neck features of all the models utilized for transfer learning
- requirements.txt - all the installed program files (and related) that were used to run our dog application
- LICENSE.txt - Udacity license information 

## Installation Instructions
1. Clone the repository and navigate to the downloaded folder:
> git clone https://github.com/aurora-nat/dog_identifier.git
> cd dog_app
2. Download the dog dataset:[Dog Images](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip)
3. Download the [Human Dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/lfw.zip)
4. Download the [Xception Bottleneck Features](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/DogXceptionData.npz) and place in a bottleneck_features folder
5. Optional you can download the rest of the bottleneck features and place them in the bottleneck_features folder if you want to run the bottleneck examples in the code: [ResNet-50](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/DogResnet50Data.npz)
[Inception](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/DogInceptionV3Data.npz)


## Google Cloud Vision API Instructions :
1. Create a Google Cloud Vision account with the email you would like to be authenticated with. Instructions [here](https://cloud.google.com/vision/docs/before-you-begin)
2. Create a Google Cloud app
3. Add a service account agent to your google cloud account for remote use in project. Instructions [here](https://cloud.google.com/iam/docs/service-accounts-create)
4. Download your own service account key credentials. This will be stored in your project. This MUST be done in order to utilize the google cloud vison API. Here are the [instructions](https://cloud.google.com/iam/docs/keys-create-delete)
5. Enable the Cloud Vision API and Billing to ensure everything is properly set up. Instructions [here](https://cloud.google.com/vision/docs/setup)

# Implementation Example: 
    You can find the final algorithm as a class called: Dog_Human_Identifier()
    Using Dog_Human_Identifier:
    ```
    dog_human_classifier = Dog_Human_Identifier()
    dog_human_classifier.classification("images/American_water_spaniel")
    ```
    
## License
    This project was designed by Udacity for the Data Scientist Nanodegree Capstone Project. The Udacity License will be found under LICENSE.txt




