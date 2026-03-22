# 📌 Project Title  
🚆 Rail Operations Performance Analysis  

# 📌 Introduction  
This project analyzes rail transport operational and ticket sales data to understand passenger behavior, revenue performance, and system efficiency. Using Power BI, the dashboard provides insights into passenger traffic trends, route profitability, station activity, and payment behavior.  

The analysis objectives include:
- Analyze passenger traffic patterns across days and time periods  
- Evaluate revenue performance by routes and ticket types  
- Identify peak travel periods for operational planning  
- Determine high-traffic stations  
- Understand customer payment preferences  
- Provide actionable insights for improving rail operations  

---

# 📂 Data Cleaning & Preparation  

The dataset consists of multiple relational tables:

- Rail Traffic Fact Table  
- Ticket Sales Fact Table  
- Stations Dimension  
- Routes Dimension  
- Trains Dimension  
- Fare Pricing Dimension  
- Payment Methods Dimension  

All tables were imported into **Power BI**, and relationships were created to form a structured data model.

---

## 🧹 Data Cleaning Overview  

| Step | Description | Action Taken |
|------|-------------|--------------|
| Data Import | Loaded datasets into Power BI | Imported all fact and dimension tables |
| Removed Duplicates | Eliminated duplicate records | Ensured uniqueness in relevant tables |
| Checked for Blanks | Ensured data completeness | Verified no missing values in key columns |
| Data Type Validation | Ensured correct formats | Adjusted numeric, date, and categorical fields |
| Data Modeling | Established relationships | Created relationships between fact and dimension tables |

---

## ⚙️ Calculated Fields & Measures

To support analysis and dashboard visuals, several DAX measures and columns were created:

### 📊 Key Measures  

- **Total Revenue** = SUM('Ticket Sales Fact Table'[Revenue])  
- **Total Passengers** = SUM('Ticket Sales Fact Table'[Passengers])  
- **Total Transactions** = COUNT('Ticket Sales Fact Table'[Transaction ID])  
- **Revenue per Passenger** = DIVIDE([Total Revenue], [Total Passengers] * 100)  

---

### 🧮 Calculated Columns  

- **Hour Column**  
  Extracted from the transaction datetime to analyze hourly trends  

- **Time Category**  
  Categorized hours into:
  - Morning  
  - Afternoon  
  - Evening  
  - Midnight  

These calculated fields enabled **passenger trend analysis, peak period identification, revenue evaluation, and operational insights** across routes, stations, and time periods.

---

## 🔧 Data Transformation Tools Used  

During the data preparation and transformation stage, the following tools were used to clean, format, and prepare the dataset for analysis:

| Tool / Platform | Purpose | Key Actions Performed |
|-----------------|---------|---------------------|
| **Power Query (Power BI)** | Data cleaning and transformation | Removed duplicates, checked for blanks, validated data types |
| **DAX (Power BI)** | Advanced calculations | Created revenue metrics, passenger measures, and time-based columns (Hour, Time Category) |
| **Power BI** | Data modeling & visualization | Built relationships between tables and designed interactive dashboard |
| **GitHub** | Version control and documentation | Stored project files and documented analysis process |

---

These tools helped streamline **data import, cleaning, modeling, analysis, and visualization** throughout the project lifecycle.

---

## 🔍 Exploratory Data Analysis (EDA)

EDA was conducted to **understand passenger behavior, traffic patterns, and revenue distribution** before deeper analysis.

### 📊 Areas Explored

| Analysis Area | Focus |
|---------------|--------|
| Overall Performance | Evaluated total revenue, passengers, and transactions |
| Passenger Traffic Trends | Analyzed passenger movement by day and time category |
| Route Performance | Compared revenue and passenger volume across routes |
| Station Analysis | Identified high-traffic stations |
| Payment Behavior | Examined distribution of payment methods |
| Time-Based Trends | Analyzed hourly demand using derived time categories |

EDA helped shape **dashboard design, KPI selection, and analytical focus**.

---

## 📊 Statistical Analysis

To complement EDA, **quantitative metrics and comparisons** were calculated to measure operational and revenue performance.

### 🔢 Methods Applied

| Method | Purpose |
|--------|---------|
| Aggregation Analysis | Calculated totals for revenue, passengers, and transactions |
| Contribution Analysis | Evaluated revenue contribution by routes and ticket types |
| Time-Based Analysis | Compared passenger demand across different time categories |
| Distribution Analysis | Assessed how passengers and payments are distributed |

---

### 📐 Metrics Evaluated  

- Total Revenue  
- Total Passengers  
- Total Transactions  
- Revenue per Passenger  
- Passenger Distribution by Time Category  
- Revenue Contribution by Route  

This approach **quantified passenger demand patterns, evaluated revenue efficiency, and enabled data-driven operational decisions**, complementing the visual insights identified during EDA.

---

## 📈 Overall Performance

The rail network demonstrates **stable passenger demand, strong route-level performance, and balanced system usage** across stations and payment channels.

| Metric | Value | Notes |
|--------|-------|-------|
| **Busiest Day** | Tuesday (91,843 passengers) | Highest traffic across all time periods |
| **Peak Demand Period** | Morning (~30K+ passengers) | Consistent across all days |
| **Top Revenue Route** | Metro Rapid ($360.9K) | Highest revenue generator |
| **Top Stations** | University & South Gate (~26K passengers each) | Major passenger hubs |
| **Payment Distribution** | 25% each across all methods | Fully balanced usage |
| **Top Ticket Type** | Adult Tickets ($1,606.3K) | Primary revenue contributor |
| **Volume vs Revenue Insight** | Mismatch observed | High passengers ≠ high revenue |

---

This overview highlights key performance drivers and sets the foundation for deeper operational insights.

---

## 💡 Insights & Recommendations

### 📊 Demand & Time-Based Insights  

| Insight | Details |
|--------|--------|
| **Peak Demand** | Morning period dominates across all days |
| **Daily Trend** | Tuesday records the highest passenger traffic (91,843) |
| **Demand Pattern** | Over 50% higher traffic in the morning compared to other periods |

**Recommendation:**  
- Increase train frequency during morning peak hours  
- Allocate more staff to manage high passenger flow  

---

### 🚆 Route Performance Insights  

| Insight | Details |
|--------|--------|
| **Top Route** | Metro Rapid generates the highest revenue ($360.9K) |
| **Efficiency Gap** | Tech Corridor has highest passengers but ranks lower in revenue |
| **Low Revenue Route** | North Line has high volume but lowest revenue (~$135K) |

**Recommendation:**  
- Analyze **revenue per passenger** across routes  
- Improve pricing or service models on underperforming routes  
- Replicate Metro Rapid’s pricing or efficiency strategy  

---

### 🏙️ Station Insights  

| Insight | Details |
|--------|--------|
| **Top Stations** | University and South Gate handle the highest passenger traffic |
| **Distribution** | Passenger load is relatively balanced across all stations |

**Recommendation:**  
- Optimize operations at high-traffic stations  
- Improve passenger flow management and infrastructure  

---

### 💳 Payment Behavior Insights  

| Insight | Details |
|--------|--------|
| **Balanced Usage** | All payment methods account for 25% each |
| **System Risk** | Failure of one channel affects 25% of transactions |

**Recommendation:**  
- Ensure reliability across all payment systems  
- Implement backup systems to prevent revenue loss  

---

### 🎟️ Ticket Revenue Insights  

| Insight | Details |
|--------|--------|
| **Top Contributor** | Adult tickets generate ~$1.6M (~70% of revenue) |
| **Lower Segments** | Senior and Child tickets contribute significantly less |

**Recommendation:**  
- Focus marketing efforts on adult commuters  
- Introduce loyalty programs for frequent travelers  

---

## 🚀 Final Takeaway  

The analysis reveals that **passenger demand is driven by morning commuter patterns, while revenue performance varies significantly across routes due to pricing and usage differences**.  

Optimizing peak-hour operations, improving underperforming routes, and leveraging high-efficiency routes like Metro Rapid can significantly enhance overall system performance.

---

## 📊 Main Dashboard

<img width="1364" height="764" alt="image" src="https://github.com/user-attachments/assets/71ad935a-da87-426e-815b-83996e270cfb" />

