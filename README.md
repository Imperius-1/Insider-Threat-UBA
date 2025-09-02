# Insider-Threat-UBA
Contains all the files of this project
# Bridging Behavioural Analytics and Compliance: Evaluating Insider Threat Detection under ISO 27001 and NIST 800-53 Frameworks

## 1. Project Overview

This project implements a User Behavioural Analytics (UBA) framework to detect insider threats within a simulated corporate environment. The primary goal is to evaluate the effectiveness of machine learning-based anomaly detection and to formally bridge the gap between these technical findings and an organisation's strategic compliance requirements. The project uses the CERT Insider Threat Dataset to engineer behavioural features, trains unsupervised machine learning models (Isolation Forest and One-Class SVM), and provides a comparative analysis with a traditional rule-based system implemented in Splunk. A key deliverable is an Audit Matrix that maps the project's outputs to controls within the ISO 27001 and NIST 800-53 frameworks.

## 2. Features

- **Data-Driven Threat Detection**: Implements a UBA framework to detect subtle anomalies in user behaviour.
- **Model-Based Analysis**: Utilises Isolation Forest and One-Class SVM for unsupervised anomaly detection.
- **Comparative Study**: Provides a benchmark by comparing the ML model's findings against rule-based alerts in a Splunk environment.
- **Compliance Mapping**: Creates a formal Audit Matrix to align technical detections with ISO 27001 and NIST 800-53 controls.
- **Reproducible Methodology**: The entire project is documented in a series of Jupyter Notebooks, ensuring the analysis is transparent and reproducible.

## 3. Getting Started

### Prerequisites

- Python 3.8+
- Jupyter Notebook
- Access to the CERT Insider Threat Dataset (logon.csv, file.csv, email.csv, device.csv, psychometric.csv)
- Splunk Enterprise (optional, for the comparative analysis)

### Installation

1.  **Clone the repository (if applicable)**:
    ```bash
    git clone [repository_url]
    cd [repository_name]
    ```

2.  **Create a Virtual Environment (Recommended)**:
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On macOS/Linux
    .\venv\Scripts\activate   # On Windows
    ```

3.  **Install Dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

## 4. Project Structure

The project follows a modular structure to keep the workflow organised(google drive project structure):
###### insider-threat-uba/
###### │
###### ├── data/ # Raw input data (CERT Insider Threat v6.2)
###### │ ├── logon.csv
###### │ ├── file.csv
###### │ ├── device.csv
###### │ └── email.csv
###### │
###### ├── notebooks/ # Jupyter notebooks for step-by-step workflow
###### │ ├── 1_Data_Preparation.ipynb
###### │ ├── 2_Feature_Engineering.ipynb
###### │ └── 3_Anomaly_Detection.ipynb
###### │
###### ├── outputs/ # Processed datasets & results
###### │ ├── merged_sessions.csv
###### │ └── uba_features.csv
###### │
###### ├── requirements.txt # Python dependencies
###### └──  README.md # Project documentation
#

## 5. How to Run the Project

The project is designed to be run in a step-by-step manner using the Jupyter Notebooks located in the `notebooks/` directory.

1. Download the log files(.csv files) from the link given in the document 
2.   **Phase 1: Data Preparation**: Run the `1_Data_Preparation.ipynb` notebook to clean, merge, and prepare the raw data.
3.  **Feature Engineering with Sample Outputs** contains how the features are taken before merging to uba_features.csv
4.  **Phase 2: Feature Engineering**: Run the `2_Feature_Engineering.ipynb` notebook to create the behavioural features. This notebook will output `uba_features.csv`.
5.  **Phase 3: Anomaly Detection**: Run the `3_Anomaly_Detection Modelling.ipynb` notebook to train the machine learning models, evaluate their performance, and generate the final visualisations for your report.

## 6.Notes to keep in mind
1. **Data Directory** have 2 log files and links to other log files 
2. **Output Directory** has the Splunk Reports I downloaded as a part of this project and images 
3. Read the README files if present in a directory, so it will give u an idea what it is about
 
## 7. Acknowledgements

This project was made possible by the publicly available **CERT Insider Threat Dataset** and the use of open-source libraries such as `scikit-learn` and `pandas`.
