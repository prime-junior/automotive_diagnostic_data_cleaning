# Automotive Diagnostic Data Cleaning

![Python](https://img.shields.io/badge/python-v3.8+-blue.svg) ![Jupyter](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=flat&logo=jupyter&logoColor=white) ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=flat&logo=pandas&logoColor=white) ![Status](https://img.shields.io/badge/status-completed-brightgreen.svg) ![License](https://img.shields.io/badge/license-MIT-green.svg)

## Project Description

This project implements a sophisticated dual-strategy data cleaning pipeline for automotive diagnostic data collected through different form systems (Google Forms and Zoho CRM). The system processes pre-screening test results for automotive ECU (Electronic Control Unit) diagnostics, transforming unstructured diagnostic notes into structured, analyzable datasets.

The project solves the complex challenge of processing diagnostic data from two distinct form systems with different structural characteristics:

- **Zoho CRM Forms**: Maintain consistent field structure over time, processed via regex-based extraction
- **Google Forms**: Have undergone multiple field updates, requiring dual-method approach (Excel merge + regex extraction)

The pipeline extracts and standardizes critical diagnostic fields including Original Problems, Original DTCs, FS1 ECU Problems, FS1 ECU DTCs, Problems Related status, Additional Notes, and Resolution from unstructured text data.

## Installation and Execution

### Prerequisites
- Python 3.8 or higher
- Jupyter Notebook or JupyterLab

### Required Dependencies
```bash
pip install pandas
pip install missingno
pip install openpyxl
pip install jupyter
```

### Installation Steps

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd automotive_diagnostic_data_cleaning
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

### Execution Instructions

**Step 1: Process Zoho CRM Data**
```bash
jupyter notebook notebooks/zoho_form_data_cleaning.ipynb
```
- Execute all cells sequentially
- Output: `data_cleaned/df_zoho_form_cleaned.csv`

**Step 2: Process Google Forms Data**
```bash
jupyter notebook notebooks/google_form_data_cleaning.ipynb
```
- Execute all cells sequentially
- Output: `data_cleaned/df_prescreen_cleaned.csv` (final consolidated dataset)

## Author
Developed by [Weverson Barbieri de Oliveira](https://github.com/weversonbarbieri)

## License
MIT