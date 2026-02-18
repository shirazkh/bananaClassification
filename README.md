# Banana Ripeness Classifier: fastai & PyTorch CNNs 🍌

This repository contains Jupyter Notebooks implementing image classifiers to predict the ripeness stage of bananas (unripe, ripe, rotten).
It covers two main exercises:
1. **Exercise 1:** Rapid prototyping using the `fastai` library and transfer learning (ResNet-18).
2. **Exercise 4:** Building and training custom Convolutional Neural Networks (CNNs) from scratch using `PyTorch`.

## How to Run the Notebooks

This notebook is designed to be run interactively in **Google Colaboratory (Colab)**. Colab provides a free, cloud-based Jupyter environment with access to GPUs.

### 1. Open in Google Colab

You can open the notebooks directly in Google Colab by clicking the "Open in Colab" badge (if available, or you can upload the `.ipynb` files directly).

### 2. Execute Cells Sequentially

Once the notebook is open in Colab, simply run all the cells sequentially from top to bottom. The notebook is structured as follows:

* **Setup and Imports**: Essential libraries are imported, and basic paths are set up.
* **Dataset Cloning**: The notebook automatically clones the required dataset from the GitHub repository `https://github.com/IvaJorgusheska/Banana_Ripeness_Level_Recognition.git`. You do not need to manually download or clone the dataset.
* **Dataset Preparation**: 
    * In Exercise 1: The dataset is split into training (80%) and a held-out test set (20%).
    * In Exercise 4: The dataset is split into training (64%), validation (16%), and test set (20%).
* **DataLoaders**: Appropriate DataLoaders are created with image transformations and augmentations.
* **Model Training**: 
    * In Exercise 1: A ResNet-18 model is trained using transfer learning with fastai's `fine_tune` method.
    * In Exercise 4: Custom PyTorch architectures (`SmallCNN`, `DeepCNN`, `DeepCNN_BN`, `DeepCNN_BN_DO`) are trained using custom training loops.
* **Evaluation**: The models' performance is evaluated on the validation/test sets, including confusion matrices, accuracy tracking, and loss visualizations.

### 3. Review Results

The notebook outputs include training progress, loss plots, confusion matrices, and sample test predictions, allowing you to review the model's performance and understand its strengths and weaknesses.

## Project Structure

After running the notebook, you will find the following directory structure created (under the main `banana_ripeness` directory):

```text
banana_ripeness/
    train/          # Training images (80% of original dataset)
        unripe/
        ripe/
        rotten/
    test/           # Held-out test images (20% of original dataset)
        unripe/
        ripe/
        rotten/
```

## Dependencies

The notebooks use the `fastai` and `PyTorch` libraries, which come pre-installed in Google Colab. No additional pip install commands are typically needed for basic usage in Colab.
