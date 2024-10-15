
# Symptom Parser and Dictionary Program

## Overview

This project processes patient symptom data from a CSV file. It includes two main components:

1. **Parser (Step 1)** – Loads and parses the dataset for further processing.
2. **Dictionary Creation and Enhancement (Step 2)** – Uses the parsed data to create a dictionary of symptoms, tracks missing data, and updates the dictionary with any new symptoms found.

## Project Structure

```
.
├── dataset.csv          # Input dataset containing patient symptoms
├── parser.ipynb         # Jupyter notebook for the parser (Step 1)
├── symptom_parser.py    # Python script for Step 2 (Dictionary creation and enhancement)
├── README.md            # This readme file
```

### Dataset (dataset.csv)

The dataset includes the following columns:

- `SrNo` – Serial number of the record.
- `Patient_Id` – Unique identifier for each patient.
- `DOB` – Date of birth of the patient.
- `Fever`, `Cough`, `Cold` – Symptoms with values indicating severity (e.g., Low, Mid, High).
- `Other Symptoms` – Free-text field for additional symptoms.

### Step 1: Parser (parser.ipynb)

This Jupyter notebook reads and prepares the dataset for further analysis:

- Loads the dataset using `pandas`.
- Cleans the data by handling missing values.
- Verifies the structure and prepares it for use in Step 2.

**Usage:**  
Run `parser.ipynb` in a Jupyter notebook environment to parse and clean the dataset.

### Step 2: Dictionary Creation and Enhancement (symptom_parser.py)

This script processes the parsed dataset and performs the following tasks:

1. **Load the Dataset** – Reads the CSV file into memory.
2. **Create a Symptom Dictionary** – Builds a dictionary for each patient with their symptoms.
3. **Track Missing Data** – Identifies and reports any missing symptoms.
4. **Enhance the Dictionary** – Updates the dictionary with new symptoms if they are found in the dataset.

**Key Components:**

- **Expected Symptoms**: A list of symptoms expected in the dataset (e.g., Fever, Cough, Cold, Other Symptoms).
- **Symptom Dictionary**: A data structure that stores patient symptom information.
- **Missing Data Tracker**: A mechanism that tracks any missing symptom data for patients.

### Requirements

- Python 3.x
- Pandas (for dataset manipulation)

To install the required dependencies:

```bash
pip install pandas
```

### Usage

1. Ensure you have the dataset (`dataset.csv`) in the same directory as the scripts.
2. Run `symptom_parser.py` to create and enhance the symptom dictionary.
3. The program will output the dictionary and any missing data, then update the dictionary with new data if found.

### Contribution

Contributions are welcome! Feel free to open issues or submit pull requests to improve the project.

### License

This project is licensed under the MIT License.

---

This README provides a high-level explanation without including code. Let me know if you'd like any further adjustments!
