# Self-Healing Data Pipeline 🔧🔄

An automated data pipeline with built-in anomaly detection, error recovery, and data quality monitoring — designed to self-diagnose and recover from common data failures without manual intervention.

![Python](https://img.shields.io/badge/Python-3.10+-blue) ![SQL](https://img.shields.io/badge/SQL-SQLite%2FPostgres-orange) ![Status](https://img.shields.io/badge/Status-Active-green)

## 🚀 Overview

This project simulates a production-grade ETL pipeline that monitors incoming data streams, detects anomalies (missing values, schema drift, outliers), logs failures, and automatically applies recovery strategies — all without human intervention.

## ✨ Features

- **Anomaly Detection** — Identifies missing values, duplicates, type mismatches, and statistical outliers
- - **Auto-Recovery** — Applies configurable fallback strategies (imputation, quarantine, retry logic)
  - - **Data Quality Scoring** — Assigns quality scores per batch with threshold alerting
    - - **Audit Logging** — Full pipeline run history with error traces and recovery actions
      - - **Modular Design** — Plug-and-play stages for ingestion, validation, transformation, and load
       
        - ## 🛠️ Tech Stack
       
        - | Tool | Purpose |
        - |------|---------|
        - | Python 3.10+ | Core pipeline logic |
        - | Pandas | Data processing & transformation |
        - | SQL (SQLite/Postgres) | Storage & querying |
        - | Logging module | Audit trail & diagnostics |
        - | pytest | Unit testing pipeline stages |
       
        - ## 📁 Repository Structure
       
        - ```
          Self-Healing-Data-Pipeline/
          ├── pipeline/
          │   ├── ingest.py          # Data ingestion layer
          │   ├── validate.py        # Quality checks & anomaly detection
          │   ├── transform.py       # Business logic transformations
          │   ├── load.py            # Output to target store
          │   └── recover.py         # Self-healing recovery strategies
          ├── tests/                 # Unit tests
          ├── logs/                  # Pipeline audit logs
          ├── data/                  # Sample input datasets
          └── README.md
          ```

          ## 🔍 Self-Healing Logic

          1. **Detect** — Each batch is validated against schema rules and statistical thresholds
          2. 2. **Diagnose** — Failures are classified (missing data, outlier, schema drift, etc.)
             3. 3. **Recover** — Recovery strategy is applied based on failure type
                4. 4. **Log** — All events are logged with timestamps for traceability
                   5. 5. **Alert** — Quality score drops below threshold trigger notifications
                     
                      6. ## 🚦 Getting Started
                     
                      7. ```bash
                         # Clone the repository
                         git clone https://github.com/kamjula/Self-Healing-Data-Pipeline.git
                         cd Self-Healing-Data-Pipeline

                         # Install dependencies
                         pip install pandas numpy pytest

                         # Run the pipeline
                         python pipeline/ingest.py
                         ```

                         ## 👤 Author

                         **Sravani Kamjula** — Data Analyst | [LinkedIn](https://linkedin.com) | [GitHub](https://github.com/kamjula)
