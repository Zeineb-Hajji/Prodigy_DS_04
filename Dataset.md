# Sentiment140 Dataset

This project uses the [Sentiment140 dataset](https://www.kaggle.com/datasets/kazanova/sentiment140), available on Kaggle. The dataset consists of 1.6 million tweets, each labeled for sentiment (positive, neutral, or negative).

## How to Use the Dataset:

1. **Download the Dataset from Kaggle:**
   - You can access the dataset by visiting the following [Kaggle link](https://www.kaggle.com/datasets/kazanova/sentiment140).
   - Download the CSV file (`training.1600000.processed.noemoticon.csv`) from the Kaggle page.

2. **Set Up Kaggle API (Optional):**
   If you prefer to download the dataset programmatically, follow these steps:
   - Install the Kaggle library using the following command:
     ```bash
     pip install kaggle
     ```
   - Set up the Kaggle API by downloading your credentials (a `kaggle.json` file) from your Kaggle account [here](https://www.kaggle.com/account).
   - Place the `kaggle.json` file in your local environment or in the appropriate directory on Google Colab.
   - Use the following Python code to download the dataset directly:
     ```python
     import os
     os.environ['KAGGLE_CONFIG_DIR'] = "/path_to_your_credentials/"

     # Download the dataset
     !kaggle datasets download -d kazanova/sentiment140 -p /content/
     ```

3. **Extract the Data:**
   - After downloading, extract the dataset file if needed (usually it is in a CSV format).
   - Use this file in your analysis by pointing to the path where you downloaded or extracted the dataset.

## Using the Dataset in This Repository:

Once you have the dataset, place the CSV file inside the `/Data` folder in this repository. Then, use the following code in the notebook or script to load the data:

```python
import pandas as pd

# Load the dataset from the /Data directory
df = pd.read_csv("Data/sentiment140.csv", encoding='ISO-8859-1')
