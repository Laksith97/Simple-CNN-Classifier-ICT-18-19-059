# Implementation of a Simple CNN Model for Multi-Class Image Classification  

This project demonstrates the implementation and evaluation of a Convolutional Neural Network (CNN) to classify fashion items into ten categories using the Fashion-MNIST dataset. The model achieves robust performance and provides insights into the application of CNNs in real-world classification tasks.  

## Overview  
- **Objective**: To classify grayscale images of fashion items into one of ten categories.
- **Dataset**: [Fashion-MNIST](https://www.kaggle.com/datasets/zalando-research/fashionmnist) 
- **Categories**:  
  1. T-shirt/top  
  2. Trouser  
  3. Pullover  
  4. Dress  
  5. Coat  
  6. Sandal  
  7. Shirt  
  8. Sneaker  
  9. Bag  
  10. Ankle Boot  

## Features  
- **Balanced Dataset**: Equal samples across categories.  
- **Compact and Standardized**: Efficient training with normalized 28x28 grayscale images.  
- **Real-World Applicability**: Retail and e-commerce use cases for inventory and recommendation systems.  

## Model Architecture  
The CNN architecture includes:  
1. **Input Layer**: Accepts 28x28 grayscale images.  
2. **Convolutional Layers**:  
   - Two layers with 32 and 64 filters (kernel size: 3x3, activation: ReLU).  
3. **Pooling Layers**:  
   - Two max-pooling layers (pool size: 2x2).  
4. **Flatten Layer**: Converts feature maps into a 1D vector.  
5. **Fully Connected Layers**:  
   - Dense Layer (128 neurons, ReLU activation).  
   - Dropout Layer (rate: 0.5).  
   - Output Layer (10 neurons, softmax activation).  

## Training and Optimization  
- **Dataset Preparation**:  
  - Training samples: 30,000 (80% training, 20% validation).  
  - Testing samples: 5,000.  
- **Optimizer**: Adam with a learning rate of 0.001.  
- **Loss Function**: Categorical Cross-Entropy.  
- **Early Stopping**: Prevents overfitting by halting training after 5 epochs with no validation improvement.  
- **Data Augmentation**: Rotations, zooms, and shifts to enhance generalization.  
- **Epochs**: Trained for 30 epochs with performance improvements in extended training phases.  

## Evaluation Metrics  
- **Accuracy**: 90% on the test set.  
- **Classification Report**: High precision, recall, and F1-scores for most categories.  
  - Notable challenges in "Shirt" classification due to overlapping features.  
- **Confusion Matrix**: Highlights true positives and misclassifications.  
- **ROC Curves & AUC**:  
  - Average AUC score: 0.98.  
  - Near-perfect performance for categories like Trouser, Sandal, and Bag.  

## Results  
The project showcases the effectiveness of CNNs for image classification tasks. The model demonstrates high accuracy and robustness, making it suitable for real-world applications.  

## How to Use  
1. **Clone Repository**:  
   ```bash
   git clone https://github.com/Laksith97/Simple-CNN-Classifier-ICT-18-19-059.git
