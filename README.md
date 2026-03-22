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

## ⚙️ CALCULATED FIELDS & MEASURES  

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


