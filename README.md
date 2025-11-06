# 🚛 Logistics & Operations Dashboard – Looker Studio

![Status](https://img.shields.io/badge/status-completed-brightgreen)
![Tool](https://img.shields.io/badge/Google%20Looker%20Studio-blue)
![Language](https://img.shields.io/badge/Language-English-lightgrey)

This project presents an interactive dashboard built in **Google Looker Studio** to analyze logistics performance, delivery volume, operational costs, and carrier efficiency over time.

---

## 🎯 Objective

The goal of this dashboard is to provide a clear and data-driven view of delivery operations, allowing business users to:

- Monitor delivery **volume and costs**
- Track the **average delivery time**
- Measure the **on-time delivery rate**
- Compare performance across different **carriers**

---

## 📊 Key Metrics

| KPI | Description |
| --- | --- |
| **Total Shipments** | Total number of deliveries in the selected period |
| **Total Cost (R$)** | Total operational cost of shipments |
| **Average Delivery Time** | Mean time between shipment and delivery |
| **% On-Time Deliveries** | Percentage of deliveries completed within SLA |

---

## 📈 Dashboard Overview

The dashboard contains three main visual sections:

1. **Shipments by Carrier** – Bar chart comparing the number of deliveries by carrier.  
2. **Delivery Volume by Date** – Line chart showing shipment trends over time (with moving average applied).  
3. **Delivery Status Distribution** – Donut chart breaking down deliveries by status (delivered, delayed, in transit, canceled).

---

## 🧭 Filters

Users can interact with the dashboard using:

- **Carrier filter** (`transportadora`)  
- **Status filter** (`status`)  
- **Date range selector** (`data_envio`)

---

## 💡 Insights

- Identify which **carriers** have better on-time performance.  
- Highlight periods with **delivery peaks or delays**.  
- Enable quick tracking of **operational costs** and **average delivery efficiency**.  

---

## 🖼️ Screenshot

<p align="center">
  <img src="imagens/dashboard_operacoes_logistica.png.png" alt="Logistics Dashboard" width="800">
</p>

---

## 🧰 Tools & Technologies

- **Google Looker Studio** – Data visualization and analytics  
- **Google Sheets / CSV** – Data source  
- **Dataset fields:** `data_envio`, `data_entrega`, `transportadora`, `status`, `custo`, `prazo_dias`, etc.  

---

## 🔗 Live Dashboard

👉 [**View the dashboard in Looker Studio**](https://lookerstudio.google.com/reporting/1e8dc6c4-17dc-470e-af61-d90ab20dd432)

---

## 👤 Author

**Daniel Gomes de Oliveira**  
_Data & Analytics Consultant | BI | ETL | Cloud | Python_  
📍 São Paulo, Brazil  

💼 [Upwork Profile](#)  
“Data-driven insights for smarter decisions.”

---

## 📂 Repository Structure



