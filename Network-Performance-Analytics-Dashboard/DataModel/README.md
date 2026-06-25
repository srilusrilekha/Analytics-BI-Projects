# Data Model & Solution Architecture

This folder provides an overview of the end-to-end reporting architecture, data modeling approach, and Power BI solution design used to support operational analytics and monitoring.

---

## 1. Solution Architecture

**File:** `1_Solution_Architecture.png`

### Purpose

Illustrates the end-to-end data flow from source systems to Power BI dashboards.

### Highlights

* Data sourced from enterprise monitoring and service management platforms.
* Data consolidated into Azure SQL Database.
* SQL queries used for data extraction.
* Data transformation and modeling performed using Power Query.
* Interactive dashboards developed in Power BI.
* Scheduled data refresh supports operational reporting.

---

## 2. Simplified Enterprise Data Model

**File:** `2_Simplified_Enterprise_Data_Model.png`

### Purpose

Provides a high-level representation of the reporting model used to support multiple operational dashboards.

### Highlights

* Hybrid dimensional data model combining Star and Snowflake design principles.
* Shared dimensions for Date, Location, Node, and Assignment Group.
* Integrated reporting across Service Management, Network Performance, Device Inventory, and Operational Metrics.
* Designed to support cross-functional reporting and drill-through analysis.
* Simplified for easier understanding of the overall solution architecture.

### Modeling Approach

This solution utilizes a **Hybrid Data Model** combining both Star and Snowflake design principles.

#### Why a Hybrid Model?

The reporting solution supports multiple operational domains, including:

* Network Performance
* Device Inventory
* Incident Management
* Change Management
* Problem Management
* SLA Monitoring

A hybrid approach was adopted to:

* Support multiple fact tables across different business processes.
* Enable shared dimensions such as Date, Location, Node, and Assignment Group.
* Improve model reusability across multiple dashboards.
* Maintain reporting performance while reducing data redundancy.
* Provide a scalable foundation for future reporting requirements.

This design enables a single Power BI semantic model to support multiple operational dashboards while ensuring consistency, flexibility, and maintainability.

---

## 3. Original Data Model (Sanitized)

**File:** `3_Original_Data_Model_Sanitized.png`

### Purpose

Shows the actual Power BI data model structure used within the reporting solution.

### Highlights

* Multiple fact and dimension tables supporting operational analytics.
* Relationships optimized for reporting and dashboard performance.
* Supports multiple dashboard pages and reporting use cases.
* Presented in a sanitized format to protect confidential business information.

---

## Technologies Used

* Power BI
* Power Query
* DAX
* Azure SQL Database
* SQL
* ServiceNow
* SolarWinds

---

## Confidentiality Notice

The original production data model has been sanitized to protect confidential client information. Sensitive identifiers, proprietary details, and client-specific information have been masked or anonymized. These artifacts are shared solely to demonstrate solution architecture, data modeling practices, and reporting design.
