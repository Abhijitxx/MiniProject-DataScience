
# MRI Hippocampus Segmentation (MRIHS) Dataset

This repository provides instructions to access and utilize the MRI Hippocampus Segmentation (MRIHS) dataset, which is available on Kaggle. The dataset is ideal for machine learning applications in medical imaging, particularly segmentation tasks.

---

## Dataset Overview

The MRIHS dataset includes MRI scans with hippocampal segmentation masks. This dataset is useful for researchers and practitioners in medical imaging, neuroscience, and machine learning.

### Key Features:
- High-resolution MRI scans
- Pre-labeled segmentation masks
- Suitable for training and evaluation of deep learning models in medical imaging

---

## Accessing the Dataset

Follow these steps to download the dataset:

### Prerequisites
1. Create a [Kaggle account](https://www.kaggle.com/).
2. Install the Kaggle Python API:
   ```bash
   pip install kaggle
   ```

3. Obtain your Kaggle API key:
   - Go to your [Kaggle API page](https://www.kaggle.com/account).
   - Click on **Create New API Token**.
   - Save the downloaded `kaggle.json` file.

4. Place the `kaggle.json` file in the `~/.kaggle/` directory or set the `KAGGLE_CONFIG_DIR` environment variable.

---

### Download Instructions

Run the following Python script to download the dataset:

```python
import os
from kaggle.api.kaggle_api_extended import KaggleApi

# Set Kaggle API key directory (if not using the default location)
os.environ["KAGGLE_CONFIG_DIR"] = "/path/to/your/kaggle.json"

# Authenticate and download the dataset
api = KaggleApi()
api.authenticate()

# Specify the dataset and target directory
dataset_name = "sabermalek/mrihs"
output_path = "datasets/mrihs"

# Download and unzip the dataset
api.dataset_download_files(dataset_name, path=output_path, unzip=True)

print("Dataset download complete!")
```

Alternatively, you can download the dataset manually by visiting [MRIHS Dataset on Kaggle](https://www.kaggle.com/datasets/sabermalek/mrihs) and following the on-screen instructions.

---

## Usage Guidelines

- Please review the dataset license on the [Kaggle page](https://www.kaggle.com/datasets/sabermalek/mrihs) before using the data.
- Cite the dataset appropriately in your research and publications.

---

## Acknowledgments

This dataset is provided by **Saber Malek**. We appreciate their contribution to the field of medical imaging.

--- 

Feel free to customize this README further to suit your project.
