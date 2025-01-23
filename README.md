# SSM

In this repository we implement two simple S4 (Structured State Space for Sequence) models which are trained on the MINST dataset. The former uses PyTorch while the second version was built only using Numpy.

# Method

We base this model on the S4 structure detailed here. In the first file we make use of PyTorch's built in functions to initialise, train and evaluate our model. We use Adam as our optimiser and cross-entropy as our loss function. After testing various batch sizes (64, 128, 256) and learning rates (0.01, 0.001, 0.0005) we found that a batch size of 256 and a learning rate of 0.0005 best minimise our testing loss.

The dataset we use is the classic MINST dataset which is composed of ... 28x28 pixels images of digits from 0 to 9, each labelled accordingly.

The aim of our model is to appropriatly classify unseen digit images. Finally, our evaluation method is simply the number of correctly classified images divided by the total number of images.

# Results

Epoch [1/5], Loss: 0.3586
Epoch [2/5], Loss: 0.3275
Epoch [3/5], Loss: 0.1513
Epoch [4/5], Loss: 0.1352
Epoch [5/5], Loss: 0.1489
Epoch [6/5], Loss: 0.1166
Epoch [7/5], Loss: 0.2430
Epoch [8/5], Loss: 0.1188
Epoch [9/5], Loss: 0.0581
Epoch [10/5], Loss: 0.0534


Epoch 1/5, Loss: 0.5155643616332608
Epoch 2/5, Loss: 0.21744363777599113
Epoch 3/5, Loss: 0.172894513521342
Epoch 4/5, Loss: 0.1398888802354398
Epoch 5/5, Loss: 0.12673826988745282

