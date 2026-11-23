# ROHANA | Pharma Supply Chain Analytics

> One integrated Power BI model, six decisions-focused dashboards, built on 18 tables of a pharmaceutical distribution supply chain (2020–2025).

---

## Project Name

**ROHANA | Pharma Supply Chain Analytics**

---

## Project Idea

A pharmaceutical distributor serves pharmacy chains in **Egypt, Saudi Arabia, the UAE, Jordan and Kuwait**. The data covers the full chain: customer orders, purchase orders, goods receipts, shipments, and inventory.

The project turns **18 raw tables** into one clean data model and **six dashboards**, one per management decision, inside a single Power BI file.

The question that drives the whole project:

> **Why do pharmacies receive only about 6 out of every 10 units they order, and what should be fixed first?**

What the data shows at a glance:

| Metric | Value |
|---|---|
| Ordered value | ~185.2M USD |
| Fulfilled value | ~110.1M USD |
| Unfulfilled value | ~75.1M USD (40.5%) |
| Overall fill rate | ~59.6% |
| Orders fully completed | 4,500 of 29,400 (~15%) |

**Approach**

1. Clean the data and set data types in **Power Query**.
2. Build one star-schema model (`ROHANA_Master.pbix`) shared by the whole team.
3. Each member builds one dashboard (an Overview page) on top of it.
4. Merge all dashboards into the master file and present the insights.

---

## Team Members

| # | Name |
|---|---|
| 1 | Ahmed Gamal |
| 2 | Asmaa Yassin |
| 3 | Ola Mohamed |
| 4 | Reham Hossam |
| 5 | Nader Ghazy |
| 6 | Haidy Essam |

---

## Work Plan

| Phase | What happens | Output |
|---|---|---|
| **1. Data understanding & cleaning** | Review the 18 tables, fix data types, convert date keys to dates, validate keys and relationships (Power Query). | Clean tables |
| **2. Master model** | Build the star schema, mark the date table, create the `_Measures` table, and apply the shared theme. | `ROHANA_Master.pbix` |
| **3. Insights** | Explore the data and extract the key findings for each decision area. | Insight list per dashboard |
| **4. Dashboard development** | Each member builds the Overview page of their own dashboard (insights, DAX measures, chart design). | 6 dashboards (6 pages) |
| **5. Merge & QA** | Merge all pages into the master file, set navigation, sync slicers, and check numbers. | Final Power BI file |
| **6. Presentation & delivery** | Prepare the presentation, the script, and the repository. | Slides + README + files |

**Dashboard standard (every dashboard follows it):**

- 1 page per dashboard
- KPI cards, filters (one of them a date filter), charts
- All amounts in **USD** (using `ExchangeRateToUSD`), all measures in a `_Measures` table
- Same theme, same layout, one insight text box per Overview

---

## Roles & Responsibilities

**By phase**

| Role | Members |
|---|---|
| Data cleaning and data types (Power Query) | Haidy Essam, Reham Hossam |
| Data Modeling (Power BI) | Haidy Essam, Reham Hossam, Ola Mohamed |
| Dashboard development (insights, DAX, design) | Each member on their own dashboard, as listed below |

**By dashboard**

| Owner | Dashboard | Main tables |
|---|---|---|
| Ahmed Gamal | Sales & Demand | `Orders`, `Order_Details` |
| Reham Hossam | Procurement & Suppliers | `Purchase_Orders`, `Purchase_Order_Details` |
| Nader Ghazy | Logistics & Shipments | `Shipments`, `Shipment_Details` |
| Ola Mohamed | Inventory Health | `Inventory_Snapshots`, `Inventory_Movements` |
| Haidy Essam | Quality & Expiry | `Batches`, `Goods_Receipts` |
| Asmaa Yassin | Product & Category Portfolio | `Products`, `Categories` |

The shared dimensions (`Date`, `Locations`, `Products`, `Categories`, `Manufacturers`, `Suppliers`, `Pharmacies`, `Pharmacy_Branches`) are cleaned once and used by everyone.

---

## KPIs

| Dashboard | KPIs |
|---|---|
| **Sales & Demand** | Ordered Value (USD), Fulfilled Value (USD), Unfulfilled Value (USD), Fill Rate %, Completed Orders % |
| **Procurement & Suppliers** | Total PO Value (USD), PO Count, Avg Lead Time, On-Time Delivery %, Cancelled / Pending PO % |
| **Logistics & Shipments** | Total Shipments, On-Time %, Avg Delay Days, Total Freight Cost (USD), Damaged Qty % |
| **Inventory Health** | Closing On-Hand Qty, Inventory Value (USD), Quarantined Qty, Damaged Qty, Write-Off Qty |
| **Quality & Expiry** | Total Batches, Rejected / Quarantined Batches %, Rejection Rate %, Short Delivery %, Batches Expiring in 90 Days |
| **Product & Category Portfolio** | Active Products, Avg Margin %, Rx Share %, Top Category Revenue, Avg Shelf Life |

---

## Instructor

**Name:** Mahmoud Emad

---

## Project Files

```
ROHANA/
├── README.md
├── assets/          # logo, dashboard backgrounds, team photos
├── data/            # the 18 source tables (CSV)
├── docs/            # team guides and documentation
└── presentation/    # slides and speaking script
```

**Data (`data/`)**

- Fact tables: [Orders](data/Orders.csv), [Order_Details](data/Order_Details.csv), [Purchase_Orders](data/Purchase_Orders.csv), [Purchase_Order_Details](data/Purchase_Order_Details.csv), [Goods_Receipts](data/Goods_Receipts.csv), [Shipments](data/Shipments.csv), [Shipment_Details](data/Shipment_Details.csv), [Inventory_Movements](data/Inventory_Movements.csv), [Inventory_Snapshots](data/Inventory_Snapshots.csv)
- Dimensions: [Products](data/Products.csv), [Categories](data/Categories.csv), [Batches](data/Batches.csv), [Manufacturers](data/Manufacturers.csv), [Suppliers](data/Suppliers.csv), [Pharmacies](data/Pharmacies.csv), [Pharmacy_Branches](data/Pharmacy_Branches.csv), [Locations](data/Locations.csv), [Date](data/Date.csv)

**Docs (`docs/`)**

- [Dashboard assignments](docs/ROHANA_Dashboard_Assignments.docx)
- [Power BI team workflow](docs/ROHANA_PowerBI_Team_Workflow.docx)

**Assets (`assets/`)**

- [Dashboard background](assets/ROHANA_BG_Overview.png)

**Power BI & presentation**

- Power BI file: `ROHANA_Master.pbix` (to be added)
- Presentation and script: `presentation/` (to be added)
