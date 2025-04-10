# Part 1: CNN Network Training & Evaluation – AlexNet & VGG19

<table>
  <tr>
    <th align="center">No Van Gogh! (on AlexNet & VGG19)</th>
    <th align="center">Yes Van Gogh! (on AlexNet & VGG19)</th>
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

### `Traning_Hyper.ipynb`
Performs hyperparameter tuning for CNN models, including grid or random search over:
- Learning rate
- Batch size
- Weight decay

Results are logged and visualized to help select optimal parameters.

<span style="color:red; font-weight:bold">You can view the results directly within the notebook.</span>


---

### `Traning_Models_V3.ipynb`
Main training script that uses selected hyperparameters to train both AlexNet and VGG19.

Includes:
- Model definition  
- Training and validation loops  
- Performance logging  
- Saving models and results

<span style="color:red; font-weight:bold">You can view the results directly within the notebook.</span>

---

### `DATA_AND_MODELS.ipynb`
Responsible for:
- Data loading and preprocessing  
- Dataset organization  
- Initial model setup

Serves as a **class module** used by other notebooks.

---

## Output Directories

### `Alex_DATA`
Contains outputs and logs from training **AlexNet**, such as:
- Accuracy/loss plots  
- Confusion matrices  
- Saved weights/checkpoints

### `VGG_DATA`
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

You can download the best-performing models for each architecture below:

- **Best AlexNet model**:  
  [Download from SharePoint](https://tauex-my.sharepoint.com/:u:/g/personal/dadashev_tauex_tau_ac_il/EQ1jWbEhdKBPtR0gtbIrBQMBPOIz9LXHd8Ow2vZJdaj1MA?e=GuKEr8)

- **Best VGG19 model**:  
  [Download from SharePoint](https://tauex-my.sharepoint.com/:u:/g/personal/dadashev_tauex_tau_ac_il/EXrXLIu4_BpIt4V5UUEm1dIB44rYrqA6Aa2EHfVi1N-lpQ?e=wRK9G7)


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

<span style="color:red; font-weight:bold">
Due to file size limitations, the output cannot be displayed directly on GitHub.  
To view the results, please download the notebook to your local machine and open it there.
</span>


### `Style_Transfer_Evaluation.ipynb`
Compares different Style Transfer results. Includes side-by-side visualizations and optional metric-based evaluation.

<span style="color:red; font-weight:bold">You can view the results directly within the notebook.</span>

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


## Authors

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/gabidadashev">
        <img src="https://github.com/gabidadashev.png" width="100px;" alt="Gabriel Dadashev"/><br />
        <sub><b>Gabriel Dadashev</b></sub>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/nivdanieli">
        <img src="https://github.com/nivdanieli.png" width="100px;" alt="Niv Danieli"/><br />
        <sub><b>Niv Danieli</b></sub>
      </a>
    </td>
  </tr>
</table>
