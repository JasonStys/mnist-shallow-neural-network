# MNIST Shallow Neural Network

A Keras and TensorFlow project that implements a shallow neural network for handwritten digit classification using the MNIST dataset. The notebook walks through loading image data, visualizing sample digits, preprocessing pixel values, building a neural network, checking parameter counts, and training the model.

## Project Overview

This project was completed for CS 478 as a class activity focused on implementing a shallow neural network. It uses the MNIST handwritten digit dataset, where each image is a 28 by 28 grayscale digit image labeled from 0 through 9.

The project demonstrates the full beginner deep learning workflow:

- Load the MNIST dataset
- Inspect training and validation shapes
- Display sample handwritten digits
- View an individual validation image and its pixel grid
- Flatten 28 by 28 images into 784 value vectors
- Normalize pixel values from 0 through 255 into a 0 through 1 range
- Convert labels into one hot encoded class vectors
- Build a shallow fully connected neural network
- Train the model with stochastic gradient descent
- Evaluate validation performance

## Model Architecture

The model is built with Keras Sequential and contains two dense layers.

| Layer | Output Size | Activation | Parameters |
|---|---:|---|---:|
| Dense hidden layer | 64 | Sigmoid | 50,240 |
| Dense output layer | 10 | Softmax | 650 |

Total trainable parameters: 50,890

The output layer has 10 units because MNIST contains 10 digit classes.

## Dataset

The project uses the MNIST dataset from Keras.

| Split | Shape |
|---|---|
| Training images | 60,000 by 28 by 28 |
| Training labels | 60,000 |
| Validation images | 10,000 by 28 by 28 |
| Validation labels | 10,000 |

## Technologies Used

- Python
- NumPy
- Matplotlib
- Keras
- TensorFlow
- Jupyter Notebook

## Files

```text
.
├── CS478_01_Jason_Stys_CA3_Implement_a_Shallow_Neural_Network.ipynb
├── Jason_Stys_CS478_01_CA3_Implement_a_Shallow_Neural_Network.pdf
├── README.md
└── requirements.txt
```

## How to Run

Clone the repository.

```bash
git clone https://github.com/your-username/mnist-shallow-neural-network.git
cd mnist-shallow-neural-network
```

Install the required packages.

```bash
pip install tensorflow numpy matplotlib notebook
```

Launch Jupyter Notebook.

```bash
jupyter notebook
```

Open the notebook and run all cells.

## Training Configuration

The notebook compiles the model with:

- Mean squared error loss
- Stochastic gradient descent optimizer
- Learning rate of 0.01
- Accuracy as the main metric
- Batch size of 128
- 200 configured training epochs

## Current Output Note

The uploaded notebook shows the model training process, but the saved run was interrupted before completing all 200 epochs and before the final evaluation cell finished. The last fully completed logged epoch in the provided notebook output is epoch 57, which shows validation accuracy of about 57.28 percent.

For the best portfolio version of this repository, rerun the notebook from start to finish before committing the final notebook output.

## Skills Demonstrated

- Neural network implementation with Keras
- Dataset loading and inspection
- Image visualization with Matplotlib
- Data preprocessing for deep learning
- Pixel normalization
- Label encoding
- Model architecture design
- Parameter count verification
- Training and validation workflow
- MNIST digit classification

## Possible Future Improvements

- Replace mean squared error with categorical cross entropy for multi class classification
- Use ReLU for the hidden layer
- Try Adam or RMSprop optimizers
- Add training and validation accuracy plots
- Add a confusion matrix for model evaluation
- Save the trained model
- Add a prediction cell for custom digit images
- Compare shallow neural network performance against a convolutional neural network

## Portfolio Summary

This project demonstrates a complete introductory deep learning workflow by building a shallow neural network for MNIST handwritten digit classification. It highlights practical experience with Keras, TensorFlow, NumPy, Matplotlib, image preprocessing, one hot encoding, model construction, and validation based training.
