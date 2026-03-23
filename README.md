Image Classification: Airplanes, Cars, and Ships
This project implements a Convolutional Neural Network (CNN) using PyTorch to classify images into three categories: Airplanes, Cars, and Ships
. The model was trained on a custom dataset and achieved a high level of accuracy during testing

📊 Dataset Overview
The dataset used for this project consists of 3,582 images
Classes: airplane, car, and ship
Pre-processing: All images are resized to 224x224 pixels and normalized using standard Mean and Standard Deviation values for RGB channels

🏗️ Model Architecture
The model is a custom NeuralNet class built with the following layers
Convolutional Layer 1: 3 input channels, 12 output channels, kernel size 5
Max Pooling: 2x2 kernel with a stride of 2
Convolutional Layer 2: 12 input channels, 24 output channels, kernel size 5
Fully Connected Layer 1: Input size of 24 * 53 * 53, outputting to 120 nodes
Fully Connected Layer 2: 120 input nodes, 84 output nodes
Output Layer: 84 input nodes, 10 output nodes (supporting the classification of the 3 target classes)
Activation Functions: ReLU is used throughout the hidden layers

🚀 Training & Performance
The model was trained for 10 epochs using the following hyperparameters
Loss Function: CrossEntropyLoss
Optimizer: Stochastic Gradient Descent (SGD) with a learning rate of 0.001 and momentum of 0.9
Batch Size: 32
Results:
Final Training Loss: 0.1564
Test Accuracy: 95.60%

💻 Installation & Usage
To run this project, you will need the following Python libraries installed
pip install numpy pillow torch torchvision matplotlib
Running the Classifier
The trained model weights are saved as trained_net.pth
You can use the load_image function provided in the notebook to preprocess new images for prediction
The model will output predictions corresponding to the defined class names: airplane, car, or ship
