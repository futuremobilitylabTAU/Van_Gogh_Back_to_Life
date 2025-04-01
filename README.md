Part 1: Neural Network Training & Evaluation – AlexNet & VGG19 

This repository contains code, data, and results for training and evaluating convolutional neural networks (CNNs), specifically AlexNet and VGG19, on a custom dataset. 

The goal is to compare performance under different hyperparameter configurations and training setups.

File Overview: 

Traning_Hyper.ipynb

Performs hyperparameter tuning for CNN models, including grid or random search over learning rate, batch size, and weight decay. Results are logged and visualized to help select optimal parameters.

Traning_Models_V3.ipynb

Main training script that uses selected hyperparameters to train both AlexNet and VGG19. Includes:

A. Model definition
B. Training and validation loops
C. Performance logging
D. Saving models and results

DATA_AND_MODELS.ipynb

Responsible for data loading and preprocessing, dataset organization, and initial model setup. 
Serves as a Class for other notebooks.

Alex_REUSULTS
Contains txt outputs and logs from training AlexNet, such as accuracy/loss plots, confusion matrices, and saved weights/checkpoints.
VGG_REUSULTS
Same as above, but for VGG19 training sessions.

Best Hyperparameters Logs

best_params_history_AlexNet.json
A list of trials for different AlexNet hyperparameter configurations, including the loss and the corresponding parameter sets (e.g., learning rate, weight decay, batch size). The json updated only is some check make the results better.

best_params_history_VGG19.json
Analogous to the AlexNet file, this documents hyperparameter search results for VGG19.
