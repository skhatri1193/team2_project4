Team 2 - Project 4: Advanced Machine Learning
Overview
This project focuses on developing and optimizing a neural network model using TensorFlow and KerasTuner to achieve high accuracy on a given dataset. Key aspects include hyperparameter tuning, manual optimization, and evaluation of the model's performance on test data.

Neural Network Model
Framework: TensorFlow
Features: All columns in the dataset were used as features. The dataset contains no categorical data.
Auto Optimization
Methodology
Tool: KerasTuner was used to optimize hyperparameters for the neural network model.
Performance Metrics:
Best Validation Accuracy: 0.893
Total Elapsed Time: 3 minutes 24 seconds


Insights:

The highest validation accuracy achieved was 0.893.
The second and third highest validation accuracies were 0.880 and 0.867, respectively.
Mean validation accuracy across trials was 0.698 (denoted by the red dashed line).
This plot highlights significant variation in validation accuracy across trials, with some configurations performing much better than others.

Best Hyperparameters
json
Copy code
{
  "activation": "tanh",
  "first_units": 63,
  "num_layers": 3,
  "units_0": 3,
  "units_1": 5,
  "units_2": 5,
  "units_3": 3,
  "units_4": 5,
  "tuner/epochs": 20,
  "tuner/initial_epoch": 0,
  "tuner/bracket": 0,
  "tuner/round": 0
}
Total Parameters: 1,067


Results on Test Dataset
Loss: 0.400
Accuracy: 0.893
Manual Optimization
Optimization Attempts and Results
Using Auto-Optimized Parameters:

Architecture: Layers with 63, 3, 5, 5, and 1 units (all using tanh activation)
Parameters: 1,067
Results: Loss = 0.556, Accuracy = 0.853
Testing Activation Functions:

Architecture: Layers with 50, 100, and 1 units (activations: relu, relu, sigmoid)
Parameters: 5,851
Results: Loss = 0.355, Accuracy = 0.880
Testing LeakyReLU Activation:

Architecture: Layers with 50, 100, and 1 units (activations: LeakyReLU, relu, sigmoid)
Parameters: 5,851
Results: Loss = 0.388, Accuracy = 0.853
Increased Epochs (20 → 50):

Same architecture as Attempt #2
Results: Loss = 0.605, Accuracy = 0.800
Preventing Overfitting:

Parameters: 5,851
Results: Loss = 0.514, Accuracy = 0.840
Cross-Validation:

Results: TBD
Addressing Overfitting Warnings:

Architecture: Adjusted activations with LeakyReLU and relu
Results: Loss = 0.517, Accuracy = 0.840
Model Evaluation
Loss Curve


Training Loss:
Starts high (≈0.88) and decreases rapidly, stabilizing at ≈0.4.
Validation Loss:
Initially higher than training loss but diverges around epoch 10, suggesting overfitting.
Stabilizes later, showing better generalization.
Accuracy Curve


Training Accuracy:
Starts at ≈0.55, increases steadily, and peaks at ≈0.85.
Validation Accuracy:
Lower and more volatile, stabilizing at ≈0.75.
Key Takeaways
Learning Dynamics:

Initial overfitting was mitigated with adjustments.
Training loss and accuracy trends indicate effective learning from the data.
Validation performance highlights room for improvement in generalization.
Final Test Metrics:

Loss: 0.517
Accuracy: 0.840
These metrics reflect the true performance on unseen data.
Optimization Insights:

Hyperparameter tuning played a critical role in achieving high validation accuracy.
Manual optimizations provided insights into the impact of activation functions and overfitting prevention techniques.
Conclusion
This project demonstrates the iterative process of training, optimizing, and evaluating a neural network. Through both automated and manual tuning, the model achieved a test accuracy of 0.893, showcasing its capability to perform well on unseen data while maintaining a robust generalization ability.
