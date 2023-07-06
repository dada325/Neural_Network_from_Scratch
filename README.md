# Neural_Network_from_Scratch
This repo is a ReBuild of the Wheel. Many people say to me it is useless to rebuild the wheel, but for me, it is just to test my understanding of the Neural Network. 


### The Essence of Neural Network

In the Notebook I will implement the following 

1. **Neurons**: Each neuron in a neural network performs a weighted sum of its inputs, adds a bias term, and then applies an activation function. Mathematically, this can be represented as:

    <code>y = f(w • x + b)</code>

    where `y` is the output of the neuron, `f` is the activation function, `w` is the vector of weights, `x` is the vector of inputs, and `b` is the bias.

2. **Activation Functions**: The activation function `f` introduces non-linearity into the model, which allows the network to learn complex patterns. Common activation functions include the sigmoid function (1 / (1 + exp(-x))), the hyperbolic tangent function ((exp(x) - exp(-x)) / (exp(x) + exp(-x))), and the rectified linear unit (ReLU) function (max(0, x)).

3. **Layers**: A neural network is composed of layers of neurons. The output of one layer serves as the input to the next layer. If we denote the weights, biases, and activation function of the `i`-th layer as `w_i`, `b_i`, and `f_i`, and the output of the `i-1`-th layer as `x_i-1`, then the output of the `i`-th layer is:

    <code>x_i = f_i(w_i • x_i-1 + b_i)</code>

4. **Loss Function**: The loss function `L(y, y_hat)` measures the difference between the actual output `y` and the predicted output `y_hat`. Common loss functions include the mean squared error (1/n * Σ(y - y_hat)²) for regression tasks and the cross-entropy loss (-1/n * Σ[y log(y_hat) + (1-y) log(1-y_hat)]) for binary classification tasks.

5. **Backpropagation and Gradient Descent**: Backpropagation is an algorithm for computing the gradient of the loss function with respect to the weights and biases. Once the gradient is computed, the weights and biases are updated using gradient descent:

    <code>w_i = w_i - α * ∂L/∂w_i</code>
    
    <code>b_i = b_i - α * ∂L/∂b_i</code>

    where `α` is the learning rate, `∂L/∂w_i` is the partial derivative of the loss function with respect to `w_i`, and `∂L/∂b_i` is the partial derivative of the loss function with respect to `b_i`.
