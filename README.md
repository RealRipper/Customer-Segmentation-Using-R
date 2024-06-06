# Customer-Segmentation-Using-R
# Importing libraries
library(readr)  # Assuming readr is used instead of read.csv for data import
library(stringr)  # Might be useful for data manipulation
library(summary)  # Base R package for summary statistics
library(ggplot2)  # For creating more advanced visualizations (optional)

# Load customer data
customer_data <- read.csv("Mall_Customers.csv")  # Assuming the file is in the working directory

# Explore data structure and variable names
str(customer_data)
names(customer_data)

# Preview first few rows
head(customer_data)

# Get summary statistics for each variable
summary(customer_data)

# Customer gender distribution (if needed)
# Assuming gender data is stored in a variable named "Gender"

# Gender frequency table (optional)
gender_counts <- table(customer_data$Gender)

# Visualizations (optional)
# Use ggplot2 for more customization

# Age distribution
ggplot(customer_data, aes(x = Age)) +
  geom_histogram(bins = 30, fill = "steelblue") +
  labs(title = "Distribution of Customer Age", x = "Age", y = "Frequency") +
  theme_bw()

# Annual income distribution
ggplot(customer_data, aes(x = `Annual.Income..k..`)) +
  geom_histogram(bins = 20, fill = "goldenrod1") +
  labs(title = "Distribution of Annual Income", x = "Annual Income", y = "Frequency") +
  theme_bw()

# Analyze spending score
summary(customer_data$`Spending.Score..1.100.`)

# Spending score distribution (optional)
ggplot(customer_data, aes(x = `Spending.Score..1.100.`)) +
  geom_histogram(bins = 20, fill = "skyblue") +
  labs(title = "Distribution of Spending Score", x = "Spending Score", y = "Frequency") +
  theme_bw()

# K-Means clustering for customer segmentation (separate code block)
# ... (code for K-Means clustering will be here) ...
