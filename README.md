# Upaj : AI-Powered Crop Yield Prediction and Optimization (iPOF)

This repository contains the source code and documentation for the "AI-Powered Crop Yield Prediction and Optimization Framework" (iPOF), a project designed to address critical challenges in Indian agriculture through advanced machine learning.

## 📝 Project Overview

The iPOF is an end-to-end system designed to provide accurate, location-specific crop yield predictions and actionable optimization recommendations for farmers in India. It leverages a state-of-the-art hybrid spatiotemporal deep learning model (CNN-LSTM) to analyze multi-modal data from satellite imagery, weather records, and soil databases.

### Key Features

-   **High-Accuracy Prediction**: Utilizes a CNN-LSTM architecture to model complex spatial and temporal patterns for reliable yield forecasting.
-   **Multi-Modal Data Fusion**: Integrates data from Sentinel-2, NASA POWER, and ISRIC SoilGrids for a holistic view of the agroecosystem.
-   **Explainable AI (XAI)**: Incorporates a SHAP-based module to provide transparent, human-readable explanations for its predictions, building user trust.
-   **Scenario Analysis for Optimization**: Allows users to simulate the impact of different farming inputs (e.g., changes in irrigation or fertilizer) to make data-driven decisions that balance productivity and sustainability.

## 🎯 Business Problem

Conventional agricultural practices in India are increasingly unsustainable due to climate change, resource depletion, and systemic inefficiencies. This leads to yield volatility and financial distress for millions of smallholder farmers. The iPOF aims to disrupt this cycle by providing an accessible, data-driven decision support tool to enhance profitability and environmental sustainability.

## 🛠️ Technology Stack

-   **Programming Language**: Python 3.9+
-   **Core Libraries**:
    -   **Data Handling**: Pandas, NumPy, GeoPandas, Rasterio, Xarray
    -   **Deep Learning**: TensorFlow / PyTorch
    -   **ML & Evaluation**: Scikit-learn
    -   **Explainability**: SHAP
-   **Data Sources**: Google Earth Engine, NASA POWER API, ISRIC SoilGrids
-   **Prototyping**: Jupyter Notebooks
-   **Deployment (Conceptual)**: Flask/Django, Docker

## 🚀 Setup and Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/d-s007/Upaj.git
    cd Upaj
    ```

2.  **Create a virtual environment:**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Install the project as a package:**
    This allows for clean, absolute imports from the `src` directory.
    ```bash
    pip install -e .
    ```

## 🏃‍♀️ How to Run the Pipelines

The project is orchestrated through main pipeline scripts.

1.  **Run the full training pipeline:**
    This will execute all steps from data ingestion to model training and evaluation.
    ```bash
    python src/pipelines/training_pipeline.py
    ```

2.  **Run the prediction pipeline:**
    This will load a pre-trained model and make a prediction on new data.
    ```bash
    python src/pipelines/prediction_pipeline.py
    ```

This structured approach ensures reproducibility, maintainability, and scalability, reflecting MLOps best practices.