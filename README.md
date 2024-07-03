# README

## Project Title: Lung and Colon Cancer Detection Using Convolutional Neural Networks


### Authors: [Vladimir Čornenki](https://github.com/cornenkiV) and [Nemanja Stjepanović](https://github.com/conamiflo)

---

## Table of Contents

1. [Introduction](#introduction)
2. [About Convolutional Neural Networks (CNNs)](#about-cnns)
3. [EfficientNetB3](#efficientnetb3)
4. [ResNet50V2](#resnet50v2)
5. [Dataset](#dataset)
6. [Problem Statement](#problem-statement)
7. [Methodology](#methodology)
9. [Conclusion](#conclusion)
---

## Introduction

This project focuses on the application of Convolutional Neural Networks (CNNs) to detect lung and colon cancer from medical images. Specifically, we have employed two state-of-the-art architectures: EfficientNetB3 and ResNet50V2, to develop and fine-tune models for accurate classification.

## About Convolutional Neural Networks (CNNs)

Convolutional Neural Networks are a class of deep learning models designed to process data with grid-like topology, such as images. CNNs are particularly effective for image recognition tasks due to their ability to capture spatial hierarchies in images through convolutional layers. These layers apply convolution operations to the input, enabling the network to learn local patterns and features at different levels of abstraction.

## EfficientNetB3

EfficientNet is a family of models that achieve state-of-the-art performance on image classification tasks by balancing network depth, width, and resolution. The EfficientNetB3 model is a specific variant that optimizes these dimensions to maximize accuracy while maintaining computational efficiency. EfficientNet employs a compound scaling method that uniformly scales all dimensions of the network, resulting in better performance with fewer parameters and FLOPS (Floating Point Operations per Second).

## ResNet50V2

ResNet, or Residual Network, introduced the concept of residual learning, which allows for the training of very deep networks. The ResNet50V2 model is a 50-layer residual network that includes several enhancements over the original ResNet, such as improved batch normalization and the use of identity mappings. This architecture addresses the vanishing gradient problem and enables the training of deeper networks with higher accuracy.

## Dataset

We used a dataset consisting of medical images of lung and colon cancer. The dataset contains a balanced set of images representing cancerous and healthy tissue. Each image is labeled accordingly, enabling supervised learning for classification.

## Problem Statement

Detecting cancer at an early stage is crucial for effective treatment and patient survival. Traditional methods of cancer detection involve manual examination of medical images by specialists, which can be time-consuming and prone to human error. By leveraging CNNs, we aim to develop an automated system for accurate and efficient cancer detection from medical images.

## Methodology

### Data Preprocessing

1. **Image Resizing**: All images were resized to a uniform dimension to match the input requirements of EfficientNetB3 and ResNet50V2.
2. **Normalization**: Pixel values were normalized to the range [0, 1] to facilitate better model training.

### Model Training

1. **EfficientNetB3**: 
   - The pre-trained EfficientNetB3 model was fine-tuned on our dataset.
   - The final fully connected layer was replaced to match our classification task.
   

2. **ResNet50V2**: 
   - The pre-trained ResNet50V2 model was similarly fine-tuned.
   - The final fully connected layer was adjusted for our classification.
   - Initial layers were frozen to retain pre-trained features while training only the top layers.

### Evaluation

- Models were evaluated using metrics such as accuracy, precision, recall, and F1 score.
- Training and validation loss and accuracy were monitored to detect overfitting and adjust training strategies accordingly.


## Conclusion

Both EfficientNetB3 and ResNet50V2 demonstrated strong performance in detecting lung and colon cancer from medical images. The fine-tuning approach allowed us to leverage the strengths of these pre-trained models, achieving high accuracy with relatively small datasets. Future work could explore further optimization techniques and the application of these models to other types of cancer.
