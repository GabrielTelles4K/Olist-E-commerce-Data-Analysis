# Olist E-commerce Data Analysis

Welcome to the Olist E-commerce Data Analysis repository! This repository contains an analysis of a Brazilian e-commerce dataset from Olist Store. The dataset consists of information on 100k orders made between 2016 and 2018, across multiple marketplaces in Brazil. The analysis provides insights into various aspects of the dataset, including total sales over time, sales distribution by product category, geographical analysis, payment analysis, and customer reviews.

## Dataset Description

The dataset represents real commercial data from Olist Store, but it has been anonymized to ensure privacy. References to the companies and partners in the review text have been replaced with the names of Game of Thrones great houses. The dataset includes the following files:

- `olist_orders_dataset.csv`: Information about the orders, including purchase timestamp, order status, and customer ID.
- `olist_products_dataset.csv`: Information about the products, including category and price.
- `olist_order_items_dataset.csv`: Information about the items in each order, including product ID and price.
- `olist_customers_dataset.csv`: Information about the customers, including location.
- `olist_order_payments_dataset.csv`: Information about the payments made for the orders, including payment type.
- `olist_order_reviews_dataset.csv`: Information about the reviews written by customers, including review score.

## Analysis Objectives

The analysis in this repository aims to provide insights into different aspects of the Olist e-commerce dataset. The objectives of each analysis script are as follows:

1. **Total Sales Over Time**: Analyzes the total sales over time and presents the sales per quarter and year.
2. **Sales Distribution by Product Category**: Examines the sales distribution across various product categories and identifies the top-selling categories.
3. **Geographical Analysis**: Investigates the geographical aspects of the dataset, including the total number of customers by state and the top cities with the most customers in the state with the highest customer count.
4. **Payment Analysis**: Analyzes the preferred payment methods used by customers and presents the distribution of payment methods.
5. **Customer Reviews**: Analyzes the customer review ratings and presents the distribution of ratings on a scale of 1 to 5.

## Dependencies

The analysis scripts in this repository require the following R libraries:

- `tidyverse`: Provides a set of packages for data manipulation and visualization.
- `ggplot2`: Enables the creation of high-quality data visualizations.
- `lubridate`: Offers functions to work with dates and times.
- `RColorBrewer`: Provides color palettes for data visualization.
- `ggthemes`: Offers additional themes for ggplot2 visualizations.
- `dplyr`: Provides functions for data manipulation.
- `ggrepel`: Offers text labels that do not overlap with data points in ggplot2 visualizations.

Please make sure to have these libraries installed before running the analysis scripts.

## Getting Started

To start modifying the code and conducting your own analysis, follow these steps:

1. **git clone https://github.com/GabrielTelles4K/olist-e-commerce-analysis.git**: Start by cloning this repository to your local machine using the following command:

2. **install.packages(c("tidyverse", "ggplot2", "lubridate", "RColorBrewer", "ggthemes", "dplyr", "ggrepel"))

**: Make sure you have the necessary dependencies installed. Run the following command to install the required libraries:

3. **Load the Dataset**: Place the dataset files (`olist_orders_dataset.csv`, `olist_products_dataset.csv`, etc.) in the repository's root directory.

4. **Modify the Code**: Open the analysis scripts in your preferred R environment (e.g., RStudio) and start modifying the code according to your specific analysis goals. Feel free to add new visualizations, explore additional variables, or apply different data transformations.

5. **Run the Code**: Execute the modified code in your R environment to generate the updated visualizations and analysis results.

6. **Document Your Changes**: As you make modifications to the code, document your changes and any insights you uncover in the repository's README file. This will help others understand your analysis and contribute to the project if desired.

7. **Commit and Push**: Once you are satisfied with your modifications, commit your changes and push them to your GitHub repository. This will make your analysis accessible

## Olist

https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce
