# Cohort Analysis and Retention Rate Evaluation

> Analysis of user data for a marketplace selling goods from Brazil.  
> Goal: measure retention rate and assess product/market fit.

## Project Overview

This project analyzes user behavior on a marketplace offering products from Brazil. Using **cohort analysis** and calculating the **monthly retention rate**, we:

- Measure how often users return to make repeat purchases.
- Evaluate business stability and sustainability through the lens of **product/market fit**.

## Objectives

1. **Estimate monthly retention rate using cohort analysis**
2. **Define cohorts based on registration month**
3. **Calculate the share of users who returned for repeat purchases in each month of the cohort lifecycle**
4. **Assess whether product/market fit exists**
5. **Draw conclusions based on retention dynamics and customer acquisition stability**

## Data Used

### Available Files:

| File | Description |
|------|-------------|
| `olist_customers_dataset.csv` | Customer information |
| `olist_orders_dataset.csv` | Orders table |
| `olist_order_items_dataset.csv` | Order item details |

---

### 1. `olist_customers_dataset.csv`

| Field | Description |
|-------|-------------|
| `customer_id` | Per-order customer identifier |
| `customer_unique_id` | Unique customer identifier (similar to a passport number) |
| `customer_zip_code_prefix` | Customer ZIP code |
| `customer_city` | Customer delivery city |
| `customer_state` | Customer delivery state |

---

### 2. `olist_orders_dataset.csv`

| Field | Description |
|-------|-------------|
| `order_id` | Unique order identifier (receipt number) |
| `customer_id` | Per-order customer identifier |
| `order_status` | Order status |
| `order_purchase_timestamp` | Order creation timestamp |
| `order_approved_at` | Payment approval timestamp |
| `order_delivered_carrier_date` | Date handed over to carrier |
| `order_delivered_customer_date` | Delivery date to customer |
| `order_estimated_delivery_date` | Estimated delivery date |

---

### 3. `olist_order_items_dataset.csv`

| Field | Description |
|-------|-------------|
| `order_id` | Unique order identifier (receipt number) |
| `order_item_id` | Item identifier within the order |
| `product_id` | Product ID (similar to a barcode) |
| `seller_id` | Seller ID |
| `shipping_limit_date` | Seller shipment deadline |
| `price` | Unit price |
| `freight_value` | Shipping cost |

---

## Unique Order Statuses

The `order_status` field in `olist_orders_dataset` contains the following values:

- `created` — created  
- `approved` — approved  
- `invoiced` — invoiced  
- `processing` — processing  
- `shipped` — shipped  
- `delivered` — delivered  
- `unavailable` — canceled due to product unavailability  
- `canceled` — canceled  
