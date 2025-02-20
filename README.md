Project Title: Dog vs. Cat Image Classifier Using CNN

Project Overview:
This project demonstrates how to build a Convolutional Neural Network (CNN) to classify images into two categories: Dog vs. Cat. The model utilizes TensorFlow and Keras for building and training the CNN. The dataset consists of images from two classes (dogs and cats), and the task is to classify the images accordingly.

Key Steps in the Project:

Data Loading: The images are loaded from a directory structure where each subdirectory represents a class (e.g., dogs and cats). The dataset is divided into training and validation sets.

![Model Architecture](images\1.png)


Data Preprocessing: Image pixel values are normalized to the range [0, 1] by dividing by 255.
The images are resized to (256, 256) pixels for consistency.

CNN Architecture: A simple yet effective Convolutional Neural Network (CNN) is built using multiple convolutional layers for feature extraction, max-pooling layers for dimensionality reduction, and dense layers for classification. Batch Normalization and Dropout are used to improve training speed and prevent overfitting.

Model Compilation: The model is compiled with the Adam optimizer and binary crossentropy loss function, suitable for binary classification tasks.

Model Training: The model is trained for 10 epochs, and performance is monitored using validation data.

Technologies Used:
TensorFlow and Keras for deep learning model development.
Python for programming and model implementation.                                                                                                                                                                              
Model Training Results:
The model was trained for 10 epochs, and here are the key observations from the training process:

Accuracy Progression:
The training accuracy started at 56.28% in the first epoch and gradually increased to 96.87% by the tenth epoch. The validation accuracy fluctuated but peaked at 80.94% in epoch 9, settling at 77.10% in the final epoch.

Loss Progression: The training loss significantly decreased from 2.48 in epoch 1 to 0.0852 in epoch 10, indicating the model was learning effectively.
The validation loss, however, did not decrease as expected. It started at 0.7568 in epoch 1, improved to 0.4465 in epoch 5, but then increased to 0.7801 in epoch 10.

Key Takeaways:
The model learned well on the training dataset, achieving high accuracy.
The validation accuracy and loss fluctuated, which suggests overfitting—the model performed exceptionally well on training data but struggled to generalize to unseen validation data.
The increasing validation loss from epoch 5 onward suggests the model is memorizing the training data rather than learning generalizable patterns.


Possible Further Improvements we can make to improve performance and reduce overfitting:
- add more data
- data augmentation
- L1/L2 Regularizer
- Dropout  - (used)
- Batch Norm  - (used)
- Reduce Complexity
