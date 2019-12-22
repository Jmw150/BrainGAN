# Generative Adversarial Networks

>"the coolest idea in machine learning in the last twenty years." - Yann LeCun

## Introduction
**Generative adversarial networks**(GANs) are a recent innovation(2014) in machine learning invented by Ian Goodfellow and his colleagues. Given a training set, a neural network will learn to generate new data with the same statistics as the training set.
For example, GANs can use a training set of photographs of human faces to create images of human faces. These generated images don't belong to any real person.

![alt text](https://github.com/pejner/keras-gan/blob/master/images/gan_faces.png "Generated faces from GAN created by NVIDIA")

### How do GANs work?
GANs consist of two neural networks that contest with each other. The generative network generates plausible candidates while the discriminative network evaluates candidates by distinguishing the generator's fake data from real data.

At the beginning of training, the generator will produce data that is obviously fake and the discriminator quickly learns to tell that it is fake data:
![alt text](https://github.com/pejner/keras-gan/blob/master/images/bad_gan.svg "Bad GAN example")

As training continues, the generator will continue to get closer to producing output that can fool the discriminator:
![alt text](https://github.com/pejner/keras-gan/blob/master/images/ok_gan.svg "Decent GAN example")

Eventually, if the generator training goes well, the generator will produce data which is difficult to distinguish as fake or real. The discriminator gets worse at telling the differences and accuracy decreases:
![alt text](https://github.com/pejner/keras-gan/blob/master/images/good_gan.svg "Good GAN example")

Picture of the whole system:
![alt text](https://github.com/pejner/keras-gan/blob/master/images/gan_diagram.svg "GAN overview")

## GAN Anatomy

### Discriminator
The discriminator in a GAN is a classifier. The discriminator tries to distinguish real data from the data created by the generator.

#### Discriminator Training
During discriminator training, the generator does not train. The weights for the generator remain constant while it produces images for the discriminator to train on.

The data used for training the discriminator comes from two sources:

- **Real Data** are considered positive instances during training.
- **Fake Data** are considered negative instances during training.

If the discriminator misclassifies real instance as fake or fake data as real, the discriminator loss penalizes the discriminator. Discriminator will use the discriminator loss to update its weights through backpropagation.

### Generator
The goals of the generator is to fool the discriminator. Using feedback from the discriminator, the generator will create fake data and learn to make the discriminator classify generator output as real data.

#### Random Input
Typically with with deep learning models, input data is an instance that we want to classify or make a prediction about. However, with GANs we want output that is entirely new data instances. Therefore, the generator will start by taking random noise as its input. The generator will then transform this noise into meaningful output.

#### Discriminator helps train the Generator
Typically, we alter a neural network's weights to reduce the error or loss of its output. However, with GANs, the generator is not directly connected to the loss we are trying to affect(the discriminator is). The generator loss penalizes the generator whenever it produces data that the discriminator classifies as fake.

Backpropagation adjusts each weight by calculating the weight's impact on the output. Backpropagation start with the output from the discriminator and flows back through the disciminator into the generator to obtain gradients. The gradients are used to change the generator weights.
