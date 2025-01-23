# SSM (Structured State Space Models)

This repository contains implementations of two simple S4 (Structured State Space for Sequence) models, both trained on the MNIST dataset. The first implementation uses PyTorch, while the second is built entirely with NumPy.

---

## Methodology

### Model Structure  
Both models are based on the S4 structure, as detailed in [this paper](https://arxiv.org/abs/2111.00396).

1. **PyTorch Implementation**  
   - Uses PyTorch's built-in functions for initialisation, training, and evaluation.  
   - The optimiser used is Adam, and cross-entropy is employed as the loss function.  
   - Hyperparameter tuning involved testing batch sizes (64, 128, 256) and learning rates (0.01, 0.001, 0.0005). A batch size of 256 and a learning rate of 0.0005 were found to minimise the testing loss effectively.

2. **NumPy Implementation**  
   - Built from scratch without the use of external deep learning frameworks.
   - We used the same hyperparameters as previously (batch size of 256 and learning rate of 0.0005).

### Dataset  
The models were trained on the MNIST dataset, a classic benchmark dataset consisting of grayscale 28x28-pixel images of digits (0–9), each labeled with its corresponding digit.

The goal of the models is to accurately classify unseen digit images.

### Evaluation  
The evaluation metric used is classification accuracy, calculated as the number of correctly classified images divided by the total number of images in the test set.

---

## Results  

### PyTorch Implementation  

Epoch [1/10], Loss: 0.3586
Epoch [2/10], Loss: 0.3275
Epoch [3/10], Loss: 0.1513
Epoch [4/10], Loss: 0.1352
Epoch [5/10], Loss: 0.1489
Epoch [6/10], Loss: 0.1166
Epoch [7/10], Loss: 0.2430
Epoch [8/10], Loss: 0.1188
Epoch [9/10], Loss: 0.0581
Epoch [10/10], Loss: 0.0534

Test Accuracy: 96.68%

### NumPy Implementation  

Epoch [1/5], Loss: 0.5156
Epoch [2/5], Loss: 0.2174
Epoch [3/5], Loss: 0.1729
Epoch [4/5], Loss: 0.1399
Epoch [5/5], Loss: 0.1267

Test Accuracy: 96.23%

