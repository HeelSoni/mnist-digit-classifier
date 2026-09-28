# MNIST Handwritten Digit Classifier (Keras)

## What this project does
Trains a neural network in TensorFlow/Keras to recognize handwritten
digits (0-9) from 28x28 grayscale images.

## Dataset
MNIST: 60,000 training images and 10,000 test images, built into Keras.

## Approach
1. Loaded MNIST and checked shapes and sample images
2. Normalized pixel values from 0-255 to 0-1 for stable training
3. Built a Sequential network: Flatten (784 inputs) -> Dense(128, ReLU)
   -> Dense(10, Softmax)
4. Compiled with the Adam optimizer and sparse categorical crossentropy loss
5. Trained for 5 epochs with a 10% validation split
6. Evaluated on the 10,000 unseen test images

## Results
- Test accuracy: 0.9788
- Loss: 0.0724

## What I learned
- Why normalizing inputs helps neural networks train
- What each layer does and how softmax produces digit probabilities
- Why a separate validation set helps detect overfitting
