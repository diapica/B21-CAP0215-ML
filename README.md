# SkinDec - Machine Learning Model for B21-CAP0215 Capstone Project - B21-CAP0215-ML

## About Project
This project was created to fulfill final capstone project held by Bangkit 2021.
This project is about a model that used to do a classification for human skin type especially face skin type. At the end, this model will be implemented on server to provide a classification result to android users.
This project was built using [Google Colab](colab.research.google.com). We also use [MobileNet_V2 by Tensorflow](https://tfhub.dev/google/tf2-preview/mobilenet_v2/classification/4) as part of our model.

## Contributor:
1. Rindang Tavip Supriyanto (M0070660)
2. Sandro Owen (M2712510)

## Recommended requirement
1. [TensorFlow: 2.5.0](https://www.tensorflow.org/api_docs)
2. [NumPy: 1.20.3](https://numpy.org/doc/)
3. [Keras: 2.4.3](https://keras.io/)

## Dataset
At first we will only have 5 labels for our model. There are **normal**, **dry**, **scar**, **oily**, and **acne**. 
We collected our dataset from various source such as [**Kaggle**](https://www.kaggle.com/shubhamgoel27/dermnet), [**Shutterstock**](https://www.shutterstock.com/search/scar+face), and [**Dermnetnz**](https://dermnetnz.org/topics/acne-face-images/). Due to the limited of datasource for oily skin type, we expand our oily skin type dataset by doing image augmentation (We add oily effect to normal skin to create more oily skin type dataset). We also use photo provider website created by AI, [**Generated Photos**](https://generated.photos/).

Our dataset are available on this repository. You also can download our dataset directly from [here](https://drive.google.com/uc?id=1BlQ0_uY3uRNxSxakjy2WyQu-fvRU8TfN)

## Directories and Files
| **Directory **                                    | **Description**
|---                                                |---
| /Dataset                                          | Dataset Folder
| /Model/skindec.ipnyb                              | Code used to create model
| /Model/saved_model.zip                            | Saved Model

## Model
| **HyperParameter**                                | **Result**
|---                                                |---
| Trainable                                         | True
| Optimizer                                         | SGD
| Learning Rate                                     | 0.002
| Momentum                                          | 0.9
| Loss Function                                     | Categorical Crossentropy
| Layer Activation                                  | Softmax
| Epochs                                            | 30
| Steps Per Epochs                                  | 20

## Results
With current version, our model got above 90% accuracy with only 30 epochs! Training & validation accuracy increasing rapidly and tend to be stable. Training & validation loss together dropped drastically and stable. The output from this project is a model that can be implemented on our capstone project.

## Other Repositories:
- [Cloud Computing](https://github.com/prawiropanji/B21-CAP0215-CC) configuration for model deployment & server configuration
- [Android Development](https://github.com/wahyurama-creator/B21-CAP0215-MD) apps for connecting server and clinet