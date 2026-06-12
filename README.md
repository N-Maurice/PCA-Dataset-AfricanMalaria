# Principal Component Analysis (PCA) on African Malaria Data

## Project Overview

This project implements Principal Component Analysis (PCA) from scratch using only NumPy and Matplotlib. The objective is to reduce the dimensionality of an African malaria dataset while preserving as much information (variance) as possible.

The implementation follows the mathematical foundations of PCA by computing:

* Data standardization
* Covariance matrix
* Eigenvalues and eigenvectors
* Explained variance
* Principal component selection
* Data projection onto lower dimensions

No machine learning libraries such as Scikit-Learn were used, as required by the assignment instructions.

---

## Dataset

The dataset used in this project contains malaria-related indicators across African countries, including:

* Malaria incidence
* Malaria cases reported
* Access to drinking water
* Access to sanitation services
* Rural population statistics
* Urban population statistics
* Malaria prevention indicators

The dataset contains:

* Numeric variables suitable for PCA
* Non-numeric variables (Country Name, Country Code, Geometry)
* Missing values (NaN), which were handled during preprocessing

Dataset Source:

https://www.kaggle.com/datasets/lydia70/malaria-in-africa?resource=download


---

## Objectives

The main objectives of this project are:

1. Implement PCA from scratch using NumPy.
2. Compute the covariance matrix manually.
3. Perform eigendecomposition.
4. Select principal components using explained variance.
5. Reduce dimensionality while preserving information.
6. Visualize data before and after PCA.
7. Evaluate information loss resulting from dimensionality reduction.

---

## Methodology

### 1. Data Cleaning

* Removed non-numeric columns.
* Identified missing values.
* Replaced missing values using column means.

### 2. Standardization

Each feature was standardized using:

z = (x - μ) / σ

where:

* x = original value
* μ = feature mean
* σ = feature standard deviation

### 3. Covariance Matrix

The covariance matrix was computed to identify relationships between variables.

### 4. Eigendecomposition

Eigenvalues and eigenvectors were calculated using NumPy's linear algebra functions.

### 5. Principal Component Selection

Principal components were ranked according to explained variance.

The number of components retained was selected based on cumulative explained variance to preserve most of the information while reducing complexity.

### 6. Data Projection

The standardized dataset was projected onto the selected principal components to create a reduced-dimensional representation.

---

## Results

The PCA model successfully reduced the number of dimensions while retaining most of the dataset's variance.

Key observations:

* Highly correlated variables were combined into fewer dimensions.
* Visualization became easier in reduced space.
* Most important malaria-related patterns were preserved.

---

## Information Lost During PCA

Although PCA preserves most of the variance, some information is inevitably lost.

Examples include:

* Country-specific characteristics
* Rare malaria patterns
* Small variations among health indicators
* Unique local environmental conditions

These lower-variance details are sacrificed in exchange for a simpler representation of the data.

---

## Technologies Used

* Python
* NumPy
* Matplotlib
* Google Colab

---

## Repository Structure

├── Template_PCA_Formative_1.ipynb
├── DatasetAfricaMalaria.csv
├── Contribution_Sheet.pdf
├── Combined_Submission.pdf
└── README.md

---

## Authors

Group Members:

* Member 1: Ketia INEZA GAKWAYA
* Member 2: Maurice NSHIMYUMUKIZA

---

## Assignment Requirements Met

✔ African-focused dataset

✔ Dataset contains missing values

✔ Dataset contains non-numeric columns

✔ PCA implemented from scratch

✔ Covariance matrix computed

✔ Eigenvalues and eigenvectors computed

✔ Dynamic principal component selection

✔ Visualization completed

✔ Performance benchmarking completed

✔ NumPy used for implementation

✔ Matplotlib used for visualization

✔ No Scikit-Learn used
