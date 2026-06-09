# MNIST Digit Classification with Neural Networks + Streamlit

This project builds and compares multiple neural network models on the **MNIST handwritten digits dataset** and deploys the best model using a **Streamlit web app** for real-time digit prediction.

---

## Dataset: MNIST

The MNIST dataset contains **70,000 grayscale images** of handwritten digits (0–9), each of size **28×28 pixels**. It is a standard benchmark for image classification tasks and is used here to explore preprocessing, model building, and evaluation.

---

## Data Preprocessing

To prepare the data for training:

- Pixel values are **normalized to the range 0–1**
- Images are **reshaped/flattened** into model-compatible input format
- Data is structured for efficient neural network training

---

## Model Development

Four neural network models were built and trained under the same conditions for fair comparison:

### Model 1 (Baseline)
- Single hidden layer
- Sigmoid activation

### Model 2
- Additional hidden layer
- Increased neurons
- Improved activation function

### Model 3
- Deeper architecture
- Optimizer changed from **Adam → SGD**

### Model 4 (Best Model)
- Leaky ReLU activation
- Batch normalization
- Dropout for regularization
- Lower learning rate for better convergence

---

## Best Model

The best-performing model is saved as: "best_model.h5"
## Streamlit Web Application

The trained MNIST model is deployed using a **Streamlit web application** to provide an interactive interface for digit recognition.

The app allows users to upload a handwritten digit image and instantly get a prediction from the trained neural network.

### What the App Does:

- Loads the saved trained model (`best_model.h5`)
- Accepts image uploads from the user
- Preprocesses the input image:
  - Resizes it to **28×28 pixels**
  - Converts it to **grayscale**
  - Normalizes pixel values to match training data
  - Formats the image for model input
- Feeds the processed image into the neural network
- Outputs the predicted digit (0–9)
- Displays the prediction instantly on the web interface

This makes the model usable outside of a notebook environment and provides a simple way to test handwritten digit recognition in real time.
