
# Olist E-commerce Data Analysis

Welcome to the Olist E-commerce Data Analysis repository! This repository contains an analysis of a Brazilian e-commerce dataset from Olist Store. The dataset consists of information on 100k orders made between 2016 and 2018, across multiple marketplaces in Brazil. The dataset offers a comprehensive view of orders from various dimensions, including order status, price, payment and freight performance, customer location, product attributes, and customer reviews. We have also provided a geolocation dataset that maps Brazilian zip codes to lat/lng coordinates.

## About the Dataset

This dataset represents real commercial data; however, it has been anonymized. References to the companies and partners in the review text have been replaced with the names of Game of Thrones great houses.

## Analysis Goals

The aim of this project is to perform various analyses on the Olist dataset using R and the following libraries: tidyverse, ggplot2, dplyr, ggrepel, ggthemes, lubridate, and RColorBrewer. The analyses will focus on the following aspects:

### Sales Analysis

- Total Sales Over Time: Identify seasonal patterns, trends, and variations in sales over time.
- Sales Distribution by Product Category: Determine the most popular product categories with high demand.

### Customer Behavior Analysis

- Geographical Analysis: Explore customer locations and identify regions with a high concentration of buyers.

### Payment Analysis

- Preferred Payment Methods: Identify the most commonly used payment methods by customers.

### Customer Feedback Analysis

- Sentiment Analysis in Reviews: Perform sentiment analysis on customer reviews to identify positive and negative opinions about products and services.
- Feedback Trends: Identify key topics mentioned in reviews and analyze trends over time.

## Getting Started

To get started with the analysis, follow these steps:

1. Clone the repository: `git clone https://github.com/GabrielTelles4K/olist-analysis.git`
2. Install the required libraries: `install.packages(c("tidyverse", "ggplot2", "ggthemes", "dplyr", "ggrepel", "lubridate", "RColorBrewer"))`
3. Launch RStudio or your preferred R environment.
4. Open the project file: `olist-analysis.Rproj`.
5. Open the analysis script: `analysis.R`.
6. Run the script to perform the desired analyses.

Feel free to explore the code, modify it according to your needs, and contribute to the repository.

## License

This project is licensed under the [MIT License](LICENSE).
