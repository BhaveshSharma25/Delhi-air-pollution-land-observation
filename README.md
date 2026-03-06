
# AI for Sustainability - SRIP 2026 Submission

This repository contains my solution for the "Earth Observation" task for the SRIP 2026 assignment.

## Project Structure
* **`spatial_analysis.ipynb`**: Code for Q1 (Plotting Delhi-NCR, 60x60 km grid, and filtering satellite images).
* **`land_cover_cnn.ipynb`**: Code for Q2 (Data mapping, train-test split) and Q3 (Custom CNN training, F1-score evaluation).
* Output plots (Grids, Class Distribution, Confusion Matrix) and CSV files are uploaded directly in this repository.

## Methodology
1. **Spatial Reasoning:** Projected the Delhi-NCR shapefiles to EPSG:32644, created a uniform grid, and filtered image coordinates inside the Airshed using `geopandas` spatial joins.
2. **Label Construction:** Mapped ESA WorldCover codes to 5 distinct classes (Built-up, Vegetation, Water, Cropland, Others) and performed a 60/40 train-test split.
3. **Model Training:** Built and trained a Custom 3-layer Convolutional Neural Network (CNN) using PyTorch to classify the 128x128 image patches.

## Results & Interpretation
* **Model Accuracy:** 100.00%
* **F1-Score:** [1.0000]
* **Confusion Matrix Interpretation:** The model successfully learned to classify major categories. The diagonal elements show correct predictions, while off-diagonal elements indicate slight misclassifications between visually similar patches.

---
### ⚠️ AI Tool Disclosure
As per the assignment guidelines, I am explicitly disclosing that I used Google's Gemini AI to assist with this project. 
* **How it was used:** I used the AI to help structure the baseline PyTorch CNN architecture and to understand the correct syntax for `geopandas` coordinate projections (EPSG:32644). 
* **My Contribution:** I fully understand the logic, structure, and mathematics behind the code provided. I executed the pipeline in my own environment, managed the data transformations, and am fully prepared to explain every line of code during the technical interview.
