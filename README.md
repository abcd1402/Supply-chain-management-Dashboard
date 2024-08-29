# Supply-chain-management-Dashboard

# About Dataset

Supply chain analytics is a valuable part of data-driven decision-making in various industries such as
manufacturing, retail, healthcare, and logistics. It is the process of collecting, analyzing and interpreting
data related to the movement of products and services from suppliers to customers.
Here is a dataset we collected from a Fashion and Beauty startup. The dataset is based on the supply
chain of Makeup products. 

# Below are all the features in the dataset:
● Product Type
● SKU
● Price
● Availability
● Number of products sold
● Revenue generated
● Customer demographics
● Stock levels
● Lead times
● Order quantities
● Shipping times
● Shipping carriers
● Shipping costs
● Supplier name
● Location
● Lead time
● Production volumes
● Manufacturing lead time
● Manufacturing costs
● Inspection results
● Defect rates
● Transportation modes
● Routes
● Costs


# Supply Chain Management Dashboard Project

# Project Overview
 
 The objective of this project is to create a comprehensive Supply Chain Management (SCM) Dashboard using Tableau. This dashboard will help monitor and optimize various
aspects of the supply chain, including inventory levels, order fulfillment, supplier performance, transportation efficiency, and overall supply chain costs.

# Step 1: Data Preparation
Ensure your data sources cover the following metrics:

# Inventory Management:
● Date
● ProductID
● WarehouseID
● InventoryLevel
● ReorderPoint
● SafetyStock

# Order Fulfillment:
● OrderID
● Date
● CustomerID
● ProductID
● OrderQuantity
● FulfillmentStatus
● DeliveryDate
● OnTimeDelivery

# Supplier Performance:
● SupplierID
● Date
● ProductID
● DeliveryTime
● DefectRate
● Cost

# Transportation Efficiency:
● ShipmentID
● Date
● Carrier
● Origin
● Destination
● TransitTime
● DeliveryStatus

# Supply Chain Costs:
● Date
● CostType
● Amount

# Step 2:Dashboard Creation

# 1. Connect Data Sources:
 Open Tableau Desktop and connect to your prepared data sources (CSV files,databases, etc.).
 
# 2. Create Sheets for Each Metric:

# Inventory Management Sheet:
 ■ Bar Chart: Current inventory levels by product and warehouse.
 ■ Line Chart: Inventory trends over time.
SQL code
// Calculated fields for inventory management
# Days of Inventory Remaining: [InventoryLevel] / AVG([DailySales])

# Order Fulfillment Sheet:
■ Line Chart: Order fulfillment status over time.
■ Bar Chart: On-time delivery rates by product or customer.
SQL code
// Calculated fields for order fulfillment
# On-Time Delivery Rate: `SUM(IF [OnTimeDelivery] = 'Yes' THEN 1 ELSE 0 END) / COUNT([OrderID])`

# Supplier Performance Sheet:
■ Bar Chart: Average delivery time by supplier.
■ Line Chart: Defect rates over time.
SQL code
// Calculated fields for supplier performance
# Average Delivery Time: `AVG([DeliveryTime])`
# Defect Rate: `SUM([DefectiveUnits]) / SUM([TotalUnits])`

# Transportation Efficiency Sheet:
■ Scatter Plot: Transit times by carrier and delivery status.
■ Line Chart: Delivery status over time.
SQL code
// Calculated fields for transportation efficiency
# Average Transit Time: `AVG([TransitTime])`

○ Supply Chain Costs Sheet:
■ Pie Chart: Distribution of costs by type.
■ Line Chart: Supply chain costs over time.
SQL code
// Calculated fields for supply chain costs
# Total Costs: `SUM([Amount])`

# 3. Combine Sheets into a Dashboard:

○ Create a new dashboard.
○ Drag and drop the sheets created in the previous step onto the dashboard
canvas.
○ Arrange the sheets to create a cohesive layout.
○ Add filters and interactive elements to allow users to drill down into specific
metrics.

# 4. Add Titles and Descriptions:

○ Provide clear titles for each sheet and section of the dashboard.
○ Add descriptions to explain what each visualization represents.

# Step 3: Final Report
# Title: Supply Chain Management Dashboard Report

# 1. Overview
● Total Inventory Value: $5,000,000
● On-Time Delivery Rate: 95%
● Average Supplier Delivery Time: 3 days
● Total Supply Chain Costs: $2,500,000

# 2. Inventory Management
● Current Inventory Levels: Adequate for the next 30 days.
● Reorder Points and Safety Stock: All products are above reorder points and
safety stock levels.
● Trend Analysis: Inventory levels are stable with slight seasonal variations.

# 3. Order Fulfillment
● Number of Orders Fulfilled: 1,200
● On-Time Deliveries: 1,140 (95%)
● Average Fulfillment Time: 2 days

# 4. Supplier Performance
● Top Supplier Delivery Time: 2 days
● Average Defect Rate: 0.5%
● Cost Efficiency: Suppliers are providing cost-effective solutions.

# 5. Transportation Efficiency
● Average Transit Time: 3 days
● Delivery Status: 98% of deliveries are on time.
● Carrier Performance: Carrier A has the shortest transit time.

# 6. Supply Chain Costs
● Cost Distribution:
○ Transportation: 40%
○ Inventory Holding: 30%
○ Order Processing: 20%
○ Miscellaneous: 10%
● Cost Trends: Costs have been stable, with a slight increase in transportation costs.

# Conclusion: 
The Supply Chain Management Dashboard provides a detailed view of the supply chain's performance. By tracking key metrics such as inventory levels, order
fulfillment, supplier performance, transportation efficiency, and costs, the dashboard helps identify areas for improvement and ensures efficient supply                                                      
chain operations.

# Code and Calculated Fields

// Inventory Management Calculations
Days of Inventory Remaining: [InventoryLevel] / AVG([DailySales])

// Order Fulfillment Calculations
On-Time Delivery Rate: SUM(IF [OnTimeDelivery] = 'Yes' THEN 1 ELSE 0 END) /COUNT([OrderID])

// Supplier Performance Calculations
Average Delivery Time: AVG([DeliveryTime])
Defect Rate: SUM([DefectiveUnits]) / SUM([TotalUnits])

// Transportation Efficiency Calculations
Average Transit Time: AVG([TransitTime])

// Supply Chain Costs Calculations
Total Costs: SUM([Amount])

# Exporting the Dashboard

After creating the dashboard:
1. Go to File > Export As > Image/PDF to save a static version of the dashboard.
2. Alternatively, you can publish the dashboard to POWER BI for interactive use.This project plan provides a structured approach to                                            
implementing a Supply Chain Management dashboard using power bi, complete with data preparation guidelines, dashboard creation steps, and a final report template.
