# Olympic Dataset Automation & Power BI Integration Guide

This guide explains how to:

- Configure the Kaggle API
- Download the Olympic dataset using Python
- Load Olympic datasets into Pandas DataFrames
- Connect Python datasets directly into Power BI

The workflow automates Olympic dataset collection and simplifies Power BI integration.

---

# ⚙️ Step 1: Setting Up Kaggle API & Python Environment

Before downloading the dataset, configure the Kaggle API and install the required Python libraries.

---

## 📌 Create a Kaggle Account

If you do not already have a Kaggle account:

1. Visit Kaggle
2. Create an account
3. Log in to your Kaggle profile

## 📌 Generate Kaggle API Token

1. Open your Kaggle account settings
2. Navigate to the **API** section
3. Click: `Create New API Token`

This downloads a file named: `kaggle.json`

which contains your Kaggle authentication credentials.


## 📌 Save the Kaggle API Token

Move the downloaded `kaggle.json` file into a secure local directory.

Example: `C:/Users/YourUsername/.kaggle`

## 📌 Install Required Python Libraries

Install the required libraries using:

```bash
pip install kaggle pandas
```

---

# 📥 Step 2: Download Olympic Dataset Using Python

The project uses a Python automation script to:

- Authenticate Kaggle access
- Download Olympic datasets
- Remove outdated files
- Extract CSV files
- Prepare datasets for Power BI

## 📂 Script Location

[Scripts/olympic_data_script.py](Scripts/olympic_data_script.py)

## 📌 Workflow Performed by the Script

### 🔐 Kaggle Authentication

The script authenticates Kaggle API access using: `KAGGLE_CONFIG_DIR`

which points to the folder containing the `kaggle.json` file.

---

### 📥 Dataset Download

The following Kaggle dataset is downloaded automatically: `piterfm/paris-2024-olympic-summer-games`

The script downloads and extracts all dataset files into the configured source directory.

---

### 🧹 Existing File Cleanup

Before downloading new datasets, the script removes old CSV files from the source folder to avoid:

- Duplicate files
- Dataset version mismatch
- Outdated data refreshes

---

### 📊 CSV Dataset Processing

The script processes Olympic datasets such as:

- athletes.csv
- medals.csv
- medallists.csv
- teams.csv
- events.csv
- medals_total.csv

and loads them into Pandas DataFrames for analytics workflows.

---

# 📚 Step 3: Loading Olympic Data into Power BI

After downloading the dataset, the data can be imported directly into Power BI using Python integration.

## 📂 Script Location


[Scripts/load_data_script.py](Scripts/load_data_script.py)


## 🔌 Connecting Power BI with Python

Follow these steps inside Power BI Desktop:

### 1️⃣ Open Power BI Desktop

Launch Power BI Desktop on your system.


### 2️⃣ Open Get Data

Navigate to: `Home → Get Data`


### 3️⃣ Select Python Script

Choose: `Python Script`

from the available data source options.


### 4️⃣ Run the Python Loading Script

Copy the contents of: `Scripts/load_data_script.py`

and paste it into the Power BI Python editor window.


### 5️⃣ Load DataFrames into Power BI

After executing the script:

- Power BI detects the Pandas DataFrames
- Select the required tables
- Click **Load**

The datasets are now available inside Power BI for transformation, modeling, and dashboard development.

---

# 🏗 Workflow Summary

```
Kaggle Dataset
        │
        ▼
Python Download Script
        │
        ▼
Olympic CSV Files
        │
        ▼
Pandas DataFrames
        │
        ▼
Power BI Python Integration
        │
        ▼
Data Modeling & Dashboard Development
```

---

# 📈 Benefits of This Workflow

This automated workflow provides:

✅ Faster dataset refreshes  
✅ Automated Olympic data ingestion  
✅ Reduced manual preprocessing effort  
✅ Scalable analytics engineering workflow  
✅ Cleaner Power BI integration process  
✅ Production-style ETL experience  


