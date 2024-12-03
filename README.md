# team2_project4
Project 4: Advanced Machine Learning
All columns were used as features, no categorical data in dataset

## Auto Optimization
Trial 60 Complete [00h 00m 04s]
val_accuracy: 0.6266666650772095

Best val_accuracy So Far: 0.8133333325386047
Total elapsed time: 00h 03m 21s

### Best Model Hyperparameters
{'activation': 'tanh',
 'first_units': 9,
 'num_layers': 3,
 'units_0': 5,
 'units_1': 3,
 'units_2': 5,
 'units_3': 1,
 'units_4': 1,
 'units_5': 3,
 'tuner/epochs': 20,
 'tuner/initial_epoch': 7,
 'tuner/bracket': 1,
 'tuner/round': 1,
 'tuner/trial_id': '0020'}

 ### Results on Test Dataset
Loss: 0.5096867084503174, Accuracy: 0.8133333325386047


## Manual Optimization
### 1st Attempt
L1: U = 9, activation = tanh
L2: U = 36, A = tanh
L3: U = 1, A = tanh
params = 514
Loss: 0.788856029510498, Accurac: 0.746666669845581

### 2nd Attempt
L1: U = 50, activation = relu
L2: U = 100, A = relu
L3: U = 1, A = sigmoid
params = 5851
Loss: 0.531, Accurac: 0.853

### 3rd Attempt
L1: U = 50, activation = LeakyReLU
L2: U = 100, A = relu
L3: U = 1, A = sigmoid
params = 5851
Loss: 0.463, Accurac: 0.853

### 4th Attempt
L1: U = 50, activation = LeakyReLU
L2: U = 100, A = relu
L3: U = 100, A = relu
L4: U = 1, A = sigmoid
params = 15,951
Loss: 1.069, Accurac: 0.813

### 5th Attempt
L1: U = 9, activation = LeakyReLU
L2: U = 36, A = relu
L3: U = 1, A = sigmoid
params = 514
Loss: 0.479, Accurac: 0.800

### 6th Attempt
L1: U = 9, activation = tanh
L2: U = 36, A = relu
L3: U = 1, A = sigmoid
params = 514
Loss: 0.473, Accurac: 0.747