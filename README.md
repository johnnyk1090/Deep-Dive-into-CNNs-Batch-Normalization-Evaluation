<img src="assets/banner.svg" width="100%" alt="Deep Dive into CNNs: Batch Normalisation. The same convolutional network, with and without batch normalisation, on handwritten digits. What actually changes?">

## The question

Batch normalisation is in almost every modern network, usually without a second thought. This project measures what it buys: a regular CNN and a CNN with batch normalisation, trained side by side on digit classification, with every layer opened up and plotted.

## What is inside

- Plotting classes for the **channels, parameters and activation outputs** of every layer
- **Batch normalisation**: take each neuron's output → compute mean and standard deviation → normalise → scale and shift → pass to the activation function
- **Convolutional neural networks**, trained and compared

## Results

In the comparison plots, the batch-normalised network is ahead from the very first epoch and stays ahead: about **97.7%** validation accuracy after one epoch against about **94.9%** for the regular CNN, finishing near **99%** against **98.6%** (read from the accuracy plot below).

<table>
<tr><td width="50%" valign="top"><img src="graphs/comparison_accuracy.png" width="100%" alt="Validation accuracy per epoch: regular CNN vs CNN with batch normalisation"><br><sub>Validation accuracy per epoch: regular CNN vs CNN with batch normalisation</sub></td><td width="50%" valign="top"><img src="graphs/comparison_loss.png" width="100%" alt="Training loss per iteration for both networks"><br><sub>Training loss per iteration for both networks</sub></td></tr>
<tr><td width="50%" valign="top"><img src="graphs/1st_layer_kernels_before_training.png" width="100%" alt="First-layer kernels before training"><br><sub>First-layer kernels before training</sub></td><td width="50%" valign="top"><img src="graphs/1st_layer_kernels_after_training.png" width="100%" alt="First-layer kernels after training"><br><sub>First-layer kernels after training</sub></td></tr>
<tr><td width="50%" valign="top"><img src="graphs/Output_after_the_1st_CNN.png" width="100%" alt="Activations after the first convolution"><br><sub>Activations after the first convolution</sub></td><td width="50%" valign="top"><img src="graphs/Output_after_the_1st_Relu.png" width="100%" alt="Activations after the first ReLU"><br><sub>Activations after the first ReLU</sub></td></tr>
<tr><td width="50%" valign="top"><img src="graphs/2nd_layer_kernels_before_training.png" width="100%" alt="Second-layer kernels before training"><br><sub>Second-layer kernels before training</sub></td><td width="50%" valign="top"><img src="graphs/2nd_layer_kernels_after_training.png" width="100%" alt="Second-layer kernels after training"><br><sub>Second-layer kernels after training</sub></td></tr>
<tr><td width="50%" valign="top"><img src="graphs/Output_after_the_2nd_CNN.png" width="100%" alt="Activations after the second convolution"><br><sub>Activations after the second convolution</sub></td><td width="50%" valign="top"><img src="graphs/Output_after_the_2nd_Relu.png" width="100%" alt="Activations after the second ReLU"><br><sub>Activations after the second ReLU</sub></td></tr>
<tr><td width="50%" valign="top"><img src="graphs/loss_accuracy_of_normal_CNN.png" width="100%" alt="Regular CNN: training loss and validation accuracy"><br><sub>Regular CNN: training loss and validation accuracy</sub></td></tr>
</table>

## Run it

1. Download `spec-file.txt`.
2. Follow the instructions in `Conda_Virtual_Env.txt`:

```bash
# a new environment from the spec file
conda create --name myenv --file spec-file.txt
# or install the listed packages into an existing environment
conda install --name myenv --file spec-file.txt
```
The full set of environment commands is in [`Conda_Virtual_Env.txt`](Conda_Virtual_Env.txt).

Then open [`CNN_&_BatchNorm.ipynb`](CNN_%26_BatchNorm.ipynb).

## Built with

`Python` · `PyTorch` · `Matplotlib` · `Torchvision` · `math`

<br>

<p align="center"><sub>Part of the work of <a href="https://github.com/johnnyk1090">Giannis Konteas</a> · end-to-end data science</sub></p>
