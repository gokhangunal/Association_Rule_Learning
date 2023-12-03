## Business Problem
- Below are the basket information for 3 different users. Make the most suitable product recommendation using association rules for these basket informations. Product recommendations can be one or more than one. Derive decision rules from 2010-2011 Germany customers.
  - User 1's basket contains product with ID: 21987
  - User 2's basket contains product with ID: 23235
  - User 3's basket contains product with ID: 22747

## Dataset Story
- The dataset named Online Retail II includes online sales transactions of a UK-based retail company between 01/12/2009 - 09/12/2011. The company's product catalog contains gift items, and it is known that most of its customers are wholesalers.

## Variables
- InvoiceNo
- StockCode
- Description
- Quantity
- InvoiceDate
- UnitPrice
- CustomerID
- Country

## Observations
- Observations: 541,909 | Size: 45.6MB
  - Invoice Number (If this code starts with 'C', it indicates the transaction is cancelled)
  - Product code (Unique for each product)
  - Product name
  - Quantity of the product (The number of each product sold in invoices)
  - Invoice date
  - Invoice price (Sterling)
  - Unique customer number
  - Country name

## Project Tasks

### Task 1: Data Preparation
- Step 1: Read the 2010-2011 sheet from the Online Retail II dataset.
- Step 2: Drop observation units with 'POST' in StockCode. (POST does not represent a charge product added to each invoice.)
- Step 3: Drop observation units containing empty values.
- Step 4: Remove values containing 'C' in Invoice. ('C' indicates cancellation of the invoice.)
- Step 5: Filter observation units with Price values less than zero.
- Step 6: Investigate and if necessary suppress outliers in Price and Quantity variables.

### Task 2: Generating Association Rules for German Customers
- Step 1: Define the create_invoice_product_df function to create an invoice product pivot table as below.
- Step 2: Define the create_rules function to generate rules and find rules for German customers.

### Task 3: Making Product Recommendations for Users Given Product IDs in Basket
- Step 1: Use the check_id function to find the names of the given products.
- Step 2: Use the arl_recommender function to make product recommendations for 3 users.
- Step 3: Look at the names of the recommended products.
