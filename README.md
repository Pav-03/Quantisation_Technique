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

## Post-Training Quantization?

Post-Training Quantization (PTQ) is a technique used in deep learning to reduce the size and computational requirements of a trained model without retraining it. This is achieved by converting the model's weights and/or activations from 32-bit floating-point (FP32) precision to lower precision, such as 8-bit integers (INT8). PTQ is particularly useful for deploying models on resource-constrained devices like mobile phones, IoT devices, and edge hardware.

### Key Benefits of PTQ

1) Reduced Model Size: Lowering the precision of weights significantly reduces the storage requirements.
2) Faster Inference: INT8 operations are computationally cheaper and faster than FP32 operations, enabling faster inference on compatible hardware.
3) Energy Efficiency: Lower precision arithmetic reduces power consumption, making it ideal for battery-powered devices.

### How It Works

1) A pre-trained floating-point model is taken as input.
2) Observers are inserted into the model to collect statistics on weights and activations during a few inference passes (using a small dataset).
3) The collected statistics are used to determine quantization parameters (scale and zero-point).
4) The floating-point weights and activations are converted to INT8 during quantization.

Unlike quantization-aware training (QAT), PTQ doesn’t require the model to be retrained, making it simpler and less time-intensive.
