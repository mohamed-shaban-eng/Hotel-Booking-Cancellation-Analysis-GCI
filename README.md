# 🏨 Hotel Booking Cancellation Analysis & Prediction

## 📌 Project Overview

This project focuses on analyzing hotel booking data to understand customer cancellation behavior and identify potential business opportunities to reduce booking cancellations.

Using Data Science, Exploratory Data Analysis (EDA), Statistical Analysis, and Machine Learning, the project investigates the factors associated with hotel booking cancellations and evaluates a business proposal aimed at improving reservation management.

The main objective is to turn historical booking data into meaningful business insights and measurable recommendations.

## 🎯 Business Problem

Hotel booking cancellations can negatively affect hotel revenue, room availability, and reservation planning.

The main business questions addressed in this project are:

- What is the hotel booking cancellation rate?
- Which factors are associated with booking cancellations?
- Does the time between booking and arrival (Lead Time) affect cancellation behavior?
- Can Machine Learning help predict booking cancellations?
- Can a business strategy based on reducing the advance booking window potentially improve reservation performance?

## 📊 Dataset

The project uses the **Hotel Booking Demand Dataset**.

- **Records:** 119,390 bookings
- **Features:** 32 columns
- **Location:** Portugal
- **Period:** 2015–2017
- **Hotels:** City Hotels in Lisbon and Resort Hotels in Algarve

The dataset includes information about:

- Hotel type
- Booking dates and lead time
- Customer information
- Room types
- Deposit types
- Average Daily Rate (ADR)
- Previous cancellations
- Reservation status

**Dataset Source:**  
[Kaggle – Hotel Booking Demand Dataset](https://www.kaggle.com/datasets/mathsian/hotel-bookings)

## 🛠️ Tools & Technologies

The following technologies and libraries were used:

- **Python** – Main programming language
- **Pandas** – Data manipulation and analysis
- **NumPy** – Numerical operations
- **Matplotlib** – Data visualization
- **Seaborn** – Statistical visualization
- **SciPy** – Statistical hypothesis testing
- **Scikit-learn** – Data splitting and model evaluation
- **LightGBM** – Machine Learning classification model
- **Jupyter Notebook** – Development environment

## 🔍 Project Workflow

### 1. Data Collection & Understanding
- Loaded the hotel booking dataset.
- Explored the dataset structure and dimensions.
- Inspected data types and statistical summaries.
- Identified missing values.

### 2. Exploratory Data Analysis (EDA)
- Analyzed numerical and categorical variables.
- Investigated booking cancellation distributions.
- Explored customer types, deposit types, and hotel categories.
- Examined the relationship between Lead Time and cancellation rates.
- Visualized important business patterns using charts.

### 3. Statistical Analysis
- Performed Correlation Analysis.
- Used Pearson Correlation to investigate relationships between monthly ADR and cancellation rates.
- Applied Independent T-tests to compare selected monthly averages.
- Investigated the relationship between Lead Time and cancellation behavior.

### 4. Machine Learning Model
Developed a binary classification model using **LightGBM** to predict whether a hotel reservation would be canceled.

- **Target Variable:** `is_canceled`
- **Training Set:** 80%
- **Testing Set:** 20%
- **Evaluation Metric:** ROC-AUC
- **Threshold Optimization:** ROC Curve and Youden's J statistic
- **Feature Importance:** Identified influential prediction features.

### 5. Business Proposal
Based on the analysis, Lead Time was identified as an important factor associated with booking cancellations.

A business proposal was developed:

Reduce the available advance booking window to approximately 70% of its original duration for selected booking periods between October and March.

### 6. Business Proposal Simulation
Applied the proposed Lead Time adjustment to a copy of the dataset and used the trained model to compare predicted cancellations before and after the proposed change.

The objective was to estimate the potential business impact of the proposed strategy.

## 📈 Key Findings & Results

### Dataset Insights
- Analyzed 119,390 hotel reservations.
- Identified missing values across four columns.
- Observed an overall cancellation rate of approximately 37%.
- Found differences in Lead Time distributions across booking groups.

### Statistical Insights
- Monthly ADR and cancellation rates showed a positive correlation of **0.720**.
- Lead Time showed a statistically significant difference in the monthly averages compared in the notebook.
- Lead Time was selected as a key variable for the business proposal.

### Machine Learning Results

| Metric | Result |
|---|---:|
| Model | LightGBM |
| ROC-AUC | 0.9219 |
| Optimal Threshold | 0.3529 |
| Training Split | 80% |
| Testing Split | 20% |

### Business Simulation Results

The model's predictions showed the following changes:

| Metric | Before | After |
|---|---:|---:|
| Predicted Cancellations | 9,575 | 9,364 |

**Difference: 211 fewer predicted cancellations** in the evaluated test subset.

These results represent a simulated scenario based on modified historical data, not a verified real-world business outcome.

## ⚠️ Limitations & Future Improvements

- Improve the data preprocessing and missing-value treatment.
- Apply more comprehensive feature engineering.
- Explore additional factors influencing booking cancellations.
- Improve statistical testing and model validation procedures.
- Investigate the possible impact of reducing advance booking availability on new reservations.
- Use real-world experiments to validate the proposed business strategy.
- Develop a more comprehensive and realistic revenue impact estimation.

The market analysis section uses supplementary Japanese hotel-market references, while the booking dataset represents hotels in Portugal. This geographic difference should be considered when interpreting market-level conclusions.

## 📂 Project Structure

```text
Hotel-Booking-Analysis/
│
├── Hotel_bookings.ipynb
│
├── README.md
│
├── requirements.txt
|
|__ Hotel Bookings Reducing Cancellations Presentation.pdf
|
└── images/
    ├── cancellation_distribution.png
    ├── lead_time_analysis.png
    ├── correlation_heatmap.png
    └── feature_importance.png
```

## ⚙️ How to Run the Project

### 1. Clone the Repository

```bash
git clone YOUR_REPOSITORY_URL
```

### 2. Navigate to the Project Directory

```bash
cd Hotel-Booking-Analysis
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

### 5. Run the Notebook

Open `Hotel_bookings.ipynb` and execute the cells sequentially.

**Note:** The notebook downloads the dataset from an external source, so an internet connection is required.

## 👨‍💻 Author

**Mohamed Shaban**

Data Science | Python | Machine Learning | Data Analysis

Feel free to explore the notebook and share your feedback!