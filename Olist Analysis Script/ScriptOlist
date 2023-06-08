# Load the necessary libraries
library(tidyverse)
library(ggplot2)
library(lubridate)
library(RColorBrewer)
library(ggthemes)

#========================================================Total Sales Over Time=========================================================================================================

# Read the CSV file
data <- read.csv("olist_orders_dataset.csv")

# Filter only delivered orders
data <- data %>% filter(order_status == "delivered")

# Convert 'order_purchase_timestamp' column to date and time format
data$order_purchase_timestamp <- as.POSIXct(data$order_purchase_timestamp, format = "%Y-%m-%d %H:%M:%S")

# Create a new column for the year
data <- data %>% mutate(Year = year(order_purchase_timestamp))

# Create a new column for the quarter
data <- data %>% mutate(Quarter = quarter(order_purchase_timestamp))

# Calculate total sales per quarter and year
sales_by_quarter <- data %>%
  group_by(Year, Quarter) %>%
  summarise(TotalSales = n())

# Define the color palette
colors <- brewer.pal(n = length(unique(sales_by_quarter$Year)), name = "Set1")

# Plot the bar chart of total sales per quarter and year
ggplot(sales_by_quarter, aes(x = factor(Quarter), y = TotalSales, fill = factor(Year))) +
  geom_bar(stat = "identity", position = "dodge") +
  geom_text(aes(label = TotalSales), vjust = -0.5, color = "black", size = 3.5, position = position_dodge(width = 0.9)) +
  labs(x = "Quarter", y = "Total Sales", title = "Total Sales per Quarter and Year") +
  scale_fill_manual(values = colors) +
  theme_bw() +
  theme(plot.title = element_text(size = 14, face = "bold"),
        axis.title = element_text(size = 12),
        axis.text = element_text(size = 10),
        legend.title = element_blank(),
        legend.position = "bottom")

#=======================================================Sales Distribution by Product Category=========================================================================================

# Read the CSV file with product information
products <- read.csv("olist_products_dataset.csv")

# Read the CSV file with order item information
order_items <- read.csv("olist_order_items_dataset.csv")

# Combine the 'products' and 'order_items' data frames using the 'product_id' column
combined_data <- inner_join(products, order_items, by = "product_id")

# Calculate total sales by product category
sales_by_category <- combined_data %>%
  group_by(product_category_name) %>%
  summarise(TotalSales = sum(price)) %>%
  arrange(desc(TotalSales)) %>%
  top_n(10)

# Plot the bar chart of sales distribution by product category
ggplot(sales_by_category, aes(x = reorder(product_category_name, TotalSales), y = TotalSales)) +
  geom_bar(stat = "identity", fill = "#FF7F00") +
  labs(x = "Product Category", y = "Total Sales", title = "Top 10 Best Selling Product Categories") +
  theme_minimal() +
  theme(axis.text.x = element_text(angle = 45, hjust = 1),
        plot.title = element_text(size = 16, face = "bold"),
        axis.title = element_text(size = 12),
        axis.text = element_text(size = 10),
        panel.grid.major = element_blank(),
        panel.grid.minor = element_blank(),
        panel.border = element_blank(),
        legend.position = "none")

#=================================================================================================================================================================


