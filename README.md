# Laptops Market Intelligence: AI-Powered ETL & Analytics Dashboard

<img width="1170" height="635" alt="Top-10-Laptop-Brands" src="https://github.com/user-attachments/assets/d968e0a8-5625-47c2-8332-eb3e9e2a379b" />


## Project Overview
An end-to-end data pipeline designed to automate market research for laptops on Amazon. This project leverages an **AI-powered ETL pipeline** using **n8n** to extract product specifications without visiting individual listing pages, stores the structured data in **Google BigQuery** and **Google Sheets**, and presents real-time market insights via an interactive **Looker Studio** dashboard.

---

## End-to-End System Architecture

![Pipeline Architecture Overview](YOUR_PIPELINE_FLOW_IMAGE_URL_HERE)

---

## Tech Stack & Tools
* **Workflow Automation:** n8n
* **AI & Parsing Engine:** LLM / AI Extractor Node (Zero-shot text extraction), JavaScript, HTML Parsing
* **Data Storage & Data Warehouse:** Google Sheets, Google BigQuery (SQL)
* **Data Visualization:** Looker Studio (Calculated Fields, Custom KPIs & Dynamic Rules)

---

## Data Pipeline Steps

### 1. Extraction & AI Processing
* Automated looping through Amazon search results pages using n8n.
* **AI Node Extraction:** Used an LLM Node directly on the search results text to extract complex laptop attributes (Brand, Processor, RAM, Storage, Screen Size, Price, Rating) without navigating into each individual product detail page—significantly reducing execution time and network overhead.

### 2. Transformation & Loading
* Cleaned and cast raw values into standardized numeric and categorical formats.
* Dynamically routed structured data to both **Google Sheets** for quick audit logs and **Google BigQuery** for scalable analytics.

### 3. Analytics & Visualization
* Built custom metrics including `Stock Availability %`, `Rating Tiers`, and RAM vs. Price correlation charts in **Looker Studio**.

---

## Project Showcase & Screenshots

### 1. n8n Automation Workflow
<img width="1277" height="675" alt="Scraping + Automation" src="https://github.com/user-attachments/assets/c15f5752-f3df-40a0-9e72-35527bf30ad8" />

---

### 2. Data Storage & Warehouse

#### Google Sheets (Staging Layer)
<img width="1280" height="909" alt="Google Sheet Data" src="https://github.com/user-attachments/assets/0c2a1fd9-e336-41bc-a6ee-56ec232d0b0f" />


#### Google BigQuery (Analytical Storage)

<img width="1280" height="908" alt="T-SQL Code on PigQuery" src="https://github.com/user-attachments/assets/df5560d9-748a-468d-b400-8da3cd79df7e" />

<img width="1280" height="910" alt="PiqQuery" src="https://github.com/user-attachments/assets/96c6558c-1a45-4eb4-b795-066cb1496ebe" />

---

### 📈 3. Looker Studio Interactive Dashboards

#### Overview & Market KPIs Dashboard
<img width="902" height="679" alt="Genral Overview Dashboard" src="https://github.com/user-attachments/assets/9b43a649-c0b3-45bd-b52c-a39b228226fe" />


#### Rating & Hardware Correlation Dashboard
<img width="1082" height="814" alt="Rating Dashboard" src="https://github.com/user-attachments/assets/8844a463-d1a1-4ec3-8ea1-dd44da7714d0" />

---

## 💼 Key Business Value
* **Efficiency:** AI-powered extraction eliminated the need for deep web scraping (saving ~80% of execution time).
* **Automated Pipeline:** Zero manual intervention required from raw data extraction to dashboard updates.
* **Market Intelligence:** Provides instant visibility into laptop pricing trends, stock availability, and hardware-to-rating correlations.
