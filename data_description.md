# 📊 Dataset Descriptions – Grocery Delivery Analytics Project

This project simulates a data environment for a modern online grocery delivery service. The goal is to analyze and optimize delivery operations, customer experience, and product demand using realistic, interconnected datasets.

---

## 1. `orders.csv`  
Simulated grocery orders placed by customers across different cities.

| Column                | Description                                        |
|-----------------------|----------------------------------------------------|
| `order_id`            | Unique identifier for each order                  |
| `customer_id`         | Linked to customer making the order               |
| `order_timestamp`     | Date and time when the order was placed           |
| `delivery_slot`       | Scheduled delivery window (e.g., 10:00–12:00)     |
| `delivery_duration_min` | Time taken to deliver the order (in minutes)   |
| `basket_value_eur`    | Total basket value in euros                        |
| `zip_code`, `city`    | Location info for logistics analysis              |

---

## 2. `customer_profiles.csv`  
Additional attributes describing customers for segmentation and behavioral analysis.

| Column            | Description                                              |
|-------------------|----------------------------------------------------------|
| `customer_id`     | Primary key, links to `orders.csv`                      |
| `signup_date`     | Date the customer registered                            |
| `preferred_slot`  | Customer's preferred delivery window                    |
| `loyalty_score`   | Loyalty score from 1 (low) to 5 (high)                  |
| `has_kids`        | Boolean indicating if the household has children        |

---

## 3. `product_orders.csv`  
Detailed breakdown of which products were included in which order.

| Column        | Description                                               |
|---------------|-----------------------------------------------------------|
| `order_id`    | Linked to an order in `orders.csv`                       |
| `product_id`  | Linked to product info in `products.csv`                |
| `quantity`    | Number of units ordered                                  |
| `unit_price`  | Price per unit of the product (in euros)                |

---

## 4. `products.csv`  
Product catalog with category information.

| Column         | Description                                 |
|----------------|---------------------------------------------|
| `product_id`   | Unique ID for each product                  |
| `product_name` | Placeholder product names                   |
| `category`     | Type of product (e.g., Fruit, Dairy, etc.)  |

---

## 5. `warehouse_operations.csv`  
Daily data from warehouse operations to evaluate logistics performance.

| Column                  | Description                                            |
|--------------------------|--------------------------------------------------------|
| `date`                   | Operational day                                       |
| `warehouse_id`           | Identifier of the warehouse                           |
| `total_orders_processed` | Number of orders processed that day                   |
| `avg_packing_time_min`   | Average time to pack one order (in minutes)           |

---

## 💡 Use Cases / Project Goals
- Identify peak delivery times and optimize delivery slot distribution.
- Segment customers and analyze purchasing behavior.
- Track product-level sales trends and category performance.
- Measure warehouse efficiency and model capacity planning.
