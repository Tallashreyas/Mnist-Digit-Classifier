# MNIST Digit Classifier

A beginner-friendly deep learning project using TensorFlow/Keras to classify handwritten digits from the MNIST dataset.

---

## Overview

This project implements a simple Artificial Neural Network (ANN) for handwritten digit recognition.

The model is trained on the famous MNIST dataset containing grayscale images of digits from 0 to 9.

This project demonstrates the complete machine learning workflow:

- Loading data
- Data preprocessing
- Data visualization
- Building a neural network
- Training the model
- Evaluating performance
- Making predictions

---

## Technologies Used

- Python
- TensorFlow / Keras
- NumPy
- Matplotlib
- Jupyter Notebook

---

## Dataset

The project uses the MNIST dataset available directly from TensorFlow.

### Dataset Details

- 60,000 training images
- 10,000 testing images
- Image size: 28 × 28 pixels
- 10 output classes (digits 0–9)

---

## Data Preprocessing

The image pixel values are normalized to improve model performance:

```python
X_train = X_train / 255
X_test = X_test / 255
```

The 28×28 images are flattened into 784-dimensional vectors before being passed into the neural network.

---

## Neural Network Architecture

```python
model = keras.Sequential([
    keras.layers.Dense(100, input_shape=(784,), activation='relu'),
    keras.layers.Dense(10, activation='sigmoid')
])
```

### Model Details

- Input Layer: 784 neurons
- Hidden Layer: 100 neurons (ReLU activation)
- Output Layer: 10 neurons
- Optimizer: Adam
- Loss Function: Sparse Categorical Crossentropy

---

## Training

The model is trained using:

```python
model.fit(X_train_flattened, y_train, epochs=5)
```

---

## Results

The neural network achieves good accuracy on handwritten digit classification using a simple ANN architecture.

Example predictions and visualizations are included in the notebook.

---

## How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/mnist-digit-classifier.git
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook
```

### 4. Open the Notebook

Run:

```text
mnist_digit_classifier.ipynb
```

---

## Future Improvements

Possible enhancements for this project:

- Add Convolutional Neural Networks (CNNs)
- Improve model accuracy
- Build a web interface using Flask or FastAPI
- Deploy the model online
- Add real-time digit drawing and prediction

---

## Author

Shreyas Talla

GitHub: https://github.com/your-username
