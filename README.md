# AIParkinScan (AIPS)

## Table of Contents
* About
* Technologies 
* Usage

## About
AIParkinScan (AIPS) is an artificial intelligence software used for the diagnosis of Parkinson's disease. It asks for the input of a drawing and an audio file, which is evaluated for inconsistency that is caused by micrographia or voice tremors. If inconsistency is detected, it is a strong indication of Parkinson's, as tremors and micrographia are common symptoms of Parkinson's.

Our aim is to develop an easy, accurate, and efficient way to diagnose Parkinson's disease. There are currently limited and unofficial tests for Parkinson's, and even after diagnosis, symptoms need to be carefully monitored. Using our software, diagnosis of Parkinson's becomes widely available to all, and can also be used for tracking of symptom progression.

The software designed for AIParkinScan utilizes both audio and image data taken from those who are afflicted with Parkinson’s disease and those who do not have the disease. The first neural network uses audio data. The audio data is preprocessed by converting each audio file in the training and testing sets into colored images of spectrograms for processing by the convolutional neural network. The images are run through an ImageDataGenerator to convert each image into a grayscale group. A novel convolutional neural network utilizing maxpooling, dropout, and convolutional 2d layers is trained using the spectrograms and is validated with test data. The second algorithm uses the image data of spirals drawn by those afflicted with Parkinson’s, signaling micrographia, which is a symptom of the disease that results in small handwriting. This data is fed into ImageDataGenerators that augment the data using zoom, cropping, and shifting to create an even greater number of unique images to train the classifier on. The Random Forest algorithm determines the pattern in the data and outputs the accuracy. The novel convolutional neural network is run on the audio data, the Random Forest classifier is run on the spiral data, weights are assigned for each result, and the software calculates and outputs the test result on the website.

## Technologies 
Project was created with:

* Python version: 3.10
* Flask version: 2.2.1
* Bootstrap version: 4.3.1
* CSS version: 3
* JavaScript
* Google Colab 
* jQuery

## Usage

For the spiral test, the Kaggle API was downloaded.
For the audio test, files were downloaded locally from Google Colab.

Recommended packages/modules:
* tensorflow
* numPy
* cv2
* matplotlib.pyplot
* pandas
* os
* shutil
* matplotlib.image

