# Bearing Fault Diagnosis Project

## Overview
This project implements a comprehensive bearing fault diagnosis system using machine learning and deep learning techniques. It includes data processing, feature extraction, dimensionality reduction, and classification of different bearing fault types (Normal, Outer Race, Inner Race, and Roller Element faults).

## Project Structure
The project is organized into multiple Jupyter notebooks, each focusing on a different aspect of the fault diagnosis process:

### Data Files
- `Normal_Bearing.csv` - Data for normal bearing condition
- `outer_race_fault_test_2.csv` - Data for outer race faults (test set 2)
- `outer_race_fault_test_3.csv` - Data for outer race faults (test set 3)
- `inner_race_fault.csv` - Data for inner race faults
- `roller_element_fault.csv` - Data for roller element faults
- `set1_timefeatures.csv` - Time domain features from set 1
- Various `Time_feature_matrix_Bearing_*_Test_*.csv` files - Time domain features extracted from different bearings and test conditions

### Notebooks
1. **bearing feature extraction.ipynb**
   - Extracts time and frequency domain features from raw bearing vibration signals
   - Calculates statistical parameters (RMS, kurtosis, skewness, etc.)
   - Performs feature selection and importance analysis

2. **bearing dimensionality reduction.ipynb**
   - Implements Principal Component Analysis (PCA) with varying numbers of components (2-6)
   - Visualizes data in reduced dimensions (2D and 3D plots)
   - Evaluates explained variance by each principal component
   - Includes visualization of feature loadings and component relationships

3. **bearing classification and model training.ipynb**
   - Trains and evaluates multiple machine learning models:
     - Random Forest (RF)
     - Support Vector Machine (SVM)
     - 1D Convolutional Neural Network (1DCNN)
     - Long Short-Term Memory Network (LSTM)
   - Compares model performance using accuracy, precision, recall, and F1-score
   - Visualizes confusion matrices and performance metrics

4. **bearing fault detection.ipynb**
   - Implements fault detection algorithms
   - Provides methods to identify the presence of faults in bearing signals
   - Distinguishes between healthy and faulty bearing states

5. **bearing Prognosis.ipynb**
   - Focuses on remaining useful life (RUL) prediction
   - Implements prognostic algorithms to predict bearing failure
   - Provides health assessment indicators

## Key Features
- Multi-class bearing fault classification (Normal, Outer Race, Inner Race, Roller Element)
- Dimensionality reduction using PCA with 2-6 components
- Comparative analysis of machine learning and deep learning models
- Normalized confusion matrices for model evaluation
- Training vs. testing accuracy comparisons
- Feature importance analysis for extracted features
- Radar charts and heatmaps for model performance visualization

## How to Use This Project

### Prerequisites
- Python 3.x
- Libraries: pandas, numpy, matplotlib, scikit-learn, PyTorch, seaborn, scipy

### Getting Started
1. Clone this repository or download the project files
2. Install required dependencies using:
   ```
   pip install pandas numpy matplotlib scikit-learn torch seaborn scipy PyQt5
   ```
3. Start with `bearing feature extraction.ipynb` to understand the feature engineering process
4. Proceed to `bearing dimensionality reduction.ipynb` to see how PCA is applied
5. Explore the model training and evaluation in `bearing classification and model training.ipynb`

### Model Workflow
1. **Feature Extraction** → Extract time and frequency domain features from raw vibration signals
2. **Feature Selection** → Select the most relevant features for fault diagnosis
3. **Dimensionality Reduction** → Apply PCA to reduce feature dimensions
4. **Model Training** → Train multiple models on the reduced feature set
5. **Model Evaluation** → Compare performance using confusion matrices and metrics
6. **Fault Detection** → Implement algorithms to detect bearing faults
7. **Prognosis** → Predict remaining useful life and bearing health

## Results
The project implements and compares different machine learning and deep learning models for bearing fault classification:

- **Random Forest**: Provides excellent performance with interpretable feature importance
- **SVM**: Shows good generalization across fault classes
- **1D CNN**: Leverages deep learning to automatically extract features from the data
- **LSTM**: Captures temporal dependencies in the data sequence

Performance metrics for all models are visualized using:
- Normalized confusion matrices
- Bar plots comparing training and testing accuracy
- Heatmaps of performance metrics
- Radar charts of testing accuracy

## Future Work
- Implement more advanced deep learning architectures
- Add real-time fault diagnosis capabilities
- Integrate with IoT systems for online monitoring
- Explore transfer learning for adapting to new bearing types

## License
This project is provided for educational and research purposes.

## Acknowledgments
- Time domain features are extracted based on bearing vibration analysis techniques
- Machine learning models are implemented using scikit-learn and PyTorch frameworks
