# Benchmark-Dataset-and-Deep-Learning-Method-for-Global-Tropical-Cyclone-Forecasting

This repository introduces the contents of our research work, which consists of **two main parts**:

1. A benchmark dataset for global tropical cyclone (TC) research – **TropiCycloneNet Dataset**
2. A deep learning-based method for predicting TC track and intensity – **TropiCycloneNet Method**

Both parts are released to foster open research and encourage reproducible results in the field of tropical cyclone forecasting.

---

## 🌪️ TropiCycloneNet-Dataset

![Dataset Image](https://github.com/user-attachments/assets/792867ad-5ea4-49c8-beb9-267276de7aec)

### 🔍 Overview

The **TropiCycloneNet Dataset** (`TCN_D`) is a comprehensive dataset designed for studying tropical cyclones worldwide. It spans from 1950 to 2023 and includes:

- `Data_1d`: Tabular records of cyclone center location, pressure, wind speed, etc.
- `Data_3d`: Gridded meteorological fields (e.g., geopotential height, wind components, SST) around the cyclone center.
- `Env-Data`: Structured environmental features that support deep learning applications.

It enables the analysis and modeling of both spatial and temporal cyclone behavior and provides a foundation for building data-driven forecasting systems.

### 📥 Download

We offer two download options:

- **[Full Dataset (1950–2023, ~25.7GB)](https://drive.google.com/file/d/1BUAab0OYyiArbraQHu2oMoj_jF-nNUxT/view?usp=sharing)**
- **[Test Subset (2017–2023, ~3.34GB)](https://drive.google.com/file/d/1Xx2rzH6ztSGLTUR9EZkfDz5mQHsvhHsi/view?usp=sharing)**

### 📊 Visualization

We provide easy-to-use scripts for loading and visualizing each part of the dataset (`read_TCND.py`). You can generate visualizations of `Data_1d`, `Data_3d`, and `Env-Data` with a single command.

Example:

```bash
python read_TCND.py dataset_path Haiyan 2001101418 WP train
```
This will produce three images showing the meteorological and environmental context of Typhoon Haiyan at a specific timestamp.
📎 Features

    Resolution: 0.25°, every 6 hours

    Ocean Regions: WP, EP, ATL, NI, SI, SP

    Pressure levels: 200, 500, 850, 925 hPa

    Additional features: SST, movement velocity, intensity change, subtropical high data

📘 Documentation

See full documentation and usage guide in the GitHub repository:

👉 [TropiCycloneNet-Dataset](https://drive.google.com/file/d/1BUAab0OYyiArbraQHu2oMoj_jF-nNUxT/view?usp=sharing)

🧠 [TropiCycloneNet-Model](https://drive.google.com/file/d/1BUAab0OYyiArbraQHu2oMoj_jF-nNUxT/view?usp=sharing)

Model Image
🔧 Introduction

TropiCycloneNet (TCN_M) is our proposed deep learning model for predicting TC track and intensity using multi-modal data (e.g., satellite images, environmental features, 1D/3D meteorological data).

This repository contains:

    Preprocessed subset of the TCN_D dataset

    Test code for inference and visualization

    Forecast results rendered on Himawari-8 satellite imagery

    🔍 Red circles: Ground truth tracks
    🌟 Green stars: Our model’s best prediction
    🟩 Green area: Multiple trajectory predictions by our model
    🟥 Red area: MMSTN’s prediction range

Prediction Sample
⚙️ Requirements

    Python 3.8.5

    PyTorch 1.11.0+

    OpenCV, NumPy, Matplotlib

Training code and model weights will be released soon.
📘 Repository

👉 TropiCycloneNet GitHub
