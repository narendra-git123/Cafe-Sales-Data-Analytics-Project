# Cafe Sales Data Analytics Project

## 📌 1. Project Summary
This project delivers an end-to-end data analytics workflow that transforms a highly corrupted, noisy 10,000-row transactional ledger into an executive-ready reporting system. The pipeline handles programmatic data cleaning, database verification, multi-tab Management Information System (MIS) creation, and a single-page interactive summary dashboard to guide strategic cafe business decisions.

---

## 🛠️ 2. Tech Stack & Purpose
* **Python (Jupyter Notebook):** Used for bulk programmatic data ingestion, error filtering, handling missing values, and Exploratory Data Analysis (EDA).
* **MySQL Workbench:** Used for relational schema creation, pipeline quality control, and secure data storage.
* **Microsoft Excel 2019:** Used for core data filtering, deep-dive pivot analysis, paginated MIS sheet layout, and final executive dashboard design.
* **Git & GitHub:** Used for professional folder structuring, version control, and portfolio deployment.

---

## 🚀 3. Step-by-Step Project Breakdown

### I. Data Cleaning & Exploratory Analysis (Jupyter Notebook)
* **Ingestion:** Processed an initial unrefined dataset of **10,000 records** where all columns were heavily corrupted with string flags like `ERROR` and `UNKNOWN`.
* **ETL Pipeline:** Dropped 460 rows containing unrecoverable chronological date corruption (**4.6% data loss**, staying safely below the standard 5% threshold). 
* **Imputation Logic:** Handled null values systematically—imputed numeric quantities with the **Median**, unit prices with the category-wise **Mode**, and filled missing text entries as `'Not Recorded'`.
* **DataType Enforcement:** Recalculated total spending mathematically ($Quantity \times Unit\ Price$) and converted variables into strict production types, outputting a pristine dataset of **9,540 rows**.
* **Key EDA Discovery:** Uncovered a price-to-quantity correlation of practically zero (**0.0053**), proving customers have zero price sensitivity and buy a rigid baseline average of **3 items per ticket**.

### II. Database Validation (MySQL Workbench)
* **Schema Setup:** Created a localized relational database (`cafe_db`) and constructed explicit tabular templates mapping out the exact cleansed columns.
* **Data Verification:** Imported the **9,540 rows** from Jupyter Notebook into MySQL Workbench to verify data health and structure before running final reports.

### III. Ingestion, MIS Reporting & Dashboard (Excel 2019)
* **Advanced Filtering:** Connected Excel directly to MySQL. Right inside the spreadsheet, filtered out incomplete administrative rows flagged as `'Not Recorded'`, isolating exactly **3,580 high-fidelity rows** containing authentic financial values for active business analysis.
* **MIS Pagination Layout:** Built a professional multi-tab report using a strict **Orange and Dark-Brown color palette** covering `MIS_KPI`, `MIS_Monthly`, `MIS_Product`, and `MIS_Payment`.
* **Key Channel Insights:**
  * **Payment & Location:** Discovered a symmetric 33/33/33 payment method split and a 50/50 In-Store vs. Takeaway split. Average Order Value (AOV) remained uniform across all channels.
  * **Day-Wise Trends:** Sunday drove peak transaction volume, Tuesday attracted the highest-spending premium clients, and Saturday suffered the lowest absolute traffic but yielded high average tickets.
* **Executive Dashboard:** Built a dynamic, single-page dashboard fed entirely by automated cross-sheet references. It features a 5-card KPI summary banner and a 2×2 visual grid detailing monthly trends, top products, payment distributions, and day-wise traffic columns.

---

## 💡 4. Top Strategic Recommendations
1. **The Cookie Price Vector:** Increase Cookie prices from ₹1.00 to ₹1.50 to instantly capture a **50% revenue boost** on this high-velocity item without triggering customer price sensitivity.
2. **The "Never Touch" Core Margin Products:** Protect Salad, Sandwich, and Smoothie lines at all costs—they combine to command **55.5% of total business revenue** and should not be subjected to experimental pricing or bundle deals.
3. **Point-of-Sale (POS) Configuration Update:** Immediately fix the checkout system logs, as **31.6% of payment methods** and **39.6% of locations** went completely unrecorded by the software during transactional processing.

---
**Prepared by:** Narendra Maram  
**Role:** Data Analyst Intern
**Location:** Hyderabad, India