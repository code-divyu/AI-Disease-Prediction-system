# AI Disease Prediction System

![Java](https://img.shields.io/badge/Java-100%25-blue)
![License](https://img.shields.io/badge/License-MIT-green)

An AI-powered disease prediction system that implements predictive diagnosis models for multiple diseases using data munging, feature selection, model training, and accuracy calculation. This project validates and improves existing methods in the disease diagnosis pipeline.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Project Structure](#project-structure)
- [Diseases Covered](#diseases-covered)
- [Methodology](#methodology)
- [Technologies Used](#technologies-used)
- [Installation & Setup](#installation--setup)
- [Usage](#usage)
- [Datasets](#datasets)
- [Results](#results)
- [Contributors](#contributors)
- [License](#license)

---

## Overview

This project implements an AI-based predictive diagnosis system focusing on improving key aspects of the disease prediction pipeline:

1. **Data Munging** - Replacing missing values using k-nearest neighbors (KNN) instead of mean substitution to reduce bias
2. **Feature Selection** - Using simulated annealing algorithm with adaptive p-value thresholds
3. **Model Training** - Training predictive models on medical datasets
4. **Accuracy Evaluation** - Comprehensive cross-validation and accuracy calculation

---

## Features

- Multi-disease prediction support (Breast Cancer, Heart Disease, Diabetes)
- KNN-based data imputation for handling missing values
- Simulated annealing for optimized feature selection
- Adaptive p-value significance thresholds
- Data augmentation techniques (noise addition, scaling)
- Cross-validation support
- MySQL database integration
- Comprehensive result visualization with graphs

---

## Project Structure

```
AI-Disease-Prediction-system/
├── BreastCancer/                 # Breast cancer dataset files
├── BreastCancerPrediction/       # Breast cancer prediction module (Maven)
├── Diabetes/                     # Diabetes dataset files
├── HeartDiseaseData/             # Heart disease dataset files
├── HeartDiseasePrediction/       # Heart disease prediction module (Maven)
├── Presentation/                 # Project presentation files
├── Project Report/               # Detailed project report
├── Results - Graphs/             # Result visualizations and graphs
├── commons-math3-*.jar           # Apache Commons Math library
├── mysql-connector-java-*.jar    # MySQL JDBC driver
├── build.xml                     # Ant build configuration
├── manifest.mf                   # JAR manifest file
└── README.md                     # Project documentation
```

---

## Diseases Covered

| Disease | Dataset Source | Prediction Module |
|---------|---------------|------------------|
| Breast Cancer | Wisconsin Breast Cancer Dataset | `BreastCancerPrediction.java` |
| Heart Disease | Cleveland & Hungarian Heart Disease Datasets | `HeartDiseasePrediction.java` |
| Diabetes | Pima Indians Diabetes Dataset | `Diabetes/` folder |

---

## Methodology

### Data Munging Improvements
- Replaced mean imputation with **k-nearest neighbors (KNN)** method
- Reduced bias introduced by majority-class substitution

### Feature Selection
- Implemented **simulated annealing algorithm** for optimal feature selection
- Adaptive p-value thresholds within configurable upper and lower bounds
- Configurable initial temperature and cooling rate parameters

### Model Evaluation
- 90/10 train-test split method
- Cross-validation results provided throughout the report
- Accuracy comparison across different feature sets

### Data Augmentation
- Noise addition techniques
- Data scaling methods
- Improved dataset diversity

---

## Technologies Used

- **Programming Language:** Java
- **Build Tools:** Maven, Apache Ant
- **Database:** MySQL
- **Libraries:**
  - Apache Commons Math 3.x
  - MySQL Connector/J 8.0
- **IDE:** NetBeans
- **Version Control:** Git & GitHub

---

## Installation & Setup

### Prerequisites

- Java Development Kit (JDK) 8 or higher
- MySQL Server (local installation)
- Maven (for prediction modules)
- Apache Ant (for main project)
- NetBeans IDE (recommended)

### Steps

1. **Clone the repository:**
   ```bash
   git clone https://github.com/code-divyu/AI-Disease-Prediction-system.git
   cd AI-Disease-Prediction-system
   ```

2. **Configure MySQL Database:**
   - Open `DBConnection.java` in both `BreastCancerPrediction/` and `HeartDiseasePrediction/` folders
   - Update the MySQL username and password:
     ```java
     String username = "root";  // Change to your MySQL username
     String password = "";      // Change to your MySQL password
     ```

3. **Build the project:**
   - For Maven modules:
     ```bash
     cd BreastCancerPrediction
     mvn clean install
     ```
   - For the main project:
     ```bash
     ant build
     ```

---

## Usage

### Running the Prediction Modules

1. **Breast Cancer Prediction:**
   ```bash
   cd BreastCancerPrediction
   java -cp target/classes com.mycompany.breastcancer.BreastCancerPrediction
   ```

2. **Heart Disease Prediction:**
   ```bash
   cd HeartDiseasePrediction
   java -cp target/classes com.mycompany.heartdisease.HeartDiseasePrediction
   ```

### Note
The main functions in each program do not execute all functionalities in sequence by default. Uncomment specific function calls to run individual modules as needed.

---

## Datasets

### Breast Cancer Dataset
- **Source:** UCI Machine Learning Repository - Wisconsin Breast Cancer Dataset
- **Location:** `BreastCancer/` folder
- **Files:** `breast-cancer-wisconsin.data`, `wdcb.data`, `Index`

### Heart Disease Dataset
- **Source:** UCI Machine Learning Repository - Heart Disease Datasets
- **Location:** `HeartDiseaseData/` folder
- **Files:** `processed.cleveland.data`, `hungarian.data`, `heart-disease.names`

### Diabetes Dataset
- **Source:** UCI Machine Learning Repository - Pima Indians Diabetes Dataset
- **Location:** `Diabetes/` folder

---

## Results

Result visualizations and graphs are available in the `Results - Graphs/` folder. The project report contains detailed accuracy metrics, cross-validation results, and comparative analysis of different methods.

---

## Contributors

- **Divyanshu** ([@code-divyu](https://github.com/code-divyu))

---

## License

This project is open-source and available under the MIT License.

---

> **Note:** This project is intended for educational and research purposes. It should not be used as a substitute for professional medical diagnosis.
