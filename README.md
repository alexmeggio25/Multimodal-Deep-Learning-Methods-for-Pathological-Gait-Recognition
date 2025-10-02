# Pathological Gait Recognition

This repository addresses the task of **pathological gait recognition** using deep learning techniques, leveraging both unimodal and hybrid approaches.

## Overview
The project includes:
- Data preprocessing  
- Model training with **Leave-One-Subject-Out Cross-Validation (LOSO-CV)**  
- A basic **web application** for inference  

Experiments were conducted on **Google Colab** with a **Tesla T4 GPU (Free Tier)**.  
The dataset is stored as a `.zip` file on Google Drive.  
A utility archive (`Utils.zip`) must be manually uploaded via the Colab interface after initializing the virtual environment.

## Repository Structure
- **Utils.zip**  
  Contains reusable functions and constants for data processing and model training.  

- **Preprocessing.ipynb**  
  Demonstrates each step of the preprocessing pipeline with visual outputs.  
  Corresponding functions are also implemented in `Utils/Preprocessing.py`.  

- **LOSO_CV.ipynb**  
  Main notebook for training and evaluating deep learning models using **LOSO-CV**.  
  The best-performing model is trained and saved along with its weights.  
  ⚠️ Due to GitHub file size limits, outputs have been removed — see `Final_Report.pdf` for results.  

- **my_app.py**  
  Prototype **Streamlit web application** for local inference.  
  Users can upload a `.csv` file, and the app predicts the gait label and displays class probabilities.  
  Relies on utility functions from the `Utils` folder and is designed to run locally (e.g., in VS Code).  

- **Report.pdf**  
  Detailed report describing methodology, experiments, and results.  

## Requirements
- Python 3.8+  
- TensorFlow 2.18.0  
- Keras 3.8.0  
- Streamlit  
- NumPy  
- Pandas  
- Scikit-learn  
- Google Colab (optional, for GPU acceleration)  
