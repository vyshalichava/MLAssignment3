**Project Objectives**
Build a Neural Network Library from scratch that can create and train neural networks.
Understand how forward and backward propagation work for different types of layers and functions.
Gain hands-on experience with core concepts of deep learning, like fully connected layers, activation functions, loss functions, and backpropagation.
Solve a simple XOR problem using your custom-built neural network.
<br>
Below is the breakdown:
<br>
**1. Base Layer Class**<br>
Purpose: Define a base class (Layer) for other layers to inherit from. It contains abstract methods forward and backward, which enforce that every layer implements these functions.
Forward pass: The method calculates the output of the layer given an input.
Backward pass: The method computes the gradients during backpropagation.
<br>
**2. Linear Layer (Fully Connected Layer)**<br>
Purpose: Implement a linear layer that computes the weighted sum of inputs and adds bias.
Forward pass: This layer computes the dot product of the input with weights and adds bias.
Backward pass: It computes the gradients of the weights, biases, and inputs, which are required for updating the model parameters during training.
<br>
**3. Activation Functions**<br>
Sigmoid Layer: Implements the sigmoid activation function, which squashes the input into the range (0,1).
Forward pass: Computes the sigmoid function.
Backward pass: Computes the derivative of the sigmoid function to propagate the gradients.
Tanh Layer: Implements the hyperbolic tangent activation function.
Forward pass: Computes the tanh function.
Backward pass: Computes the derivative of the tanh function.
Softmax Layer: Implements the softmax activation function for multi-class classification.
Forward pass: Computes softmax, which normalizes input values into probabilities.
Backward pass: Simplified when used with cross-entropy loss for classification tasks.
<br>
**4. Cross-Entropy Loss**
Purpose: Implements cross-entropy loss for classification problems.
Forward pass: Computes the cross-entropy between predicted probabilities and actual labels.
Backward pass: Computes the gradient of the loss with respect to the predictions to facilitate backpropagation.
<br>
**5. Sequential Class**
Purpose: Implements a sequential container to build the neural network layer by layer. It allows you to add layers, perform forward propagation through all layers, and compute backward propagation through the entire network.
Functionality:
Add layers sequentially.
Run forward and backward passes for the whole network.
Save and load model weights for future use or evaluation.
<br>
**6. XOR Problem Solution**
Purpose: Demonstrates how to construct a neural network to solve the classic XOR problem using the created library.
**Steps:**
Construct a network with 1 hidden layer and 2 nodes.
Train the model on XOR input-output pairs.
Implement forward and backward passes with sigmoid and tanh activations.
Save the trained model's weights.
<br>
**7. Polymorphism and Layer Inheritance**
Each layer (LinearLayer, SigmoidLayer, TanhLayer, SoftmaxLayer) inherits from the base Layer class, which enforces the implementation of forward and backward methods through polymorphism.
This design ensures that each layer can be used interchangeably in the network, and the network class (Sequential) can call the forward and backward methods of any type of layer in a consistent manner.
<br>
**8. Training and Testing**
After constructing the library, you implemented a small neural network to solve the XOR problem using one hidden layer with 2 nodes. XOR is a classic example of a non-linearly separable problem, so it's a good test for a neural network.
You tried two activation functions—Sigmoid and Tanh—to compare which one works better for training the network.
You also implemented functionality to save the trained model’s weights into a file (XOR_solved.w) and to load the weights for evaluation or further training.
<br>
So, this is the summary of what I did:
1. Implemented core building blocks of a neural network, such as linear layers and activation functions.
2. Created reusable classes for constructing, training, and saving neural networks.
3. Solved the XOR problem using a simple network architecture.
4. Compared activation functions to see which performs better for this specific problem (Sigmoid vs. Tanh).
5. Added functionality to save and load model weights, allowing for persistence of trained models.
<br>
**Output:**<br>
Predicted XOR Output:<br>
Epoch: 0, Loss: 0.2978 
Epoch: 1000, Loss: 0.0010 
Epoch: 2000, Loss: 0.0005 
Epoch: 3000, Loss: 0.0003 
Epoch: 4000, Loss: 0.0002 
Epoch: 5000, Loss: 0.0002 
Epoch: 6000, Loss: 0.0002 
Epoch: 7000, Loss: 0.0001 
Epoch: 8000, Loss: 0.0001 
Epoch: 9000, Loss: 0.0001 
Predicted XOR output: 
[[0.99950743]
[0.99981859] 
[0.99981722] 
[0.99988554]]

**Predicting Trip Duration:<br>
Features Used:**<br>
The below are the features used:<br>
**1. Numerical Features**<br>
● passenger_count: The number of passengers in the taxi ride.<br>
● pickup_longitude: Longitude coordinate of the pickup location.<br>
● pickup_latitude: Latitude coordinate of the pickup location.<br>
● dropoff_longitude: Longitude coordinate of the drop-off location.<br>
● dropoff_latitude: Latitude coordinate of the drop-off location.<br>

**2. Categorical Features**<br>
● vendor_id: Categorical variable indicating the provider of the taxi service.<br>
● store_and_fwd_flag: Binary categorical variable indicating whether the trip record was held in
the vehicle memory before sending it to the vendor.<br>

**Transformations:**
**1. Date and Time Features:**<br>
● The original pickup_datetime column is converted to datetime format.<br>
● Additional temporal features are extracted:<br>
● pickup_hour: Hour of the day when the trip started.<br>
● pickup_day: Day of the month when the trip started.<br>
● pickup_month: Month when the trip started.<br>
● pickup_dayofweek: Day of the week when the trip started.<br>

**2. Distance Feature:**<br>
● The haversine_distance function is applied to calculate the great-circle distance between
pickup and drop-off locations. This feature represents the distance of the trip in kilometers.<br>

<img width="300" alt="image" src="https://github.com/user-attachments/assets/e134c685-b232-4af4-9b9b-3d83a7e7762f"><br>

<img width="300" alt="image" src="https://github.com/user-attachments/assets/562d21db-964e-49d6-abf9-9b1b070647d9"><br>

<img width="300" alt="image" src="https://github.com/user-attachments/assets/eece8580-a2fe-4368-8f59-a91bcb613dba"><br>

<img width="300" alt="image" src="https://github.com/user-attachments/assets/0cde5816-4eca-45db-aa5e-355942eccb6d"><br>

<img width="300" alt="image" src="https://github.com/user-attachments/assets/8ef55601-6d0e-4dd2-abf3-70cb0302db5c"><br>

<img width="300" alt="image" src="https://github.com/user-attachments/assets/90b9d4aa-9847-4655-80b1-ceec25cee2f8"><br>





