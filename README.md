📘 Feature Extraction from Anime Dataset

A Data Cleaning & Feature Engineering Project using Python

📌 Overview

This project focuses on extracting meaningful features from an anime dataset, specifically the episode count, which was embedded within the title text. Using Python and Pandas, I transformed messy text data into clean, structured numeric values that can support analysis, visualization, and machine learning workflows.

The core work was developed in the Jupyter Notebook:
FeatureExtraction.ipynb

📂 Project Workflow
1. Importing Required Libraries

The notebook begins by importing essential data analysis libraries:

import numpy as np
import pandas as pd

2. Loading the Dataset

The anime dataset is loaded from a CSV file:

df = pd.read_csv("anime.csv")

3. Data Exploration

Viewing the first few rows (df.head())

Accessing rows and specific fields using loc

Understanding the structure of titles containing episode counts, e.g.:

Naruto (220 eps)
Demon Slayer (26 eps)

4. Feature Extraction (Episode Count)

The project includes:

A custom function for reading episode numbers

String cleaning using .str.replace(" eps", "")

A robust regex approach to extract digits reliably:

df['Episodes'] = df['Episodes'].str.extract(r'(\d+)').astype(int)


This converts text like:

"(220 eps)" → 220
"(64 eps)" → 64

5. Final Output

A clean dataset with a new numeric column:

Episodes
---------
220
64
25
...

This structured feature enables:

->Ranking anime by episode count

->Visual analytics

->Preparation for ML-driven recommendation systems

->Statistical analysis

🧠 Key Concepts Demonstrated

.Data Cleaning

.String Manipulation

.Regular Expressions (Regex)

.Feature Engineering

.Pandas DataFrame Operations

🛠 Technologies Used

.Python

.Pandas

.NumPy

.Jupyter Notebook

📁 Files Included

FeatureExtraction.ipynb — Main notebook containing all code

anime.csv — Input dataset (not included unless added manually)

🚀 How to Run This Project

Clone the repo:

git clone https://github.com/your-username/your-repo-name.git


Install dependencies:

pip install pandas numpy


Open Jupyter Notebook:

jupyter notebook


Run:

FeatureExtraction.ipynb

📈 Future Enhancements

Visualizing episode distribution

Adding genre-based insights

Building a recommendation engine

Deploying a dashboard using Streamlit or Dash

🙌 Acknowledgments

This project highlights the importance of feature engineering in building quality datasets for analytics and machine learning.
Feel free to fork, improve, and contribute!
