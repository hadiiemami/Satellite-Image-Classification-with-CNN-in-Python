# Satellite Image Classification with CNN in Python

![Python Logo](https://www.python.org/static/community_logos/python-logo-master-v3-TM.png)  
![Satellite Image Classification](https://raw.githubusercontent.com/eostools/eostools.github.io/master/images/satellite_image_classification.jpg)

A Jupyter Notebook implementing Convolutional Neural Network (CNN) classification for satellite imagery, specifically using Sentinel-2 data. This project focuses on land cover classification, leveraging Python libraries for geospatial data processing and machine learning.

## Overview
This repository contains a Jupyter Notebook (`Classification.ipynb`) that demonstrates the classification of Sentinel-2 satellite images using a CNN model. The code processes multispectral imagery and ground truth data for tasks like land cover mapping, suitable for applications in remote sensing, environmental monitoring, and geospatial analysis.

## Table of Contents
- [Features](#features)
- [Tutorials](#tutorials)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Data](#data)
- [Contributing](#contributing)
- [License](#license)

## Features
- Loads and preprocesses Sentinel-2 imagery using `rasterio` and `pyrsgis`.
- Applies data standardization and PCA for dimensionality reduction.
- Implements a CNN model for multi-class land cover classification.
- Visualizes results with `matplotlib` for model evaluation.
- Optimized for Google Colab with Google Drive integration for data storage.

## Tutorials
The repository includes the following Jupyter Notebook:
- **Classification.ipynb**: Covers the end-to-end process of satellite image classification:
  - Loading Sentinel-2 imagery (`Sistan_Sentinel.tif`) and ground truth data (`Sistan_Sentinel_Training.tif`).
  - Preprocessing with standardization (`StandardScaler`) and PCA (`sklearn.decomposition.PCA`).
  - Building and training a CNN model for land cover classification.
  - Visualizing results with `matplotlib`.

## Prerequisites
- **Python**: Version 3.8 or higher.
- **Jupyter Notebook**: For running `.ipynb` files.
- **Required Python Packages**:
  - `rasterio` for geospatial data handling.
  - `pyrsgis` for satellite image processing.
  - `numpy` for numerical operations.
  - `matplotlib` for visualization.
  - `scikit-learn` for preprocessing and PCA.
  - `gdal` for geospatial data support.
- Google Colab environment (optional, for running with Google Drive integration).
- Google Drive account for accessing input files (`Sistan_Sentinel.tif`, `Sistan_Sentinel_Training.tif`).

## Installation
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/satellite-cnn-classification.git
   ```

2. **Install Dependencies**:
   - Install required packages using `requirements.txt`:
     ```bash
     pip install -r requirements.txt
     ```
   - Alternatively, install packages manually:
     ```bash
     pip install rasterio pyrsgis numpy matplotlib scikit-learn gdal
     ```

3. **Set Up Google Colab (Optional)**:
   - If using Google Colab, mount your Google Drive:
     ```python
     from google.colab import drive
     drive.mount('/content/drive')
     ```
   - Ensure input files (`Sistan_Sentinel.tif`, `Sistan_Sentinel_Training.tif`) are in your Google Drive.

## Usage
1. Navigate to the repository folder:
   ```bash
   cd satellite-cnn-classification
   ```
2. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
3. Open `Classification.ipynb` and follow the cells to:
   - Load Sentinel-2 imagery and ground truth data.
   - Preprocess data (standardization, PCA).
   - Train the CNN model.
   - Visualize classification results.

## Data
- **Input Files**:
  - `Sistan_Sentinel.tif`: Multispectral Sentinel-2 image with 10 bands (866x770 pixels).
  - `Sistan_Sentinel_Training.tif`: Ground truth data for training (1 band, 866x770 pixels).
- **Source**: Data should be stored in Google Drive or locally, as specified in the notebook.
- **Note**: Replace file paths in the notebook with your own data paths if not using Google Drive.

## Example
To classify land cover types in Sentinel-2 imagery:
- Open `Classification.ipynb` in Jupyter or Google Colab.
- Load `Sistan_Sentinel.tif` and `Sistan_Sentinel_Training.tif`.
- Run preprocessing steps (e.g., `StandardScaler`, `PCA`).
- Train the CNN model and visualize results with `matplotlib`.

## Notes
- Ensure input TIFF files are correctly formatted and accessible.
- Adjust CNN hyperparameters (e.g., layers, epochs) in the notebook for better performance.
- For large datasets, consider using a GPU in Google Colab for faster training.
- Check the [Copernicus Open Access Hub](https://scihub.copernicus.eu/) for additional Sentinel-2 data.

## Contributing
Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Add or improve notebooks with clear comments and examples.
4. Submit a pull request with a description of changes.

## License
MIT License