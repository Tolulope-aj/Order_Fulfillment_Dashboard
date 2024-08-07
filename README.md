# Streamline Logistics Order Fulfillment Dashboard

### Project Overview

Streamline Logistics Solutions is facing significant challenges in its order fulfillment process, including: mounting order backlogs, lack of order visibility for customers, rising customer dissatisfaction due to delays and communication gaps, and escalating operational costs. This data analysis project aims to address these challenges by developing an interactive Excel dashboard that enhances visibility, efficiency, and customer satisfaction in its order fulfillment operations.


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
- splitting the delivery address column into 2 (delivery address and delivery city), to allow for easy readability and analysis.


###  Exploratory Data Analysis (EDA)

EDA was conducted using pivot tables and statistical techniques to uncover insights into the challenges in Streamline logistics solutions. Analyzing customer satisfaction through average delivery time, customer complaints related to delays, helps benchmark performance against customer expectations, and address pain points; while customer communication, monitoring progress and delays, resource allocations and efficiency patterns were analyzed across the order timestamp.
By analyzing the delivery data, this project aims to provide actionable recommendations to drive sustainable business growth.


### Results and Insights

1. Streamline logistics solutions has 1,500 orders to be delivered to 5 cities (City A, B, C, D, and E), within the 1st and the 8th of September, 2023. This logistics company has 100 drivers with unique driver IDs and three different vehicles used for deliveries i.e Van A, Truck B and Bike C.
2. Currently, there are 767 orders in progress and 733 orders have been completed. Despite the high volume, delays are a significant issue. Of the completed orders, 712 experienced delays, and 742 of the in-progress orders are also delayed.
3. There are 529 negative feedbacks, 490 neutral feedbacks, and 481 positive feedbacks from customers. This distribution highlights the need for targeted improvements to increase positive customer experiences.
4. The average delay time for customers is 15 minutes, meaning any delay beyond this is considered extreme. About 46.73% of customers orders were extremely delayed.
5. Drivers are averaging 16 trips each. Drivers with fewer than 16 trips are considered underutilized. Notably, Driver 34, who has made 25 trips in 8 days, has the highest number of delays in minutes, indicating potential areas for review in driver allocation and route planning.
6. September 3rd stands out as the peak delivery day between September 1st and September 8th, indicating potential capacity issues on that specific date.
7. Delivery times vary significantly across cities. City B has the highest average delivery time of 153.16 minutes, while City D boasts the lowest average delivery time at 149.70 minutes.
8. City B is handling the highest volume with 320 orders, whereas City E has the lowest with 272 orders.
9. For all completed orders, Route 2 experienced the highest number of delay time with a total of 2,201 mins, while Route 1 experienced the lowest with a total of 1,898 mins.


### Recommendations

1. Reevaluate the allocation of trips to drivers, especially focusing on underutilized drivers (those with fewer than 16 trips). Ensure a more balanced distribution of trips to prevent overburdening certain drivers, such as Driver 34. Also, provide additional training and support to drivers experiencing high delays to improve their efficiency and adherence to schedules.
2. If the high number of delay minutes attributed to Route 2 is due to bad road conditions, other routes should be considered. However, if the delays are primarily due to traffic congestion, then deploying Bike C on that route more frequently could help reduce backlogs.
3. Provide customers with real-time updates on their order status, including estimated delivery times and notifications of any delays. This can help manage customer expectations and reduce dissatisfaction.
4. Increase resources (drivers and vehicles) on peak delivery days like September 3rd to handle the higher volume of orders efficiently. This can prevent capacity issues and ensure timely deliveries.
5. To ensure that the different vehicle types are being utilized efficiently based on order size, delivery location, and traffic conditions. Smaller vehicles like Bike C could be more effective for short-distance or inter-city deliveries.
6. Integrate advanced technologies such as GPS tracking, automated dispatch systems, and real-time traffic data to reduce delays and improve overall operational efficiency.
7. Enhance customer support services to promptly address and resolve issues related to delays and other concerns, this can help mitigate the impact of delays on customer satisfaction.
8. Consider offering incentives such as discounts or vouchers to customers affected by significant delays, as a goodwill gesture to maintain positive relationships and loyalty.
9. Use key performance indicators (KPIs) such as average delivery time, delay times, driver utilization, and customer feedback to continually assess and improve the effectiveness of implemented strategies.


### Conclusion

Streamline Logistics Solutions faces several challenges in its order fulfillment processes, including significant delays, uneven driver utilization, and varying delivery times across cities. By optimizing driver allocation, improving route planning, enhancing customer communication, and focusing on city-specific strategies, we can address these issues effectively. 
Implementing real-time updates, increasing resources on peak delivery days, and leveraging technology for operational efficiency will further reduce delays and improve customer satisfaction. Regular performance monitoring and targeted improvements based on feedback will help maintain its reputation for reliability and excellence. By adopting these recommendations, Streamline Logistics Solutions can achieve a more efficient, customer-centric, and successful order fulfillment process.
