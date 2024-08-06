# Streamline Logistics Order Fulfillment Dashboard

### Project Overview

Streamline Logistics Solutions is facing significant challenges in its order fulfillment process, including: mounting order backlogs, lack of order visibility for customers, rising customer dissatisfaction due to delays and communication gaps, and escalating operational costs. This data analysis project aims to address these challenges by developing an interactive Excel dashboard that enhances visibility, efficiency, and customer satisfaction in our order fulfillment operations.

### Data Sources

Delivery data: The primary dataset used for this analysis is the "Delivery_data.xlsx" file containing detailed information about each delivery made from the 1st to the 8th of September, 2023.

### Tools

- Excel - Data cleaning, analysis, visualization and dashboard development.

### Data Description

This case study contains a single dataset and it comprises of;
-  Order ID: A unique identifier for each customer order.
-  Delivery Address: The address to which the order is to be delivered.
-  Order Timestamp: The date and time when the order was placed (e.g., "2023-09-01 08:00").
-  Order Status: The current status of the order (e.g., "In Progress" or "Completed").
-  Driver ID: A unique identifier for each driver assigned to deliver orders.
-  Vehicle Info: Information about the delivery vehicle used for the order.
-  Current Location: The current location of the delivery driver during order delivery.
-  Delays: Any delays that occurred during the delivery, measured in minutes (e.g., "15 min").
-  Driver Status: Provides information on drivers with high number of trips and those with few trips.
-  Delivery Time: The total time taken for delivery, measured in minutes (e.g., "120 min").
-  Actual Delivery Duration: The actual delivery time.
-  Delay Status: Stores information about the orders that were delayed and the orders that were on time.

### Data Cleaning and Preparation

The dataset underwent thorough cleaning and preparation to ensure data integrity and suitability for analysis. Steps included:

- creating a table using CTRL + T,
- standardizing formats,
- creating new columns:
  - Driver status, using (=IFERROR((IF(COUNTIFS([Driver ID], [@[Driver ID]]) < 16, "Under Utilized","Utilized")), "")),
  - Actual Delivery Duration, using (=[@[Delivery Time (min)]]-[@[Delays (min)]]),
  - Delay Status, using (=IF([@[Delays (min)]]>0,"Delayed", "On time")).
- splitting the delivery address column into 2 (delivery address and delivery location), to allow for easy readability and analysis.

###  Exploratory Data Analysis (EDA)

EDA was conducted using pivot tables and statistical techniques to uncover insights into the challenges in Streamline logistics solutions. Analyzing customer satisfaction through average delivery time, customer complaints related to delays, helps benchmark performance against customer expectations, and address pain points; while customer communication, monitoring progress and delays, resource allocations and efficiency patterns were analyzed across the order timestamp.
By analyzing the delivery data, this project aims to provide actionable recommendations to drive sustainable business growth.

### Results and Insights





