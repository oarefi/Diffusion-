# Diffusion Model from Scratch


This repository contains the implementation of an enhanced diffusion model for reconstructing images from the MNIST dataset using PyTorch. The model architecture is designed to improve expressive power and stability during training. It includes features like early stopping, TensorBoard integration, and visualization of reconstructed images.

## Features

- **Model Architecture**: The model uses multiple fully connected layers with batch normalization and ReLU activation functions to increase its expressive power.
- **Gaussian Diffusion Process**: The model is trained to reverse the effects of a Gaussian diffusion process applied to input images.
- **Early Stopping**: To prevent overfitting, training stops early if there is no improvement in validation loss for a specified number of epochs.
- **TensorBoard Integration**: Training metrics are logged and visualized using TensorBoard.
- **Model Visualization**: The training process includes visualizing original, noisy, and reconstructed images to ensure the model is learning effectively.
- **Model Saving**: The best model based on validation loss is saved during training.

## Requirements

- Python 3.x
- PyTorch
- torchvision
- matplotlib
- TensorBoard

## Training Details

- **Input Dimension**: 28x28 (flattened to 784)
- **Batch Size**: 64
- **Number of Epochs**: 50 (with early stopping)
- **Learning Rate**: 0.001
- **Early Stopping Patience**: 5 epochs

## Model Architecture

The enhanced diffusion model consists of four fully connected layers with the following configuration:
- **Input Layer**: Concatenates the input image vector with a time step.
- **Hidden Layers**: Three fully connected layers with 256 neurons each, followed by batch normalization and ReLU activation.
- **Output Layer**: A fully connected layer that outputs the reconstructed image vector.

## Visualization

During training, the script visualizes the following:
- **Original Images**: The original input images.
- **Noisy Images**: Images after applying the Gaussian diffusion process.
- **Reconstructed Images**: Images reconstructed by the model from the noisy inputs.

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue.

## License

This project is licensed under the MIT License.
