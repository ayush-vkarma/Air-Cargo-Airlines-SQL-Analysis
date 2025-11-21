# ✈️ Air Cargo / Airlines SQL Analysis

![ER Diagram](Documentation/ER_DIAGRAM_AIRLINE_DATABASE.png)

## 🔍 Objective
Design and implement a fully-functional airline database to analyze regular customers, busiest routes and ticket revenue by class and brand. The system demonstrates end-to-end SQL skills including schema design, query development, analytical reporting, stored program units, performance tuning and access control.

## 🧱 Database Schema Overview
The system is centered around four core entities:

| Table | Description |
|-------|-------------|
| `customer` | Passenger demographic information |
| `routes` | Flight route and distance details |
| `passengers_on_flights` | Actual travel and seating information |
| `ticket_details` | Ticket purchase, pricing and brand info |

The ER diagram illustrates direct and indirect relationships between customers, flights, brands, travel segments and ticket sales.

---

## 🗂 Dataset Files
| File | Purpose |
|------|---------|
| `customer.csv` | Customer demographic dataset |
| `routes.csv` | Route and airport distance dataset |
| `passengers_on_flights.csv` | Travel and flight seat dataset |
| `ticket_details.csv` | Ticket purchase dataset |
| `AIRLINES_PROJECT_AYUSH_VISHWAKARMA.csv` | Combined dataset extract |

---

## 🛠 Technologies & SQL Concepts Used
- SQL RDBMS (MySQL-compatible)
- DDL / DML / DCL / TCL
- Joins, grouping, HAVING, IF condition
- Window functions
- ROLLUP for hierarchical aggregation
- Stored procedures & stored function
- View creation
- Cursor
- Indexing and EXPLAIN for performance tuning

---

## 🧩 Major SQL Deliverables Completed

### 🔹 Table Creation & Constraints
- Created `ROUTE_DETAILS` with:
  - `ROUTE_ID` → `PRIMARY KEY` + `UNIQUE`
  - `FLIGHT_NUM` → `CHECK (FLIGHT_NUM > 0)`
  - `DISTANCE_MILES` → `CHECK (DISTANCE_MILES > 0)`

### 🔹 Analytical Queries
- Passengers travelling on **routes 01–25**
- **Passenger count and total revenue** for **Business class**
- **Full customer name** extraction using concatenation
- Customers who **registered AND booked**
- Find customers by **brand** (Emirates)
- Identify **Economy Plus passengers** using `GROUP BY` + `HAVING`
- `IF` logic to check if **revenue crossed 10,000**

### 🔹 Performance Optimization
- Indexing and execution plan analysis (`EXPLAIN`) on queries filtering **route_id = 4**
- Window function for **maximum ticket price per class**
- ROLLUP to compute **total revenue across aircraft IDs per customer**

### 🔹 Stored Programs
| Object Type | Purpose |
|-------------|---------|
| View | All **Business class customers** along with airline brand |
| Stored Procedure 1 | Passenger details for **dynamic route range** (with error handling) |
| Stored Procedure 2 | Routes with **distance > 2000 miles** |
| Stored Procedure 3 | Group routes into **SDT, IDT, LDT** distance categories |
| Function + Procedure | Return complimentary services flag (`Business` & `Economy Plus` = Yes) |
| Cursor | Fetch first customer whose **last name ends with “Scott”** |

---

## 📈 Business Insights Generated
- **Frequent-flyer customers** identified by ticket history can be targeted for loyalty programs.
- **Asia and North America routes** generate the highest traffic and require capacity planning.
- **Business class** produces the highest revenue despite fewer passengers.
- **Complimentary services** directly improve repeat travel probability for premium classes.
- Ticket pricing varies significantly by route distance and brand positioning.

---

## 🚀 Business Impact
This database enables Air Cargo to:
- Improve route-wise aircraft allocation
- Personalize offers based on customer travel frequency
- Optimize pricing and promotional strategy by class and brand
- Strengthen customer experience using service eligibility logic
- Enable scalable automation of airline ops and reporting

---

## ▶️ How to Run
1. Create a database (e.g., `air_cargo_db`)
2. Import the CSV datasets into their respective tables
3. Run the contents of `SQL_Scripts/AIRLINES_PROJECT_AYUSH_VISHWAKARMA.sql`
4. Execute analytical queries, stored procedures and view
5. Optionally run indexed queries and EXPLAIN for performance measurement

---

## 📁 Repository Structure

```text
📦 Air-Cargo-Airlines-SQL-Analysis
├── 📂 Datasets
│   ├── customer.csv
│   ├── routes.csv
│   ├── passengers_on_flights.csv
│   ├── ticket_details.csv
│   └── AIRLINES_PROJECT_AYUSH_VISHWAKARMA.csv
├── 📂 Documentation
│   ├── 1697127212_cep2aircargoanalysisproblemstatement.docx
│   ├── ER_DIAGRAM_AIRLINE_DATABASE.png
│   └── AYUSH_VISHWAKARMA_AIRLINES_PROJECT_ANSWERS.pdf
├── 📂 SQL_Scripts
│   └── AIRLINES_PROJECT_AYUSH_VISHWAKARMA.sql
└── README.md
```
## 👨‍💻 Author

Ayush Vishwakarma — Data Analyst
GitHub Portfolio: https://github.com/ayush-vkarma
LinkedIn: https://www.linkedin.com/in/ayush-d-vishwakarma
