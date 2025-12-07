Neural Network Forward Pass – Project Documentation
1. Overview

This project demonstrates a manual forward pass through a simple artificial neural network.
It is designed to help beginners and intermediate developers understand how activations, weighted sums, and loss functions work internally—without relying on deep learning frameworks like TensorFlow or PyTorch.

The network architecture, activations, and loss calculations are all implemented manually to provide full visibility into the mathematics behind neural networks.

2. Network Architecture

The model contains:

Input Layer

Accepts a single numeric input value.

Hidden Layer

Contains two neurons.

Each neuron applies:

A weighted sum of the input.

A bias term.

A sigmoid activation function to produce the neuron’s output.

Output Layer

Contains one neuron.

Takes the two hidden neuron outputs as inputs.

Applies:

A weighted sum.

A bias term.

A sigmoid activation to produce the final prediction (y_hat).

This structure is similar to a classic single-hidden-layer neural network used for binary classification.

3. Forward Pass Explanation

The forward pass runs through the following steps for every input sample:

Step 1: Input Processing

The network receives one numeric value and prepares it for hidden layer computation.

Step 2: Hidden Layer – Weighted Sums

Each hidden neuron calculates a value called z, which is computed as:

(weight × input) + bias


This is the raw score before activation.

Step 3: Hidden Layer – Activation

The hidden neurons apply the sigmoid activation function to their respective z values.
This produces non-linear outputs, enabling the network to learn complex relationships.

Step 4: Output Layer – Weighted Sum

The outputs from the hidden layer are passed into the output neuron.
Each value is multiplied by a corresponding weight, summed together, and then a bias is added.

Step 5: Output Layer – Activation

The output neuron applies sigmoid activation, producing a prediction (y_hat) between 0 and 1.
This value represents the network's predicted probability.

Step 6: Loss Calculation

The network compares the predicted value with the actual label (y_true) using Mean Squared Error (MSE).
This loss indicates how far the prediction is from the expected output.

Step 7: Result Logging

For every input sample, the program prints:

Input value

Hidden layer raw outputs

Hidden layer activated outputs

Final output neuron score

Predicted output

Error/loss

This makes the forward pass transparent and easy to debug or analyze.

4. Dataset

The example dataset consists of simple binary input–output pairs.
Each pair contains:

An input value

A target label

The network processes each pair sequentially to demonstrate how predictions and loss values differ for each case.

5. Purpose of the Project

This project is intended for developers who want to:

Understand neural networks from the ground up

Learn how activations and losses work mathematically

Build their foundation before moving to framework-based training

Debug or test neural network logic manually

Explore model behavior with different weight, bias, and dataset settings

It is designed as an educational resource rather than a production-level model.

6. How to Run the Project

Follow these instructions:

Step 1: Install Python

Ensure Python 3.7+ is installed on your system.

Step 2: Download the Project File

Save the script locally with any filename, such as:

nn_forward.py

Step 3: Run the Script

Use a terminal or command prompt:

python nn_forward.py

Step 4: View Output

The console will display:

Intermediate computations

Activation outputs

Final predictions

Loss values

Each run processes the entire dataset and prints a detailed forward pass explanation for every input sample.

7. Future Enhancements (Optional Ideas)

You may extend this project to include:

Backpropagation and gradient descent

Multiple hidden layers

Different activation functions

Additional loss functions

Visualization of forward pass values

Training loop and weight updates

If you want, I can generate the extended version as well.
