readme_content = """
# Banana Ripeness Classifier with fastai 🍌

This repository contains a Jupyter Notebook that implements an image classifier to predict the ripeness stage of bananas (unripe, ripe, rotten) using the fastai library.

## How to Run the Notebook

This notebook is designed to be run interactively in **Google Colaboratory (Colab)**. Colab provides a free, cloud-based Jupyter environment with access to GPUs, which is ideal for deep learning tasks.

### 1. Open in Google Colab

You can open this notebook directly in Google Colab by clicking the "Open in Colab" badge (if available, or you can upload the `.ipynb` file directly).

### 2. Execute Cells Sequentially

Once the notebook is open in Colab, simply run all the cells sequentially from top to bottom. The notebook is structured as follows:

*   **Setup and Imports**: Essential libraries are imported, and basic paths are set up.
*   **Dataset Cloning**: The notebook automatically clones the required dataset from the GitHub repository `https://github.com/IvaJorgusheska/Banana_Ripeness_Level_Recognition.git`. You do not need to manually download or clone the dataset.
*   **Dataset Preparation**: The dataset is split into training, validation, and a held-out test set.
*   **DataLoaders**: fastai `DataLoaders` are created with appropriate image transformations and augmentations.
*   **Model Training**: A ResNet-18 model is trained using transfer learning with fastai's `fine_tune` method.
*   **Evaluation**: The model's performance is evaluated on both the validation set and the unseen test set, including confusion matrices and top loss visualizations.

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

The notebook uses the `fastai` library, which comes pre-installed in Google Colab. No additional `pip install` commands are typically needed for basic fastai usage in Colab.

"""

with open('README.md', 'w') as f:
    f.write(readme_content)

print("README.md file created successfully in the current directory.")
