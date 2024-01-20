# Covid-Image-Classification-using-CNN
This project involves the development of a Convolutional Neural Network (CNN) for the classification of medical images into two classes: COVID-19 and Healthy. Below is a comprehensive description of the project:

1. Neural Network Architecture Definition:

The project starts by importing necessary modules and classes from TensorFlow and Keras.
It defines a Sequential model, a type of neural network, using convolutional and dense layers.
The architecture includes two convolutional layers with max-pooling, followed by flattening and dense layers, ending with a binary classification output layer.

2. Image Data Augmentation and Generator Setup:

The code involves the importation of the Keras ImageDataGenerator to perform data augmentation on the training dataset.
Augmentation parameters include rescaling, rotation, zooming, horizontal and vertical flipping.
Separate generators are created for the training and validation datasets, with specified target sizes and batch sizes.

3. Model Training Configuration and Callbacks:

The project utilizes early stopping and learning rate reduction callbacks during the training process to enhance model performance.
Early stopping monitors validation loss and stops training if it does not improve for three consecutive epochs.
Learning rate reduction adapts the learning rate if the validation loss plateaus.
The model is compiled using the Adam optimizer, binary crossentropy loss, and accuracy as the metric.
Training is performed for 25 epochs using the previously defined generators for training and validation datasets.

4. Image Prediction and Visualization:

The project includes code for loading an image from a specified path and resizing it to the target size.
The loaded image is visualized using Matplotlib.
The image is converted to a NumPy array and expanded dimensions for compatibility with the model.
A prediction is made using the trained model, and the result is printed, indicating whether the image is predicted as 'COVID-19' or 'Healthy'.
Overall Objective:

