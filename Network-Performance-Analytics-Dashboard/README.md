# Network Operations Analytics Dashboard

## Project Overview

This project delivers a centralized Power BI reporting solution designed to provide visibility into network performance, availability, capacity utilization, service management operations, and infrastructure health across multiple geographic locations.

The solution integrates operational data from enterprise monitoring and service management platforms into a unified reporting layer, enabling stakeholders to monitor network health, identify trends, and make data-driven decisions through interactive dashboards.

---

## Business Problem

Network Operations teams relied on multiple systems to monitor infrastructure performance and service management activities. This created challenges in obtaining a consolidated view of network health and operational metrics.

Key challenges included:

* Limited visibility into network performance, availability, and capacity metrics.
* Difficulty correlating network incidents with service availability and performance degradation.
* Lack of centralized reporting across multiple locations and network sites.
* Manual effort required to gather and consolidate operational data from different platforms.
* Limited visibility into Incident, Problem, Change, and SLA management activities.

---

## Solution Overview

A centralized Power BI solution was developed to consolidate operational data from multiple enterprise systems into a single reporting platform.

The solution provides:

* Executive-level operational visibility
* Network performance monitoring
* Critical site monitoring
* Service Management reporting
* Interactive drill-through analysis
* Daily operational monitoring dashboards

---

## Solution Architecture

The solution integrates data from multiple enterprise platforms into Azure SQL Database, where reporting datasets are prepared using SQL queries. Data transformation and modeling are performed using Power Query, and interactive dashboards are delivered through Power BI.

### Data Sources

* SolarWinds
* ServiceNow
* Azure SQL Database

For detailed architecture, refer to:

* `Data_Model/1_Solution_Architecture.png`

---

## Data Modeling Approach

The solution utilizes a **Hybrid Data Model** combining both Star and Snowflake design principles.

### Why a Hybrid Model?

The reporting solution supports multiple operational domains, including:

Network Performance
Device Inventory
Incident Management
Change Management
Problem Management
SLA Monitoring

A hybrid approach was adopted to:

* Support multiple fact tables across different business processes.
* Enable shared dimensions such as Date, Location, Node, and Assignment Group.
* Improve model reusability across dashboards.
* Maintain reporting performance while reducing data redundancy and supporting future scalability.

This design enables a single Power BI semantic model to support multiple operational dashboards while ensuring consistency, flexibility, and maintainability.

For additional details, refer to:

* `Data_Model/2_Simplified_Enterprise_Data_Model.png`
* `Data_Model/3_Original_Data_Model_Sanitized.png`

---

## Primary Use Cases

The solution was developed to provide operational visibility across the network landscape and support proactive monitoring.

Key use cases include:

* Download and Upload Traffic Monitoring
* Network Availability Tracking
* Critical Site Monitoring
* Capacity Utilization Monitoring
* Incident Management Reporting
* Problem Management Reporting
* Change Management Reporting
* SLA Compliance Monitoring
* Device Inventory Reporting
* Location-wise Performance Analysis

---

## Key Metrics

### Performance Analytics

* Location-wise Availability
* Critical Site Health
* Capacity Utilization

### ServiceNow Metrics

* Network Devices
* Incidents
* Problems
* Changes
* SLA Breached/Not Breached

### SolarWinds Metrics

* Response Time
* Packet Loss
* Uptime Percentage
* Network Bandwidth Utilization Percentage
* Upload & Download Traffic

---

## Dashboard Portfolio

This repository showcases selected dashboards from the reporting solution:

* Network Cockpit
* Network Performance Dashboard
* Daily Operational Monitoring Report
* Critical Site Monitoring Dashboard
* Drill-through Performance Analysis

### Note

The complete enterprise solution includes additional dashboards and reporting pages that are not included in this repository due to confidentiality requirements. Only a subset of dashboards has been included to demonstrate the overall reporting architecture and analytics capabilities.

---

## Data Refresh & Monitoring

The reporting solution supports scheduled operational reporting through Power BI Dataflows.

### Refresh Schedule

* Dashboard refresh every 12 hours
* Scheduled refresh windows:

  * 07:00 AM EST
  * 07:00 PM EST

### Monitoring & Optimization

To ensure reporting accuracy and reliability:

* Dataflow refreshes are actively monitored.
* Refresh discrepancies are investigated and resolved.
* Dashboard performance is periodically reviewed and optimized.
* Visualizations are continuously enhanced based on business requirements and stakeholder feedback.

---

## My Contributions

I was involved throughout the end-to-end development lifecycle of the reporting solution.

Responsibilities included:

* Business requirement analysis and stakeholder discussions.
* Metrics identification, KPI definition, and validation.
* SQL query development for data extraction from Azure SQL Database.
* Power Query transformations and data preparation.
* Data modeling and relationship design using a Hybrid Data Model.
* DAX measure and calculation development.
* Interactive dashboard and visualization development.
* Dataflow implementation and scheduled refresh management.
* Dashboard performance tuning and optimization.
* Maintaining transparency and consistency in business logic across stakeholders and project teams.
* Stakeholder walkthroughs, dashboard demonstrations, and knowledge transfer sessions.

---

## Technologies Used

* Power BI
* Power Query
* DAX
* SQL
* Azure SQL Database
* ServiceNow
* SolarWinds

---

## Business Impact

The solution delivered significant operational and reporting improvements:

* Centralized reporting across multiple enterprise platforms.
* Improved visibility into network performance, availability, and capacity utilization.
* Faster identification of operational issues and service disruptions.
* Enhanced monitoring of critical sites and infrastructure assets.
* Reduced manual reporting effort through automation.
* Enabled benchmark and percentile-based performance analysis.
* Improved executive and operational decision-making through data-driven insights.

---

## Repository Structure

```text
Enterprise-Network-Operations-Analytics/
│
├── README.md
│
├── Data_Model/
│   ├── README.md
│   ├── 1_Solution_Architecture.png
│   ├── 2_Simplified_Enterprise_Data_Model.png
│   └── 3_Original_Data_Model_Sanitized.png
│
└── Dashboard_Screenshots/
    ├── README.md
    └── Dashboard Images
```

---

## Confidentiality Notice

Client names, proprietary identifiers, operational metadata, and sensitive business information have been intentionally anonymized or obscured to maintain confidentiality and comply with organizational data protection policies. The artifacts in this repository are presented solely to demonstrate solution architecture, data modeling practices, reporting design, and analytics capabilities.

