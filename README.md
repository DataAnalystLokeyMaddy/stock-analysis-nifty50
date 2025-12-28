# 📊 Stock Analysis Dashboard

## Overview

This project is an end-to-end **data analytics pipeline** that starts from raw stock data processing in **Python**, serves insights via **Streamlit**, stores and manages data using **MySQL (XAMPP)**, and delivers interactive business insights through **Power BI**.

The goal is to demonstrate a **realistic analyst workflow**: data cleaning → storage → querying → visualization.

---

## 🧱 Tech Stack

* **Python** – Data extraction, cleaning, transformation
* **Pandas / NumPy** – Data manipulation
* **Streamlit** – Lightweight app for preview & logic validation
* **MySQL (XAMPP)** – Relational database storage
* **Power BI** – Final analytics & dashboarding

---

## 📁 Project Structure

```
stock_analysis_project/
├── data/
│   ├── raw_yaml/          # Raw downloaded stock data
│   ├── processed_csv/     # Cleaned CSV outputs
│   └── sector_data.csv    # Sector mapping (optional)
│
├── scripts/
│   ├── 01_yaml_extraction.py
│   ├── 02_data_cleaning.py
│   ├── 03_database_load.py
│
├── streamlit_app/
│   └── app.py
│
├── sql/
│   └── table_schema.sql
│
└── README.md
```

---

## 🔄 Data Flow (Step-by-Step)

### 1️⃣ Data Extraction (Python)

* Raw stock data is extracted from YAML files
* Key fields retained: `date`, `ticker`, `open`, `high`, `low`, `close`, `volume`
* Converted into structured CSV format

### 2️⃣ Data Cleaning & Transformation

* Date standardization
* Null value handling
* Numeric column validation
* Feature readiness for analytics

Output → **Processed CSV files**

---

### 3️⃣ Database Layer (MySQL via XAMPP)

* MySQL server managed using **XAMPP**
* Tables created using defined schema
* Cleaned CSV data loaded into MySQL
* Enables structured querying and scalability

---

### 4️⃣ Streamlit (Validation & Exploration)

* Used as a **development & validation layer**
* Confirms:

  * Data correctness
  * Aggregations (Avg Close, Returns)
  * Filtering logic
* Acts as a quick UI before Power BI

---

### 5️⃣ Power BI Integration

* Connected to MySQL using **MySQL ODBC Connector (64-bit)**
* Import mode used for performance
* Measures and visuals created using Power BI

#### Key Visuals:

* 📈 **Line Chart** – Avg Close Price over Time

  * X-axis: Date
  * Y-axis: Average of Close
  * Legend: Ticker
  * Limited to **Top 5 Tickers** for clarity

* 📊 Bar Charts – Returns / Volume comparisons

* 🎛️ Slicers – Date range, ticker selection

---

## 🎯 Design Decisions

* **Top 5 ticker limit** to reduce visual clutter
* Page-level headings for clarity and storytelling
* Clean axis titles and descriptive chart titles
* Power BI used as the *final presentation layer*

---

## ✅ Key Learnings Demonstrated

* End-to-end ETL thinking
* SQL + BI integration
* Data modeling awareness
* Visual clarity & dashboard best practices
* Real-world analyst workflow

---

## 🚀 Future Improvements

* Add calculated returns in SQL
* Enable dynamic Top N selection
* Automate data refresh
* Add sector-level analysis

---

## 🧠 Conclusion

This project proves hands-on capability across **Python, SQL, Streamlit, and Power BI**, showing not just tools—but **analytical thinking and data storytelling**.
