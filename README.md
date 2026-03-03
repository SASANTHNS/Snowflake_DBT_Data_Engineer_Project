# 🏠 Airbnb End-to-End Data Engineering Project

## 📋 Overview

This project implements a complete end-to-end data engineering pipeline for Airbnb data using modern cloud technologies.

The solution demonstrates best practices in:

- Data warehousing
- Data transformation
- Incremental processing
- Slowly Changing Dimensions (SCD Type 2)
- Analytics-ready modeling

The pipeline processes Airbnb listings, bookings, and hosts data using a **Medallion Architecture (Bronze → Silver → Gold)**.

---

# 🏗️ Architecture

## 🔄 Data Flow


Source CSV Files
↓
AWS S3
↓
Snowflake (Staging)
↓
Bronze Layer
↓
Silver Layer
↓
Gold Layer


- **Bronze** → Raw tables
- **Silver** → Cleaned & standardized
- **Gold** → Analytics-ready datasets

---

## 🛠 Technology Stack

| Layer | Tool |
|-------|------|
| Cloud Data Warehouse | Snowflake |
| Transformation | dbt |
| Cloud Storage | AWS S3 |
| Language | Python 3.12+ |
| Version Control | Git |

### Key dbt Features Used

- Incremental models
- Snapshots (SCD Type 2)
- Custom macros
- Jinja templating
- Data tests
- Documentation generation

---

# 📊 Data Model

## 🥉 Bronze Layer (Raw)

Minimal transformation from staging.

- `bronze_bookings`
- `bronze_hosts`
- `bronze_listings`

---

## 🥈 Silver Layer (Cleaned)

Validated and standardized datasets.

- `silver_bookings`
- `silver_hosts`
- `silver_listings`

---

## 🥇 Gold Layer (Analytics-Ready)

Business-optimized models.

- `fact`
- `obt` (One Big Table)
- Ephemeral intermediate models

---

## 🕒 Snapshots (SCD Type 2)

Historical tracking enabled for:

- `dim_bookings`
- `dim_hosts`
- `dim_listings`

Tracks:
- `valid_from`
- `valid_to`
- historical changes


---

# 🚀 Getting Started

## Prerequisites

- Snowflake Account
- AWS Account
- Python 3.12+
- pip or uv

---

## Installation

### 1️⃣ Clone Repository

```bash
git clone <repository-url>
cd AWS_DBT_Snowflake
