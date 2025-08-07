## Handwritten Digit Classification using ANN (MNIST)

_This project aims to classify handwritten digits (0–9) using a basic Artificial Neural Network (ANN) trained on the built-in MNIST dataset._

#### Dataset Details
- Dataset: MNIST
- Source: `tensorflow.keras.datasets.mnist` 
- Training Samples: 60,000
- Testing Samples: 10000
-Image Shape:** 28 x 28 pixels (grayscale)  
-Labels: Integers from 0 to 9 (10 classes)

#### ML Workflow: 
1. Importing Libraries
    1. `numpy`, `matplotlib` for numerical operations and visualization  
    2. `tensorflow.keras` for dataset loading and model building
2. Data Splitting
    1. Loaded the MNIST dataset from Keras and split into training and test sets  
    2. Images are 28x28 grayscale pixels, and labels are integers representing digits
3. Data Visualization
    1. Visualized several sample digits using `matplotlib` to understand pixel intensity and variation    
4. Model Architecture
    1. The model is a simple feedforward ANN consisting of:
        1. A Flatten layer to reshape each 28x28 image into a 1D array of 784 pixels  
        2. One Dense hidden layer with 128 neurons and ReLU activation  
        3. One Dense output layer with 10 neurons and softmax activation for multiclass classification
    2. Loss Function: Sparse Categorical Crossentropy
    3. Optimizer: Adam
5.  Model Training
    1. Compiled and trained the model for 10 epochs. 
6. Evaluation
    1. Metrics used: `Accuracy`

#### Results
Accuracy Score: 0.97

Loss: 0.004

Val Loss: 0.13

#### Key Observation 
Even a single hidden layer ANN can classify handwritten digits with over 97% accuracy when trained on clean, well-labeled image data like MNIST.

#### Improvements
1. Using convolutional layers (CNN) would likely enhance performance and reduce the number of parameters
2. Using Regularization and dropout could make the model more robust

#### Visualizations
Loss Curve
<img width="748" height="562" alt="Screenshot 2025-08-07 175146" src="https://github.com/user-attachments/assets/6fa0cd85-7866-4c5a-bc96-c90ca375c2e7" />

Val Loss Curve
<img width="728" height="617" alt="Screenshot 2025-08-07 175153" src="https://github.com/user-attachments/assets/8303e3e1-4d37-450f-b9ef-6cdd0ab7b929" />

#### Assumptions
1. All input images are 28x28 grayscale digits  
2. Classes are balanced and labeled correctly  

