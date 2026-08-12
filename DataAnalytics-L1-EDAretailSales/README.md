# Retail Sales Data Analysis Project
**Objective:** Explore an e-commerce customer behavior dataset to uncover patterns, understand our customers, and make actionable business recommendations.

## 1. Initial Data Check
When I first loaded the dataset, I checked its structure to see what we were working with:
* **Size:** I looked at how many rows and columns we had.
* **Data Types:** I noticed dates were saved as text, which needed to be fixed for time-based analysis.
* **Missing Data:** I checked for any empty spots or missing values in the dataset.

## 2. Basic Statistics
I calculated the average (mean), middle point (median), and most common values (mode) for numerical columns like Age and Total Amount. 
* This helped me quickly see if a few massive purchases were skewing the average.

## 3. Finding Trends Over Time
I converted the dates into the proper format and grouped the sales by Month and Quarter.
* **Monthly Trends:** I used line charts to see the peaks and valleys in sales throughout the year (like holiday spikes).
* **Quarterly Trends:** I looked at high-level business growth across Q1, Q2, Q3, and Q4.

## 4. Understanding the Customers
To help with targeted marketing, I analyzed *who* was buying from the store:
* **Age:** I used a histogram to find the most common age bracket of our shoppers.
* **Gender:** I used a pie chart to see the percentage breakdown between male and female customers.

## 5. What Products Are Selling?
I looked at the product categories in two different ways using bar charts:
* **By Quantity:** Which items sell the most physical units? (Good for inventory planning).
* **By Revenue:** Which items bring in the most money? (Some items sell less but cost more, making them highly profitable).

## 6. How Are Things Connected?
I created a **Correlation Heatmap** to see how strongly variables relate to each other.
* I checked if older customers tend to spend more money, and if discounts directly lead to higher purchase quantities.

## 7. The Impact of Slow Delivery
I dug deeper to find a non-obvious insight: Does delivery speed affect customer happiness?
* Using a **Boxplot**, I compared delivery times against 1-to-5 star Customer Ratings.
* This showed whether the 1-star ratings were consistently linked to packages taking longer to arrive.

## 8. Final Business Recommendations
Based on the data, I came up with 3 actionable recommendations:
1. **Prepare for Peaks:** Stock up inventory and boost marketing budgets right before our identified busy months.
2. **Promote the Money-Makers:** Keep high-quantity items in stock to drive traffic, but aggressively upsell the high-revenue categories to boost profits.
3. **Speed Up Shipping:** Because slow delivery proved to cause bad reviews, the business should partner with faster shipping companies to improve customer retention.

