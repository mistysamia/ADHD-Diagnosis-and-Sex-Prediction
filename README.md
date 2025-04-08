
# Brain activity pattern differences in ADHD
## Project Overview

This project aims to develop a model to predict ADHD diagnosis and sex in children and adolescents using functional brain imaging data and socio-demographic information. Special attention is given to ensuring that the model avoids gender bias, as girls are often underdiagnosed with ADHD. The model should also be explainable, using methods like SHAP or LIME, to meet GDPR requirements. The data includes four datasets: `Metadata_A`, `Metadata_B`, `Func`, and `label`.

## Dataset
Download the dataset from the provided source. It contains four datasets:
- `Metadata_A`: Socio-demographic and emotional data
- `Metadata_B`: Parenting information
- `Func`: fMRI data
- `Label`: ADHD diagnosis and sex labels

## Python Version and Third-Party Libraries

### Python Version:
    Python Version: 3.11.11
### Third-Party Libraries:
1. NumPy: 1.26.4
2. Pandas: 2.2.2
3. scikit-learn: 1.6.1
4. Seaborn: 0.13.2
5. Kneed: 0.8.5
6. SciPy: 1.13.1
7. Plotly: 5.24.1
8. Matplotlib: 3.10.0
9. Tensorflow: 2.15.0

## Running the Code

Follow the steps below to run the code in the correct order:

### **Install Python and Third-Party Libraries**
Before running the code, ensure that **Python 3.11.11** is installed. If necessary, update to this version.

Install the required libraries by running the following command in your terminal:

```bash
pip install numpy==1.26.4 pandas==2.2.2 scikit-learn==1.4.2 seaborn==0.13.2 kneed==0.8.5 scipy==1.13.0 plotly==5.24.1 matplotlib==3.8.4 tensorflow==2.15.0
```

## Setup Instructions
1. Ensure Python version **3.11.11** is installed.
2. Install the required libraries.

### Data Exploraion and Preprocessing 
1. Load the notebook ``sm23788_Data_Exploration.ipynb``.
2. Download the dataset and place it in the specified directory.
   - Ensure the dataset files (e.g., `Metadata_A`, `Metadata_B`, `Func`, `Label`) are located in the correct directory.
3. **Update the paths**:
      - **`data_path`**: This is the path where you load the dataset. Update the notebook with the correct file path where the raw data is stored.
      - **`preprocessed_data_path`**: This is the path where the preprocessed (cleaned) data will be saved after processing. Update the notebook with the correct file path where the preprocessed data should be stored (e.g., `preprocessed_dataset.csv`).
4. Run ``sm23788_Data_Exploration.ipynb`` and start the analysis.
5. After running the setup, the clean (preprocessed) dataset will be generated and saved in the specified `preprocessed_data_path`. The following files will be saved:
   - `X_train.csv`: Training features
   - `X_test.csv`: Testing features
   - `y_train.csv`: Training labels
   - `y_test.csv`: Testing labels

### Modelling and testing :
1. Load the notebook ``sm23788_Modelling_Result.ipynb``.
2. **Update the path**:
      - **`data_path`**: This is the path where you saved preprocessed dataset. Update the notebook with the correct file path where the raw data is stored.
3. Run ``sm23788_Modelling_Result.ipynb`` and start the analysis.
