# ✈️ Aerospace Data Lakehouse Project

An enterprise-grade, end-to-end data engineering pipeline built on **Databricks**, utilizing **PySpark**, **Delta Lake**, and **Unity Catalog** to ingest, clean, validate, aggregate, and report on multi-source aerospace telemetry and operational data.

---

## 🏗️ Architecture & Notebook Structure

This project follows the **Medallion Architecture** pattern, divided into clean, modular notebooks stored in this repository:

```mermaid
flowchart LR
    A["Aerospace_source\n(Raw CSVs)"] -->|Bronze Notebook| B[("Bronze Layer\n(Raw Delta)")]
    B -->|Silver Notebook| C[("Silver Layer\n(Cleaned)")]
    C -->|Data Quality Notebook| D[("Data Quality\nChecks")]
    D -->|Gold Notebook| E[("Gold Layer\n(Aggregations)")]
    E -->|Final Reporting Notebook| F[("Reporting Ready")]
