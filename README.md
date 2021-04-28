# Digit Recognizer

# Objective

- This project belongs to [kaggle's competitions](https://www.kaggle.com/c/digit-recognizer) and I carried out as a part of a specialization called [DeepLearning.AI TensorFlow Developer Specialization](https://www.coursera.org/account/accomplishments/specialization/certificate/L6R6AFWVXHZT) which is given by DeepLearning.AI. This specialization is conformed by 4 courses: 
1. Introduction to TensorFlow for Artificial Intelligence, Machine Learning, and Deep Learning 
2. Convolutional Neural Networks in TensorFlow 
3. Natural Language Processing in TensorFlow 
4. Sequences, Time Series and Prediction

Specifically this project is part of the second course in this specialization. 

- MNIST ("Modified National Institute of Standards and Technology") is the de facto “hello world” dataset of computer vision. Since its release in 1999, this classic dataset of handwritten images has served as the basis for benchmarking classification algorithms. As new machine learning techniques emerge, MNIST remains a reliable resource for researchers and learners alike.

- The objective of this study is to correctly identify digits from a dataset of tens of thousands of handwritten images.

# Code and Resources Used

- **Phyton Version:** 3.0
- **Packages:** pandas, numpy, sklearn, seaborn, matplotlib

# Data description 

- The data files train.csv and test.csv contain gray-scale images of hand-drawn digits, from zero through nine.

- Each image is 28 pixels in height and 28 pixels in width, for a total of 784 pixels in total. Each pixel has a single pixel-value associated with it, indicating the lightness or darkness of that pixel, with higher numbers meaning darker. This pixel-value is an integer between 0 and 255, inclusive.

- Each pixel column in the training and test set has a name like pixelx, where x is an integer between 0 and 783, inclusive.

- The figures looks like that
  <p align="center">
   <img src="https://github.com/lilosa88/DigitRecognizion/blob/main/Images/Captura%20de%20Pantalla%202021-04-28%20a%20la(s)%2022.16.22.png" width="460" height="140">
  </p> 
  
  # Feature engineering
  
  - Defining X and Y from the df_train dataset
  - We check which is the maximum value that you can find in one row of the df_train dataset. The maximum value is 255. If we are training a neural network, for    various reasons it's easier if we treat all values as between 0 and 1, therefore we need to normalize our datasets.
  - So we normalize dividing by 255.
  - Resahping, following X = X.values.reshape(-1, 28,28,1)
  - Label encoding for the y label
  - Split into train and test

# Neural Network model

We compare the performance of two following two neural networks:
- Simple Model (Accuracy 0.97238)
- Model with double convolutions and pooling (Accuracy 0.9864)

In both case the activation functions used were 'relu' and 'softmax', the lr = 0.001 and as loss function we use categorical_crossentropy.
  
  
