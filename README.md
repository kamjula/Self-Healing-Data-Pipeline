# 🔧 Self-Healing Data Pipeline

A Python + SQL data pipeline that detects its own failures and recovers automatically — handling missing values, schema drift, duplicates, and outliers without manual intervention.

## ✨ What It Does

| Feature | Description |
|---------|-------------|
| 🔍 Anomaly Detection | Flags missing values, type mismatches, duplicates, and statistical outliers per batch |
| 🛠 Auto-Recovery | Applies recovery strategies — imputation, quarantine, retry — based on failure type |
| 📋 Data Quality Scoring | Scores each batch and triggers alerts when quality drops below threshold |
| 🗒️ Audit Logging | Logs every pipeline run with failure type, recovery action, and timestamp |
| 🔌 Modular Stages | Ingest → Validate → Recover → Transform → Load — each stage is independently testable |

## 🚨 Self-Healing Logic

Each batch goes through:

1. **Detect** — validate against schema rules and statistical thresholds
2. 2. **Classify** — missing data / outlier / schema drift / duplicate
   3. 3. **Recover** — apply the right fix automatically
      4. 4. **Log** — full audit trail for every event
         5. 5. **Alert** — notify when quality score drops below threshold
           
            6. ## 🛠 Tech Stack
           
            7. Python · Pandas · SQL (SQLite / Postgres) · Logging · pytest
           
            8. | Layer | Technology |
            9. |-------|-----------|
            10. | Pipeline logic | Python + Pandas |
            11. | Storage & querying | SQL (SQLite / Postgres) |
            12. | Audit trail | Python logging module |
            13. | Testing | pytest |
           
            14. ## 📁 Project Structure
           
            15. ```
                Self-Healing-Data-Pipeline/
                ├── pipeline/
                │   ├── ingest.py        # Data ingestion
                │   ├── validate.py      # Quality checks + anomaly detection
                │   ├── transform.py     # Business logic
                │   ├── load.py          # Write to target store
                │   └── recover.py       # Self-healing recovery strategies
                ├── tests/
                ├── logs/
                ├── data/
                └── README.md
                ```

                ## 🚀 How to Run

                ```bash
                git clone https://github.com/kamjula/Self-Healing-Data-Pipeline.git
                cd Self-Healing-Data-Pipeline
                pip install pandas numpy pytest
                python pipeline/ingest.py
                ```

                ## 👩‍💻 Author

                Sravani Kamjula | Data Analyst &nbsp; [LinkedIn](https://linkedin.com) · [Portfolio](https://github.com/kamjula)
