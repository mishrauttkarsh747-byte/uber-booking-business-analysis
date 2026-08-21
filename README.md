# 🚕 Uber Booking & Revenue Analytics

### Turning 150K+ Uber bookings into actionable business insights using SQL & Power BI
---
## 📌 Project Overview

This project analyzes **150,000 Uber booking records** to understand booking performance, revenue generation, cancellations, customer behavior, vehicle performance, payment methods, demand patterns, and operational inefficiencies.

The objective was not just to create a dashboard, but to answer important **business questions using SQL** and convert the findings into actionable recommendations.

The analysis focuses on one key question:

> **Where is Uber losing bookings and revenue, and what actions can improve operational performance and revenue?**

---

# 🎯 Business Objectives

The analysis was designed to answer the following business questions:

* How many Uber bookings are successfully completed?
* What percentage of bookings are cancelled by drivers?
* How much revenue is generated from completed rides?
* Which vehicle type generates the highest revenue?
* Which vehicle has the highest revenue per kilometer?
* Which payment method is most popular?
* Which customer segment generates the most revenue?
* Which month generates the highest and lowest revenue?
* What are the peak demand hours?
* Which pickup/drop locations generate the most business?
* How significant are customer and driver cancellations?
* How many bookings are lost because no driver is available?
* Why are bookings becoming incomplete?
* Where are the biggest opportunities for revenue improvement?

---

# 📊 Dataset

### Dataset Size

| Metric                 |        Value |
| ---------------------- | -----------: |
| Total Bookings         |  **150,000** |
| Completed Bookings     |   **93,000** |
| Driver Cancellations   |   **27,000** |
| Customer Cancellations |   **10,500** |
| No Driver Found        |   **10,500** |
| Incomplete Bookings    |    **9,000** |
| Completed Revenue      | **~₹47.26M** |

### Key Dataset Fields

The dataset contains information related to:

* Booking ID
* Customer ID
* Booking Status
* Date & Time
* Vehicle Type
* Pickup Location
* Drop Location
* Booking Value
* Ride Distance
* Payment Method
* Customer Rating
* Driver Rating
* Cancellation Information
* Incomplete Ride Reasons

---

# 🛠️ Tools & Technologies

### Data Analysis

* **MySQL**
* SQL
* Window Functions
* CTEs
* Aggregations
* CASE statements
* Ranking functions

### Visualization

* **Microsoft Power BI**
* Interactive dashboard
* KPI cards
* Charts
* Filters & slicers
* Business-focused storytelling

### Data Preparation

* Excel
* Data cleaning
* Data validation
* Data transformation

---

# 🔎 Analysis Approach

The project followed a structured analytics workflow:

```text
Raw Uber Dataset
       ↓
Data Cleaning & Validation
       ↓
Exploratory Data Analysis
       ↓
Business Question Identification
       ↓
SQL Analysis
       ↓
KPI & Metric Creation
       ↓
Power BI Dashboard
       ↓
Business Insights
       ↓
Recommendations
```

---

# 📈 Key Business KPIs

## Booking Performance

| KPI                        |      Result |
| -------------------------- | ----------: |
| Total Bookings             | **150,000** |
| Completed Bookings         |  **93,000** |
| Completion Rate            |     **62%** |
| Driver Cancellation Rate   |     **18%** |
| Customer Cancellation Rate |      **7%** |
| No Driver Found Rate       |      **7%** |
| Incomplete Booking Rate    |      **6%** |

### 🚨 Major Finding

Driver cancellations are significantly higher than customer cancellations.

**Driver cancellations: 18%**

vs.

**Customer cancellations: 7%**

This indicates that driver-side operational issues represent a much larger source of booking loss.

---

# 💰 Revenue Analysis

### Total Completed-Ride Revenue

> **~₹47.26M**

The analysis focuses only on completed rides when calculating actual ride revenue.

---

## 🥇 Highest Revenue Vehicle

**Auto**

* Revenue: **~₹11.73M**
* Revenue contribution: **~24.8%**

Auto is the largest revenue-generating vehicle category in the dataset.

---

## 🥈 Second-Highest Revenue Vehicle

**Go Mini**

* Revenue: **~₹9.41M**
* Revenue Rank: **#2**

This analysis uses the SQL `RANK()` window function to identify vehicle revenue rankings.

---

# 🚗 Revenue Efficiency

## Highest Revenue per Kilometer

**Go Sedan**

> **~₹19.71/km**

This metric was calculated as:

```text
Total Completed Revenue
----------------------
Total Ride Distance
```

This helps identify vehicle categories that generate more revenue relative to the distance travelled.

---

# 💵 Highest Average Booking Value

**Go Sedan**

> **~₹512 average booking value**

This suggests that although another vehicle category may generate higher total revenue because of booking volume, Go Sedan performs strongly on **revenue per completed ride**.

---

# 💳 Payment Analysis

## Most Popular Payment Method

**UPI**

* Completed bookings: **41,834**
* Share of completed bookings: **~45%**

UPI is the dominant payment method among completed Uber rides.

---

## 🥈 Second-Highest Revenue Payment Method

**Cash**

* Revenue: **~₹11.76M**
* Revenue contribution: **~24.9%**

This demonstrates the importance of maintaining both digital and cash payment options.

---

# 👥 Customer Analysis

Customer behavior was segmented according to completed ride frequency.

### Customer Segments

```text
1 Ride        → First-time
2 Rides       → Return Customer
3–5 Rides     → Regular Customer
6+ Rides      → Other / Highly Active
```

---

## 🏆 Highest-Revenue Customer Segment

**First-time riders**

> **~51.3% of completed revenue**

This is a significant finding because first-time customers represent a major portion of Uber's revenue in this dataset.

### Business Opportunity

The next opportunity is to convert first-time customers into repeat customers through:

* Loyalty programs
* Personalized offers
* Ride credits
* Referral programs
* Targeted promotions

---

# 🔁 Regular Customer Value

Customers completing **3–5 rides** contribute approximately:

> **~36.6% of completed revenue**

This makes customer retention an important revenue-growth opportunity.

### Business Question

> How can Uber convert first-time riders into regular customers?

This is one of the key strategic questions identified through the analysis.

---

# 📅 Time Analysis

## 🥇 Highest-Revenue Month

**March**

> **~₹4.17M**

---

## 📉 Lowest-Revenue Month

**August**

> **~₹3.87M**

The difference between the strongest and weakest months was further investigated using:

* Completed bookings
* Average booking value
* Driver cancellations
* Customer cancellations
* No-driver-found bookings
* Vehicle performance

This helps move the analysis beyond:

> "August had the lowest revenue."

toward:

> "What operational factors contributed to the weaker performance?"

---

# 🕐 Peak Demand

## Highest-Demand Hour

**6 PM**

> **7,617 completed rides**

This indicates a strong evening demand period.

### Business Opportunity

Uber could use this information to improve:

* Driver allocation
* Dynamic pricing
* Driver incentives
* Supply planning
* Peak-hour availability

---

# 📍 Location Analysis

## Highest-Revenue Drop Location

**Narsinghpur**

* Revenue: **~₹325K**
* Average booking value: **~₹567**

---

## Highest-Volume Pickup Location

**Barakhamba Road**

* Completed rides: **594**
* Revenue: **~₹310K**

These locations can be used to identify areas where additional driver supply or targeted incentives could improve service availability.

---

# 🚨 Cancellation Analysis

One of the most important findings of the project:

| Cancellation Type     |   Bookings | Percentage |
| --------------------- | ---------: | ---------: |
| Driver Cancellation   | **27,000** |    **18%** |
| Customer Cancellation | **10,500** |     **7%** |

### Key Insight

Driver cancellations are more than **2.5×** customer cancellations.

This makes driver-side cancellation reduction one of the strongest opportunities identified in the analysis.

---

# 🚗 No Driver Found

> **10,500 bookings**

Approximately:

> **7% of all bookings**

were lost because no driver was available.

This represents a major operational problem because these bookings potentially represent **lost revenue opportunities**.

Further analysis was performed by:

* Vehicle type
* Pickup location
* No-driver-found rate

---

# ⚠️ Incomplete Bookings

> **9,000 bookings**

Approximately:

> **6% of all bookings**

were incomplete.

### Main Reasons

| Reason            | Approx. Count |
| ----------------- | ------------: |
| Customer Demand   |     **3,040** |
| Vehicle Breakdown |     **3,012** |
| Other Issue       |     **2,948** |

This indicates that incomplete bookings are caused by multiple operational factors rather than one single issue.

---

# 📊 Power BI Dashboard

The SQL analysis was converted into an interactive **Power BI dashboard** to make the insights easier for business stakeholders to understand.

### Dashboard Includes

* Total Bookings
* Completed Rides
* Completion Rate
* Revenue
* Driver Cancellation Rate
* Customer Cancellation Rate
* No Driver Found
* Revenue by Vehicle Type
* Revenue by Payment Method
* Monthly Revenue Trends
* Peak Demand Hours
* Pickup Location Analysis
* Drop Location Analysis
* Booking Status Distribution
* Customer Segment Analysis

### Dashboard Preview

> Add your Power BI dashboard screenshot here.

```markdown
![Uber Power BI Dashboard](images/uber_dashboard.png)
```

---

# 💡 Key Business Insights

### 1️⃣ Driver cancellations are the biggest booking-loss problem

**18% of all bookings** were cancelled by drivers.

This is significantly higher than the **7% customer cancellation rate**.

---

### 2️⃣ Uber completed only 62% of total bookings

Out of:

**150,000 bookings**

only:

**93,000 bookings**

were successfully completed.

This means a significant portion of demand does not convert into completed rides.

---

### 3️⃣ Driver availability is a major opportunity

**10,500 bookings** were lost because no driver was found.

Improving driver availability could directly increase completed rides and revenue.

---

### 4️⃣ Auto is the largest revenue contributor

Auto generated approximately:

> **₹11.73M**

or:

> **~24.8% of completed revenue**

---

### 5️⃣ Go Sedan has strong revenue efficiency

Go Sedan achieved approximately:

> **₹19.71/km**

and:

> **₹512 average booking value**

This indicates strong revenue efficiency despite not being the largest total-revenue vehicle.

---

### 6️⃣ Evening demand is extremely important

6 PM recorded:

> **7,617 completed rides**

This creates an opportunity for targeted driver incentives during peak demand.

---

### 7️⃣ Customer retention represents a major opportunity

First-time customers contribute approximately:

> **51.3% of completed revenue**

while regular 3–5 ride customers contribute:

> **36.6%**

Converting first-time riders into repeat customers could create a strong long-term revenue opportunity.

---

# 🚀 Business Recommendations

## Recommendation 1 — Reduce Driver Cancellations

### Problem

Driver cancellations account for:

> **27,000 bookings / 18%**

### What Uber Should Do

* Identify the most common reasons for driver cancellations
* Introduce targeted driver incentives
* Improve driver-trip matching
* Monitor cancellation behavior by driver and location
* Penalize repeated unjustified cancellations
* Provide better trip information before acceptance

### Expected Business Impact

Reducing driver cancellations can increase:

* Completed rides
* Driver utilization
* Customer satisfaction
* Revenue

---

# Recommendation 2 — Improve Driver Availability

### Problem

**10,500 bookings** were lost because no driver was found.

### What Uber Should Do

Focus additional driver supply around:

* High-demand locations
* 6 PM peak hours
* High no-driver-found locations
* High-volume pickup areas

Use demand forecasting to move driver supply before demand peaks.

### Expected Business Impact

Better driver availability can increase:

**Bookings → Completed Rides → Revenue**

---

# Recommendation 3 — Convert First-Time Riders into Regular Customers

### Problem

First-time riders contribute approximately:

> **51.3% of completed revenue**

but there is a significant opportunity to convert them into repeat users.

### What Uber Should Do

Introduce:

* Second-ride discounts
* Loyalty rewards
* Personalized offers
* Referral incentives
* Ride bundles

### Expected Business Impact

Higher customer retention can increase:

* Customer lifetime value
* Ride frequency
* Revenue
* Long-term customer loyalty

---

# 🧠 SQL Skills Demonstrated

This project demonstrates practical SQL skills including:

### Basic SQL

* `SELECT`
* `WHERE`
* `GROUP BY`
* `ORDER BY`
* `HAVING`
* `LIMIT`

### Aggregations

* `COUNT()`
* `SUM()`
* `AVG()`
* `ROUND()`

### Conditional Logic

* `CASE WHEN`

### Advanced SQL

* Common Table Expressions (`CTE`)
* Window Functions
* `RANK()`
* `SUM() OVER()`
* `RANK() OVER()`
* Percentage calculations
* Multi-level aggregations
* Customer segmentation
* Business KPI calculations

---

# 📁 Project Structure

```text
Uber-Booking-Analytics/
│
├── README.md
│
├── Dataset/
│   └── uber.xlsx
│
├── SQL/
│   └── uber_analysis.sql
│
├── Dashboard/
│   └── Uber_Dashboard.pbix
│
├── Images/
│   └── uber_dashboard.png
│
└── Documentation/
    └── Business_Insights.pdf
```

---

# 📌 Project Outcome

This project demonstrates how raw transactional data can be transformed into **business decisions** using SQL and Power BI.

Instead of only reporting numbers, the analysis identifies:

> **Where Uber is losing bookings → Why it is happening → Where revenue opportunities exist → What the business should do next.**

---

# ⭐ Key Takeaways

| Area                  | Finding             |
| --------------------- | ------------------- |
| Total Bookings        | **150K**            |
| Completion Rate       | **62%**             |
| Driver Cancellation   | **18%**             |
| Customer Cancellation | **7%**              |
| No Driver Found       | **7%**              |
| Incomplete Bookings   | **6%**              |
| Completed Revenue     | **~₹47.26M**        |
| Top Vehicle Revenue   | **Auto**            |
| Best Revenue/km       | **Go Sedan**        |
| Top Payment Method    | **UPI**             |
| Highest Revenue Month | **March**           |
| Lowest Revenue Month  | **August**          |
| Peak Demand           | **6 PM**            |
| Top Drop Location     | **Narsinghpur**     |
| Top Pickup Location   | **Barakhamba Road** |

---

# 👨‍💻 Skills Demonstrated

**SQL • MySQL • Power BI • Data Analysis • Business Intelligence • Data Visualization • KPI Development • Customer Segmentation • Revenue Analysis • Operational Analytics • Window Functions • CTEs • Business Storytelling**

---

# 📬 Contact

If you are a recruiter, hiring manager, or data professional and would like to discuss this project or my analytical approach, feel free to connect with me on LinkedIn.

**Open to Data Analyst / Business Analyst opportunities.**

---

### ⭐ If you found this project interesting, consider giving the repository a star!

