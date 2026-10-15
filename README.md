# Task-3-Isaac_Okolie
# Project 3: E-Commerce Sales Analysis Using SQL
### DecodeLabs Data Analytics Internship

---

## 📌 What This Project Is About

This project uses SQL to extract actionable business insights from an
e-commerce sales dataset. Raw transactional data was queried, cleaned,
and analyzed to uncover patterns across revenue, customers, products,
marketing channels, and order fulfillment.

The core principle: **Transform raw data into meaningful business decisions.**

---

## 🎯 Objectives

- Analyze revenue performance
- Understand customer behavior
- Measure product performance
- Evaluate marketing effectiveness
- Assess order fulfillment performance

---

## 📊 Dataset Overview

| Property | Detail |
|----------|--------|
| Dataset | Orders Table |
| Total Records | 1,200 Orders |
| Database | MySQL |
| Database Name | Project_3 |

### Columns in Dataset:
- OrderID, Date, CustomerID, Product, Quantity, UnitPrice
- ShippingAddress, PaymentMethod, OrderStatus, TrackingNumber
- ItemsInCart, CouponCode, ReferralSource, TotalPrice

---

## 🛠️ Tools Used

- MySQL (Database Management System)
- SQL (Structured Query Language)

---

## 🗄️ Database Setup

```sql
CREATE DATABASE Project_3;
USE Project_3;
```

---

## 🔍 Data Cleaning

### Issue Found: Missing CouponCode Values

**Finding:** 309 records had empty CouponCode values

**Resolution:**
```sql
UPDATE orders_table
SET CouponCode = 'No Coupon Used'
WHERE CouponCode = '';
```

**Impact:** No records lost — dataset completeness improved ✅

---

## 📋 Queries & Business Insights

### 1. Revenue Analysis

| Query | Result | Business Insight |
|-------|--------|-----------------|
| Total Revenue | **$1,264,762** | Business generated over $1.26M in sales |
| Average Order Value | **$1,053.97** | Customers spend ~$1,054 per transaction |

### 2. Customer Analysis

| Query | Result | Business Insight |
|-------|--------|-----------------|
| Unique Customers | **1,189** | Strong customer base acquired |

### 3. Order Fulfillment

| Query | Result | Business Insight |
|-------|--------|-----------------|
| Revenue Lost to Returns | **$243,278** | Significant revenue lost post-delivery |
| Revenue Lost to Cancellations | **$276,396** | Even greater loss before fulfillment |
| Combined Loss | **$519,674** | 41% of revenue at risk |

---

## 💡 Key Findings

- Total Revenue exceeded **$1.26 million**
- Average Order Value was approximately **$1,054**
- **1,189 unique customers** made purchases
- Returns resulted in **$243,278** in lost revenue
- Cancellations resulted in **$276,396** in lost revenue
- Marketing channels differ significantly in revenue contribution
- Product performance varies across categories
- Coupon usage provides insight into promotion effectiveness

---

## ✅ Final Recommendations

1. Increase focus on top-performing products
2. Optimize marketing spend toward high-revenue referral sources
3. Reduce cancellations through improved order processing
4. Investigate return causes to recover lost revenue
5. Expand successful promotional campaigns
6. Develop customer retention strategies
7. Use revenue trends for forecasting and inventory planning

---

## 📁 Files in This Repository

| File | Description |
|------|-------------|
| `project_3_dataset.csv` | Raw dataset imported into MySQL |
| `project_3_queries.sql` | All 18 SQL queries used in analysis |
| `project_3_report.docx` | Full written report with findings |
| `screenshots/` | Query result screenshots |
| `README.md` | This documentation file |

---

## 🔢 Full Query List

| # | Query | Category |
|---|-------|---------|
| 1 | View full dataset | Inspection |
| 2 | Count total orders | Inspection |
| 3 | Preview first 10 records | Inspection |
| 4 | Check unique values | Cleaning |
| 5 | Count coupon usage & fix nulls | Cleaning |
| 6 | Total revenue generated | Revenue |
| 7 | Average order value | Revenue |
| 8 | Total unique customers | Customer |
| 9 | Revenue by product | Product |
| 10 | Quantity sold by product | Product |
| 11 | Revenue by payment method | Payment |
| 12 | Revenue by referral source | Marketing |
| 13 | Orders by status | Fulfillment |
| 14 | Revenue lost through returns | Fulfillment |
| 15 | Revenue lost through cancellations | Fulfillment |
| 16 | Average cart size by referral source | Behavior |
| 17 | Most used coupon code | Promotional |
| 18 | Revenue by year | Trend |

---

## 👤 Author
**Isaac Okolie**
DecodeLabs Data Analytics Intern

