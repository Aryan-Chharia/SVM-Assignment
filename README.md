# SVM Hyperparameter Optimization on Wine Quality Dataset

**Author:** Aryan Chharia  
**Email:** achharia_be22@thapar.edu  
**Roll No.:** 102203313

---

## Project Overview

This project optimizes a Support Vector Machine (SVM) classifier for the Wine Quality dataset using the Optuna library. The goal is to maximize classification accuracy by tuning SVM hyperparameters across 10 different train-test splits, ensuring robustness. The dataset is sourced from the UCI Machine Learning Repository, and the quality scores (3–8) are treated as discrete classes.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Dependencies](#dependencies)
- [How to Run](#how-to-run)
- [Outputs](#outputs)
- [Results](#results)
- [Approach](#approach)

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/your-repo.git
   ```
2. Navigate to the project directory:
   ```sh
   cd your-repo
   ```
3. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
   *(Or manually install as listed below)*

## Usage

Provide examples of how to run or use your project:

```sh
python main.py
```
or, if using a notebook:
```sh
jupyter notebook svm.ipynb
```

## Features

- **Hyperparameter Tuning**: Optimizes `kernel`, `C`, `gamma`, `degree`, and `coef0` using Optuna with 100 trials per split.
- **Multiple Splits**: Evaluates performance over 10 train-test splits for reliability.
- **Visualizations**: Includes a convergence plot for the best sample and a bar chart of accuracies across splits.
- **Results Storage**: Saves results to a CSV file and plots as PNG images.

## Dependencies

- Python 3.8+
- `pandas`
- `numpy`
- `scikit-learn`
- `optuna`
- `matplotlib`

Install them using:
```sh
pip install pandas numpy scikit-learn optuna matplotlib
```

## How to Run

Clone the Repository:
```sh
git clone <repository-url>
cd <repository-directory>
```

Run the Script:
```sh
python svm_optimization.py
```
Replace `svm_optimization.py` with the actual script filename if different.

## Outputs

- `svm_optimization_results.csv`: Table of results for each split.
- `convergence_plot.png`: Convergence graph for the best sample.
- `accuracy_bar_plot.png`: Bar chart of best accuracies.

## Results

The script outputs a table with the sample ID, best accuracy (%), and best hyperparameters for each of the 10 splits.
Visualizations provide insights into the optimization process and performance consistency.
Example output files are generated after running the script.

## Approach

- **Data**: Loads the Wine Quality dataset (red wine) from UCI.
- **Preprocessing**: Standardizes features using StandardScaler.
- **Optimization**: Uses Optuna to tune SVM parameters over 10 splits.
- **Evaluation**: Maximizes accuracy via SVC’s score method.
