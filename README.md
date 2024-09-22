# RFM Analysis of Online Retail Data

## Project Overview
This project implements RFM (Recency, Frequency, Monetary) analysis on the [Online Retail II dataset](https://archive.ics.uci.edu/ml/datasets/Online+Retail+II) to segment customers and generate actionable insights for marketing strategy optimization. The dataset consists of transaction data from a UK-based online retailer, recorded between 2009-2011.

## Business Problem
Understanding customer behavior is critical for improving customer acquisition, retention, and loyalty. RFM analysis provides a framework to categorize customers based on:

- **Recency**: Days since last purchase.
- **Frequency**: Number of purchases.
- **Monetary**: Total amount spent.

## Data Description
- **InvoiceNo**: Unique identifier for each transaction (cancellations prefixed with 'C').
- **StockCode**: Unique product code.
- **Description**: Product name.
- **Quantity**: Number of products per transaction.
- **InvoiceDate**: Date and time of transaction.
- **UnitPrice**: Product price (in GBP).
- **CustomerID**: Unique customer identifier.
- **Country**: Customer's residing country.

## Data Preprocessing
- **Missing Data**: Handled missing `Description` and `CustomerID` values.
- **Refunds and Negative Quantities**: Removed cancelled transactions and negative-quantity entries to ensure data accuracy.
- **Irrelevant Products**: Filtered out products with '0.00' prices and non-sale items (e.g., marketing materials, samples).

## Methodology

### RFM Segmentation
1. **Recency**: Calculated as the days since the customer's last purchase.
2. **Frequency**: Count of unique transactions per customer.
3. **Monetary**: Total spend by customer.

Customers were assigned scores from 1 (lowest) to 5 (highest) for each metric, and these scores were used to segment the customer base.

### Segments & Recommendations:

- **Champions**: (Highest RFM Scores) Recently active, frequent, and high spenders.
    - **Recommendations**: 
        - Loyalty Programs: Offer exclusive rewards for continued purchases.
        - VIP Events: Invite them to special sales events.
        - Personalized Thank You Notes: Express gratitude for their loyalty.

- **Loyal Customers**: Regular buyers with solid spending patterns.
    - **Recommendations**: 
        - Targeted Offers: Send exclusive discounts to encourage more purchases.
        - Referral Programs: Incentivize referrals with rewards.

- **New Customers**: Recent buyers with potential for loyalty.
    - **Recommendations**: 
        - Onboarding Campaign: Welcome email series with a discount.
        - Interactive Guides: Tutorials on using their first purchase.

- **At-Risk**: Previously frequent customers who haven’t purchased in a while.
    - **Recommendations**: 
        - Win-Back Campaign: Offer 20% off the next order, valid for 7 days.
        - Feedback Requests: Solicit feedback to understand reduced engagement.

- **Hibernating**: Customers who have stopped engaging.
    - **Recommendations**: 
        - Re-engagement Campaign: Targeted email with a special offer.
        - Exclusive Access: Early access to new arrivals.

## Key Insights

### Product-Level Insights:
- Top 5 products contribute 4.98% of total revenue.
  - **Regency Cake 3 Tier** is the best seller with 1.66% revenue share.
  - Products like **Jumbo Bag Red Retrospot** show high quantities sold per order.

### Country-Level Insights:
- The **UK** dominates sales, accounting for **86%** of total revenue.
- Other countries contribute about **3%** each, showing potential for international growth.

### Sales Trends:
- **Day Performance**: **Thursday** is the highest-performing day, while **Saturday** shows minimal sales.
- **Optimal Sales Hours**: Peak sales hours occur between **12 PM** and **3 PM**, indicating optimal times for marketing campaigns.
- **Seasonal Trends**: Increased sales are observed from **May to October**.

## Recommendations
1. **Engagement Strategy**: Focus on Champions and Loyal Customers for upselling and loyalty programs. Offer exclusive deals to At-Risk and Hibernating customers to re-engage them.
2. **Product Strategy**: Promote high-revenue products like **Regency Cake** and **Jumbo Bag** in top-performing customer segments.
3. **Timing Campaigns**: Schedule promotions during peak sales hours and optimize resources around Thursday, the most active sales day.
4. **International Expansion**: Explore targeted campaigns for non-UK markets, especially the top 5 international countries.

For a detailed analysis of all customer segments and their performance metrics, refer to the Jupyter Notebook file (`RFM Analysis - Online Retail.ipynb`), which includes in-depth visualizations and RFM segmentation strategies.

## Files Included
- **online_retail_II.xlsx**: The dataset used for analysis (download from [this link](https://archive.ics.uci.edu/ml/datasets/Online+Retail)).
- **RFM Analysis - Online Retail.ipynb**: Jupyter Notebook containing the analysis, visualizations, and RFM segmentation strategies.

## Conclusion
RFM analysis has provided a clear segmentation of customers, helping us identify high-value segments, optimize marketing efforts, and increase overall customer retention and revenue.
