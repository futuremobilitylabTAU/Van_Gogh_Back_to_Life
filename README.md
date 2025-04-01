# Part 1: CNN Network Training & Evaluation – AlexNet & VGG19

<table>
  <tr>
    <th align="center">No Van Gogh!</th>
    <th align="center">Yes Van Gogh!</th>
  </tr>
  <tr>
    <td align="center">
      <img src="https://github.com/futuremobilitylabTAU/Van_Gogh_Back_to_Life/blob/main/Classi/no_example.jpg" height="300"/>
    </td>
    <td align="center">
      <img src="https://github.com/futuremobilitylabTAU/Van_Gogh_Back_to_Life/blob/main/Classi/yes_example.jpg" height="300"/>
    </td>
  </tr>
</table>

This repository contains code, data, and results for training and evaluating convolutional neural networks (CNNs), specifically **AlexNet** and **VGG19**, on a dataset.

The goal is to compare model performance and evaluate their ability to **classify whether a given painting is by Van Gogh or not**.


---

## File Overview

### `Traning_Hyper.ipynb`
Performs hyperparameter tuning for CNN models, including grid or random search over:
- Learning rate
- Batch size
- Weight decay

Results are logged and visualized to help select optimal parameters.

---

### `Traning_Models_V3.ipynb`
Main training script that uses selected hyperparameters to train both AlexNet and VGG19.

Includes:
- Model definition  
- Training and validation loops  
- Performance logging  
- Saving models and results

---

### `DATA_AND_MODELS.ipynb`
Responsible for:
- Data loading and preprocessing  
- Dataset organization  
- Initial model setup

Serves as a **class module** used by other notebooks.

---

## Output Directories

### `Alex_RESULTS`
Contains outputs and logs from training **AlexNet**, such as:
- Accuracy/loss plots  
- Confusion matrices  
- Saved weights/checkpoints

### `VGG_RESULTS`
Same as above, but for **VGG19** training sessions.

---

## Best Hyperparameters Logs

### `best_params_history_AlexNet.json`
A list of trials for different **AlexNet** hyperparameter configurations, including:
- Loss values  
- Corresponding parameter sets (e.g., learning rate, weight decay, batch size)  

The JSON is updated **only if** the new configuration shows improved results.

### `best_params_history_VGG19.json`
Analogous to the AlexNet file, this documents **VGG19** hyperparameter search results.


---

# Part 2:  Style Transfer

<table>
  <tr>
    <th align="center">Before </th>
    <th align="center">After (Van Gogh Style)</th>
  </tr>
  <tr>
    <td align="center">
      <img src="https://github.com/futuremobilitylabTAU/Van_Gogh_Back_to_Life/blob/main/Content/18.jpg?raw=true" height="300"/>
    </td>
    <td align="center">
      <img src="https://github.com/futuremobilitylabTAU/Van_Gogh_Back_to_Life/blob/main/VGG19/18.jpg?raw=true" height="300"/>
    </td>
  </tr>
</table>

### `Style_Transfer_V2.ipynb`
Implements neural style transfer using PyTorch. Includes loading content/style images, computing losses, and optimizing the generated image using gradients.

### `Style_Transfer_Evaluation.ipynb`
Compares different Style Transfer results. Includes side-by-side visualizations and optional metric-based evaluation.

---

## Getting Started

1. Clone the repository.
2. Install dependencies from environment.yml.

Open Anaconda Prompt and run:

```
conda env create -f environment.yml
conda activate cnn-style-transfer-env
```

Now you can use JupiterLab for runing the filies!


3. Run `DATA_AND_MODELS.ipynb` to load and preprocess data.
4. Use `Traning_Hyper.ipynb` to search for optimal hyperparameters.
5. Use `Traning_Models_V3.ipynb` to train models.
6. Run the style transfer notebooks with your own images to generate styled outputs.
