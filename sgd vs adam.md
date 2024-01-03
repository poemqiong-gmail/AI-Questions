# How to choose optimizer for model training

In deep learning, optimizers are functions or algorithms, that adjust the model's parameters during training to minimize a loss function.
When training a new model or finetuning an existing model, choosing the optimizer is an improtant step, because the optimizer affects both the model training speed and the model quality.
This article focuses on the differences between two commonly used optimizers: SGD and Adam, and discuss about how to adjust optimizer to optimize training performance and prevent overfitting.

# What is SGD
Stochastic Gradient Descent has some relatives, like GD (Gradient Descent), Mini-batch GD, and SGD with momentum.

## Gradient Descent (GD):
Calculates the gradient of the loss function using the entire training dataset.
Updates the model parameters based on the average gradient across all data points.
Advantages: More accurate updates, smoother convergence.
Disadvantages: Computationally expensive and slow, especially for large datasets.

## Stochastic Gradient Descent (SGD):
Calculates the gradient of the loss function using a single data point (sample) from the training dataset.
Updates the model parameters based on the gradient of that single data point.
Advantages: Faster than GD, less memory intensive.
Disadvantages: Noisy updates, can lead to erratic convergence.

## Mini-batch Gradient Descent (mini-batch GD):
Calculates the gradient of the loss function using a small batch of data points (e.g., 32 or 64) at each iteration.
Updates the model parameters based on the average gradient across the mini-batch.
Advantages: Combines the benefits of GD and SGD. Faster than GD, less noisy than SGD, often converges faster than SGD.
Disadvantages: Still requires tuning the mini-batch size for optimal performance.

## SGD with momentum:
Similar to SGD, but it adds a "momentum term" that considers the past gradients, helping to overcome the noisy updates of SGD.
Can converge faster than SGD, especially for problems with smooth error surfaces.
Requires tuning an additional hyperparameter (momentum coefficient) for optimal performance.

## Summary
In general, mini-batch GD is the preferred choice for deep learning as it offers a good balance between speed, accuracy, and computational efficiency.
However, the best choice for a specific problem may depend on factors such as the size of the dataset, the available computational resources, and the desired level of accuracy.

# What is Adam

# Comparisions

# Conclusion
