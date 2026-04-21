# Star, Galaxy & Quasar Classifier

A machine learning project that classifies astronomical objects from the [Sloan Digital Sky Survey (SDSS)](https://www.kaggle.com/datasets/fedesoriano/stellar-classification-dataset-sdss17) dataset into three categories: stars, galaxies, and quasars (QSOs).

## Overview

The SDSS is one of the most comprehensive astronomical surveys ever conducted. This project uses photometric and spectroscopic measurements from 100,000 observed objects to train a Random Forest classifier that can distinguish between stars, galaxies, and quasars with ~98% accuracy.

The project sits at the intersection of astrophysics and machine learning — the features used (brightness filters and redshift) are physically meaningful, and the model's confusion patterns reflect real observational challenges in astronomy.

## Dataset

- **Source:** Sloan Digital Sky Survey DR17
- **Size:** 100,000 objects
- **Classes:** GALAXY (59,445), STAR (21,594), QSO (18,961)
- **Features used:** u, g, r, i, z (brightness across 5 wavelength filters) and redshift

## Results

| Class | Precision | Recall | F1-Score |
|--------|-----------|--------|----------|
| GALAXY | 0.98 | 0.99 | 0.98 |
| QSO | 0.96 | 0.92 | 0.94 |
| STAR | 1.00 | 1.00 | 1.00 |
| **Overall** | | | **0.978** |

Stars are classified with near-perfect accuracy due to their distinct spectral signatures. The main source of error is QSOs being misclassified as galaxies — a challenging distinction even for professional astronomers, since quasars are essentially the extremely luminous cores of distant galaxies.

## Tech Stack

- Python
- pandas, matplotlib, seaborn
- scikit-learn (RandomForestClassifier)

## Project Structure

```
sdss-star-classifier/
├── sdss_classifier.ipynb   # Main notebook
├── star_classification.csv # Dataset
└── README.md
```

## How to Run

1. Clone the repo
2. Install dependencies:
   ```
   pip install pandas matplotlib scikit-learn seaborn
   ```
3. Open `sdss_classifier.ipynb` in VS Code or Jupyter and run all cells
