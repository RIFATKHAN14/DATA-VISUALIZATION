# Transaction Data Analysis

This repository contains the code for analyzing transaction data from a CSV file. The data includes information such as withdrawal and deposit amounts, categories, and balances. The goal of this analysis is to clean the dataset, perform exploratory data analysis (EDA), and visualize key insights.

## Dataset

The dataset (`MyTransaction.csv`) consists of the following columns:

- **Date**: The date of the transaction.
- **Category**: The category of the transaction (e.g., Rent, Misc, Food).
- **RefNo**: A reference number for the transaction (removed during data cleaning).
- **Withdrawal**: The amount withdrawn during the transaction.
- **Deposit**: The amount deposited during the transaction.
- **Balance**: The account balance after the transaction.

### Data Cleaning Steps

1. **Handling Missing Values**: Dropped rows with null values.
2. **Duplicate Columns**: Removed the duplicated column `Date.1` (which mirrored `Date`) and `RefNo` as it was not required for the analysis.
3. **Date Conversion**: Converted the `Date` column to a `datetime` object for easier manipulation and extracted `year`, `month`, and `day`.
4. **Duplicates**: Dropped any duplicate rows.
5. **Year Filter**: Removed the transaction for the year 2024 as it had very few observations.

## Exploratory Data Analysis (EDA)

The analysis included the following:

### 1. **Distribution of Categories**
   - Visualized the frequency of transactions per category using a bar chart.

### 2. **Average Monthly Withdrawal**
   - Calculated and plotted the average monthly withdrawal amounts.

### 3. **Average Monthly Withdrawal and Deposit**
   - Compared the average withdrawal and deposit amounts per month.

### 4. **Descriptive Statistics**
   - Provided summary statistics (`count`, `mean`, `min`, `max`, etc.) for `withdrawal`, `deposit`, and `balance`.

### 5. **Visualizations**
   - **Kernel Density Estimate (KDE)** plots for withdrawal, deposit, and balance.
   - **Boxplots** to identify outliers in withdrawal, deposit, and balance.

## Visualizations

1. **Category Distribution**: Bar plot showing the number of transactions per category.
2. **Average Withdrawal Amount per Month**: Line chart with monthly averages for withdrawals.
3. **Comparison of Monthly Withdrawal and Deposit Amounts**: Line chart showing trends for both.
4. **Descriptive Statistics Boxplots**: Boxplots highlighting the distribution and outliers for withdrawal, deposit, and balance.

## Results

- The majority of transactions are categorized as Misc, followed by Rent and Food.
- Significant fluctuations in the average monthly withdrawal amount, with large withdrawals seen in certain months.
- Most deposits are zero, and a few large deposits skew the data.
- The balance shows significant variance, with some extremely high outliers.

## Prerequisites

To run this analysis, you will need the following libraries:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`

Install them via `pip`:

```bash
pip install pandas numpy matplotlib seaborn
