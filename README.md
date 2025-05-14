Multivariate Analysis on Sleeping Posture Data
This project performs a comprehensive multivariate analysis on sleeping posture data using techniques from clustering, classification, dimensionality reduction, and regression. The dataset includes pressure sensor readings captured from different body postures on a mattress. This study explores how well postures can be classified and whether body mass index (BMI) can be predicted from pressure data.

📊 Project Structure
🔹 1. Data Preprocessing
Imported data from Pressure_Data.csv

Randomly sampled 400 observations for analysis

Transformed skewed pressure readings (V1–V144) using log1p()

🔹 2. Exploratory Data Analysis
Visualized density plots before and after log transformation

Grouped pressure data by sensor regions for better interpretability

🔹 3. Clustering Analysis
Hierarchical Clustering:

Performed using single, complete, average, and Ward linkage

Ward linkage showed best performance with Rand Index = 0.70

K-Means Clustering:

Optimal number of clusters found using Elbow Method (K = 3)

Agreement with ground truth labels: Rand Index = 0.68

Comparison:

Rand Index between Hierarchical (Ward) and K-Means: 0.88

🔹 4. Classification
Linear Discriminant Analysis (LDA):

Classified sleeping posture with a 7.25% misclassification rate

Quadratic Discriminant Analysis (QDA):

Not suitable due to high dimensionality and low sample size

🔹 5. Dimensionality Reduction (PCA)
PCA revealed that 34 principal components are needed to explain 90% of the variance

PC1 distinguishes between Left and Right postures; Supine is centered

🔹 6. Decision Boundary Visualization
Plotted LDA decision boundaries on PC1 vs PC2

🔹 7. Subject Classification
Used LDA and QDA on 34 PCA components to classify subjects

LDA misclassification rate: 49%

QDA misclassification rate: 59.75%

🔹 8. Principal Component Regression (PCR)
Target variable: Body Mass Index (BMI)

Full data: R² = 0.24

Supine-only data: R² = 0.53

Demonstrates posture-dependence of pressure patterns

📁 Files Included
Multivariate Analysis On Sleeping Posture Data.pdf: Detailed project report

Pressure_Data.csv (not included here): Pressure map data

Subject_info_data.csv (not included here): Height and weight info for BMI calculation

🔧 Tools & Libraries
R, ggplot2, dplyr, tidyr, MASS, pls, e1071, gridExtra
