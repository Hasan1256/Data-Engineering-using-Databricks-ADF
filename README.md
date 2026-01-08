# Data-Engineering-using-Databricks-ADF


## 📌 Overview
This project is a **real-time, production-grade implementation** of an end-to-end **Azure Databricks pipeline**. It demonstrates how to ingest, transform, and serve data using the **Medallion Architecture (Bronze → Silver → Gold)** while incorporating **streaming, data governance, and advanced transformations**.  

The project is designed to help data engineers gain **hands-on mastery** over Databricks features including **Unity Catalog, Delta Live Tables, Slowly Changing Dimensions (Type 1 & 2), PySpark transformations, and Auto Loader for incremental ingestion**.  

---

## ⚙️ Architecture

**Medallion Architecture (Lakehouse):**

- **Bronze Layer**
  - Incremental ingestion using **Databricks Auto Loader** (`cloudFiles`)  
  - Underlying **Spark Structured Streaming** for continuous processing  
  - **Idempotency** to ensure exactly-once processing  
  - Data stored in **Parquet (columnar) format**  

- **Silver Layer**
  - Data cleaning and transformations using **PySpark functions**  
  - Incorporation of **Python OOP principles** within PySpark code  
  - Reusable **Unity Catalog functions** for standardization  
  - Data written and stored in **Delta format**  

- **Gold Layer**
  - **Star Schema modeling** (Fact & Dimension tables)  
  - **Slowly Changing Dimensions (SCD):**
    - **Type 1** – implemented via PySpark  
    - **Type 2** – implemented using **Delta Live Tables (DLT)**  
  - Data prepared for analytics and reporting in **Delta tables**  

---

## 📊 Dataset

- Retail dataset with **Orders, Customers, Products, and Regions**  
- Converted into **Parquet format** for efficiency  
- Supports **incremental ingestion** for simulating real-world streaming flows  

---

## 🚀 Features Covered

- ✅ Creation of **Azure Data Lake Storage (ADLS Gen2)** & containers  
- ✅ **Databricks Workspace** setup and connector configuration  
- ✅ **Unity Catalog & Metastore** for centralized governance  
- ✅ **External Data Locations** for Bronze, Silver, Gold, and Source layers  
- ✅ **Databricks Auto Loader** for automated, incremental ingestion  
- ✅ **Delta Tables** in Silver and Gold layers for reliable storage  
- ✅ **Delta Live Tables (DLT)** for automated pipeline orchestration  
- ✅ **Star Schema + Slowly Changing Dimensions (SCD 1 & 2)**  
- ✅ **End-to-End Real-Time Data Engineering Flow**  

---

## 🛠️ Technologies Used

- **Azure Databricks** (Spark, SQL, Auto Loader, Unity Catalog, DLT)  
- **Azure Data Lake Storage (ADLS Gen2)**  
- **Azure Resource Groups & Access Connectors**  
- **PySpark (with OOP concepts)**  
- **Delta Lake & Delta Live Tables**  

---

## 🔧 Setup Instructions

1. **Prerequisites**
   - Azure Free Account (with $200 credits)
   - Databricks Workspace (Trial Premium enabled)
   - Basic familiarity with Python/PySpark

2. **Environment Setup**
   - Create an **Azure Resource Group**
   - Provision **Storage Account (ADLS Gen2)** and configure containers:
     - `source/`, `bronze/`, `silver/`, `gold/`
   - Upload incremental **Parquet files** (`orders`, `customers`, `products`, `regions`)

3. **Databricks Setup**
   - Create **Databricks Workspace** and **Access Connector**
   - Configure **Unity Catalog + Metastore**
   - Register **External Locations** for each layer

4. **Pipeline Development**
   - Bronze Layer: Incremental ingestion using **Auto Loader + Spark Structured Streaming** (Parquet)
   - Silver Layer: Data transformation + Unity Catalog functions, written to **Delta format**
   - Gold Layer: Star schema + SCD handling + Delta Live Tables, stored as **Delta tables**

---

## 📈 Results

- Fully functional **Lakehouse pipeline** simulating real-world scenarios  
- **Star Schema** with SCD1 & SCD2 for analytics  
- Covers **real-time + batch ingestion** with governance and optimization  

---

## 🔮 Future Enhancements

- Add **CI/CD automation** for pipeline deployment  
- Integrate **Databricks Workflow Orchestration** with ADF/Airflow  
- Implement **advanced performance tuning** (Z-Ordering, Optimize, Caching)  
- Expand dataset with **IoT/Streaming telemetry data** for scalability testing  
