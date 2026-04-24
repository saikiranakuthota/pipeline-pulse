# 📡 Pipeline Pulse

> A production-grade AWS data pipeline monitoring dashboard — built as a single-file web app.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-blue?style=for-the-badge&logo=github)](https://saikiranakuthota.github.io/pipeline-pulse)
[![HTML](https://img.shields.io/badge/Built%20With-HTML%2FJS-orange?style=for-the-badge&logo=html5)]()
[![AWS](https://img.shields.io/badge/Simulates-AWS%20Stack-yellow?style=for-the-badge&logo=amazonaws)]()

---

## 🚀 Overview

**Pipeline Pulse** is an interactive AWS Data Engineering operations dashboard that simulates real-time monitoring of a production data platform. It mirrors the exact infrastructure I designed and managed professionally — from S3 ingestion through Glue ETL, Delta Lake, Redshift, and Power BI delivery.

Fully self-contained. No backend. No build tools. Open `index.html` and it runs.

---

## ✨ What's Inside

| Page | Description |
|---|---|
| **Dashboard** | Live pipeline flow animation (REST APIs → S3 → Glue → Delta Lake → Redshift → Power BI), KPI cards updating in real time, throughput charts, and Glue job table |
| **Pipelines** | Full pipeline registry with schedule, SLA, and run status |
| **Data Quality** | Quality score by dimension (completeness, uniqueness, freshness), validation rule pass rates, 14-day trend |
| **Redshift** | Cluster metrics (CPU, storage, QPM), WLM queue utilization, top queries by duration |
| **Airflow DAGs** | 10-run history for each DAG with success/warn/fail color indicators |
| **Logs** | Filterable CloudWatch-style log stream |
| **Cost Monitor** | MTD spend by service, 30-day trend, IaC savings tracker |

---

## 🛠️ AWS Stack Simulated

```
REST APIs / Event Streams
        ↓
   Amazon S3  (raw zone → processed zone → curated zone)
        ↓
  AWS Glue  (PySpark ETL jobs, triggered via Airflow DAGs)
        ↓
  Delta Lake on S3  (ACID-compliant, schema-enforced)
        ↓
  Amazon Redshift  (dimensional star schema, WLM-tuned)
        ↓
  Power BI Dashboards  (DirectQuery + scheduled refresh)
```

Monitoring layer: **Amazon CloudWatch** + **AWS Lambda** alerting + **Terraform** IaC tracking.

---

## 💡 Key Engineering Concepts Demonstrated

- **WLM Queue Monitoring** — visualizes concurrent workload balancing across analytics teams
- **Data Quality Framework** — 6-dimension scoring (completeness, uniqueness, referential integrity, domain, schema, freshness)
- **Pipeline SLA Tracking** — per-pipeline success rate against defined SLAs
- **Redshift Performance Metrics** — CPU, IOPS, QPM, connection pooling
- **Airflow DAG Run History** — 10-run color-coded run grid per DAG
- **Cost Attribution** — per-service AWS spend with IaC savings tracking
- **Live Metrics** — all KPI cards update every 2 seconds with realistic jitter

---

## 🏁 Running It

```bash
git clone https://github.com/saikiranakuthota/pipeline-pulse.git
open pipeline-pulse.html
```

Or deploy to GitHub Pages for a live URL in 60 seconds:
> **Settings → Pages → Branch: main / root → Save**

---

## 👤 Author

Built by [Sai Kiran Akuthota](https://github.com/saikiranakuthota)  
Data Engineer · AWS · PySpark · Redshift · Airflow · Power BI · Atlanta, GA

---

## 📄 License

MIT
