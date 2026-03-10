# operational-risk-analytics-dashboard
Power BI dashboard simulating enterprise operational risk reporting including control testing, issue remediation, and audit oversight.
# Operational Risk & Control Monitoring Dashboard (Power BI)

## Overview

This project is a multi-page Power BI dashboard designed to simulate an **Operational Risk and Control Monitoring reporting suite** similar to those used within financial institutions.

The dashboard consolidates information across **risk assessments, control testing, issue remediation, and audit oversight** to provide leadership with a centralized view of operational risk exposure and remediation progress.

The goal of this project was to demonstrate how **data analytics and visualization can support risk governance, oversight, and decision-making**.

---

## Key Features

The dashboard includes five core reporting areas:

### 1. Executive Overview
Provides a high-level snapshot of organizational risk posture including:

- Enterprise Risk Rating
- Control Failures
- Open Issues
- Overdue Issues
- Key trends and distributions across the enterprise

This page serves as the **entry point for executive leadership**.

---

### 2. Issues & Control Monitoring

Tracks operational risk issues and control performance across business units.

Key insights include:

- Enterprise risk rating indicators
- Control exceptions by control type (Preventive / Corrective / Detective)
- Overdue issues by business unit
- Root cause distribution of operational issues
- Detailed issue tracking table

This page supports **second-line risk oversight and issue monitoring**.

---

### 3. Control Effectiveness & Testing

Analyzes results from control testing activities.

Metrics include:

- Total control tests executed
- Control pass rate
- Needs improvement results
- Control failures
- Failure trends over time
- Control failures by business unit

This view helps evaluate **control design and operational effectiveness**.

---

### 4. Issues & Remediation

Focuses on issue lifecycle management and remediation performance.

Key indicators:

- Total issues
- Open vs closed issues
- Average days open
- Issue creation trend
- Overdue issues by business unit
- Recurring issue drivers

This page provides visibility into **remediation progress and operational backlog**.

---

### 5. Audit Oversight

Monitors audit findings and related remediation activity.

Included insights:

- Open audit findings
- Severity distribution of findings
- Audit finding trends over time
- Root causes of audit findings
- High severity findings table with aging indicators

This supports **audit risk oversight and governance reporting**.

---

## Data Model

The dashboard is built using a **star schema model** to support scalable analysis.

### Fact Tables

- `fact_issue` – operational risk issues and remediation tracking
- `fact_control_test` – control testing results
- `fact_rcsa_assessment` – risk and control self-assessment data

### Dimension Tables

- `dim_business_unit`
- `dim_process`
- `dim_control`
- `dim_risk`

This structure enables efficient filtering across **business units, processes, and risk categories**.

---

## Tools Used

- **Power BI Desktop**
- **DAX (Data Analysis Expressions)**
- **Dimensional Data Modeling**
- **Data Visualization Design**

---

## Key DAX Measures

Examples of measures implemented:

```DAX
Failure Rate =
DIVIDE([Failed Controls], [Total Controls])
