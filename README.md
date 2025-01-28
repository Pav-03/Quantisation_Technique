# Quantisation_Technique

## Introduction

Quantization is a method used to reduce the size of a deep learning model by converting its weights and activations from floating-point precision (32-bit or 16-bit) to lower precision (like 8-bit integers). This is essential when deploying models on devices with limited computational or memory resources.

## In this example:

A simple feedforward neural network (SimpleNet) is trained on the MNIST dataset.
The model is then quantized using Post-Training Quantization (PTQ).
The performance (accuracy and model size) is evaluated before and after quantization.
Why Quantization?

## Quantization offers the following benefits:

1) Reduced Model Size: Lower precision weights require less storage.
2) Faster Inference: Integer operations are computationally cheaper compared to floating-point operations.
3) Energy Efficiency: Reducing precision can lower energy consumption during inference.

However, quantization can lead to a small loss in model accuracy, which must be carefully evaluated against the benefits.
